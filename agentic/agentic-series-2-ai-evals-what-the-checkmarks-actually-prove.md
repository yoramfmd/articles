# AI Evals: What the Checkmarks Actually Prove

*Series: Agentic Experience Design, Article 2*

---

The conference room smells like cold coffee and mild anxiety. Someone has already updated the JIRA board with today's date. The dev lead has a demo queued up. The QA lead has a spreadsheet.

You open the ticket. You remind everyone what the epic was about, the persona you were targeting, the user stories behind the stories. You walk through the acceptance criteria, the ones you spent two hours debating three sprints ago, and the release criteria that the compliance team added after the last incident. The dev lead shows the demo. It works. The QA lead pulls up the test matrix and walks the room through forty-three test cases, each one traced back to an acceptance criterion, each one marked green. You count the checkmarks. Everyone counts the checkmarks. The engineering manager says "we're good." You say "ship it."

You have done this a hundred times. So has everyone in the room. Requirements become stories, stories become tests, tests become evidence, evidence becomes a release decision. The whole system runs on traceability.

Now your team is telling you the AI agent is ready to ship. They ran evals. Every test passed. The results report looks a lot like the QA matrix you just signed off on. And somewhere, quietly, you realize you have no idea whether it means the same thing.

It doesn't. The mental model that has served you for twenty years breaks in exactly three places when the system stops executing code and starts making decisions. The checkmarks are still there. What they prove is not.

---

## What Evals Actually Are

Before the three breaks, a grounding. An AI evaluation framework is the way you check whether the system behaves correctly, reliably, and safely before and after deployment. Not whether the code compiles. Whether the system makes the decisions it was designed to make, under conditions that resemble the real world.

Evals are not a complete validation system. They are partial observability tools. They approximate behavior under controlled conditions. They do not prove correctness. They bound uncertainty. The PM who treats a passing eval suite the way they treat a passing QA matrix has imported a precision that the tool does not actually provide.

---

## The Translation That Works

The structural mapping between your QA process and AI evaluation is direct, and worth naming clearly before getting to where it breaks.

An epic becomes an agent capability definition. Acceptance criteria become eval criteria: task success rate, intent resolution accuracy, tool call correctness. Unit tests become single-step evals checking one reasoning step or tool invocation. Integration tests become trajectory evals checking whether the full multi-step chain executes correctly end to end. The QA test plan becomes the eval suite. The traceability matrix can become an LLM-as-judge rubric mapped back to original criteria. UAT becomes human review of flagged agent trajectories. Regression testing becomes continuous evals that re-run after every model update or prompt change, because a model update is a behavioral change, not an infrastructure event.

The division of ownership is identical: engineering runs the evals, the PM owns what success means. You define the criteria. You set the pass thresholds. You review the failure traces.

But here is what the translation omits: the dataset is the product. What you choose to test becomes what you optimize for. The scenarios you include in the eval suite define the edges of what the system will be validated against. Most production failures happen outside those edges. This is not a tooling problem. It is a coverage problem, and it belongs to whoever owns the criteria.

---

## Where the Model Fails

**The determinism problem.** In traditional software QA, a passing test proves the code will behave correctly. Given the same input, the same code produces the same output, every time. One green checkmark means the behavior is fixed.

In agentic AI, one green checkmark is a sample from a distribution. Even in systems configured for low variance, non-determinism persists at the system level due to retrieval variability, external tool responses, and context differences across sessions. The same agent, given the same task on different days, may succeed, fail, or take a path you did not anticipate.

The practical consequence: binary pass/fail is not a sufficient quality gate for agentic AI. Leading teams use repeated sampling and distribution-based metrics, tracking success rates across multiple runs and monitoring the shape of that distribution over time. A system that succeeds six out of eight attempts may be acceptable for low-stakes automation. For anything that touches a customer, a financial record, or a consequential workflow, that is a meaningful failure rate dressed up as a green checkmark.

The first question to ask when your team presents eval results is not "did it pass?" It is "how many times did you run it, and what was the distribution?"

The practice has a name in the eval literature: pass@k. You run the eval k times, typically somewhere between five and ten, and report the success rate across the distribution, not the result of a single run. A team that presents one green checkmark on a non-deterministic system has not told you whether the agent passed. They have told you it passed once.

**The compound probability problem.** This one has no equivalent in traditional software development, which is why it catches experienced PMs off guard more than anything else.

Suppose your agentic system runs a ten-step workflow: search, retrieve, filter, extract, format, validate, draft, review, send, log. Every single step passes at 95% accuracy in isolation. In a traditional system, you sign off.

In an agentic system, 95% accuracy across ten steps produces an end-to-end success rate of roughly 60%. The math: 0.95 to the power of 10 is 0.598. End-to-end reliability is the product of the steps, not their average. That said, this assumes the steps are independent, which rarely holds in practice. In real systems, errors are often correlated, and some workflows include recovery steps that partially compensate. The actual degradation can be higher or lower. What the math guarantees is that component-level accuracy and system-level reliability are different numbers, and that difference grows with every step added to the chain.

If your eval suite tests each component in isolation, you have not tested the system. You have tested the components.

**The background failure problem.** In traditional QA, execution is observable. The code either ran or it did not. Deterministic execution means you can always verify that the intended action occurred.

An agentic system can produce a semantically correct output, pass the eval, and never have triggered the underlying action. In multiple production deployments, audits have revealed cases where "order updated and closed" messages never corresponded to any API call. The agent wrote the right words, the automated judge scored the output as accurate, and the test passed. No state validation layer. Invisible to metrics until someone looked directly at the system state.

Semantic validation reads what the agent said. State validation checks what actually changed. You need both. A release gate that runs one and calls it done has half a gate.

---

## The Coverage Problem

Evals only test what someone thought to test. Every scenario in the eval suite represents a hypothesis someone had before launch about how the system might behave. The long tail of production behavior, the edge cases no one anticipated, the combinations of inputs that only emerge at scale, the adversarial patterns that users discover in real use, none of those appear in the pre-launch eval suite. Most consequential production failures happen outside the scenarios anyone thought to include.

Coverage is not a scoring problem. You can have a perfectly designed rubric with excellent calibration and still be measuring the wrong things. The hardest question in eval design is not "how do we score this?" It is "what are we missing?"

This is the same reason roughly 95% of AI proof-of-concepts succeed in the demo and fail when moved to production. The PoC was built on curated data that matched the team's assumptions. The eval suite was built on scenarios the team thought to include. Production arrived with live, messy, real-world data that matched neither. The mechanism is identical. The scale is different.

---

## Evals Inform Risk. They Do Not Eliminate It.

Evals are not a binary release gate. Leading teams treat them as one signal among several. A passing eval suite informs the release decision. It does not make it.

In practice, responsible agentic deployments pair offline evals with production monitoring: canary releases to a small percentage of traffic, shadow testing against live inputs, feedback loops that surface failures as they occur, and drift detection that catches behavioral changes introduced by model updates or shifting data. The most important evals often happen after deployment. Real-world variability exposes behaviors that no offline suite can fully anticipate.

The PM who waits for every eval to pass before signing off has the wrong mental model. The PM who ships with eval coverage, production monitoring, and a clear incident response path has the right one.

---

## What the PM Owns

The PM's role in the eval process is what it has always been: own the definition of success. But the definition has components that do not exist in traditional QA.

Define what graceful failure looks like. An agent that cannot complete a task has two options: fail silently or fail legibly. Only one is acceptable, and the PM is the right person to specify which.

Set the end-to-end pass threshold, not just the component thresholds. If the team is reporting component accuracy, ask for the system-level number.

Own the coverage decision. Which scenarios are in the eval suite? Which user intents, failure modes, and adversarial inputs did you choose to test? That selection is a product decision with real consequences, and it belongs with whoever owns the criteria.

Define the acceptable tradeoffs. Not just success, but the acceptable balance between cost, latency, reliability, and human oversight. Those tradeoffs determine how the eval criteria are weighted, and they require a PM judgment, not an engineering default.

Before sign-off, ask: did you run state validation, not just semantic validation? What does the distribution of outcomes look like across repeated runs, not just a single pass? What is the True Negative Rate on your automated judge? If the team cannot characterize that number, they do not know whether the automated quality gate is catching the failures that matter.

---

## The Checkmarks Are Still There

The release decision meeting for an agentic system looks the same from the outside. Someone has updated the JIRA board. The dev lead has a demo. The QA lead has a results report. The checkmarks are still there.

What has changed is what they prove. A passing eval suite tells you the agent behaved correctly in the scenarios someone thought to test, under controlled conditions, at one moment in time. It bounds uncertainty. It does not eliminate it.

The teams that understand this before they ship do three things differently. They pair offline evals with production monitoring from day one. They treat the first weeks of deployment as an extension of the eval process, not its conclusion. And they build incident response into the release plan before anyone asks for it.

The teams that carry the traditional checkmark model into agentic AI intact discover the gaps the same way most software gaps get discovered. In production. By users. In ways that were never in the test suite.

Because the test suite only catches what someone thought to measure. In agentic AI, that gap is wider, more consequential, and far less obvious than anything on the QA lead's spreadsheet.

---

*This article is part of an ongoing series on AI product design, healthcare data, and the human side of technology adoption.*
