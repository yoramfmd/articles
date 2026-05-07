# Not Every Problem Deserves an Agent

*Series: Agentic Experience Design, Article 0*

---

The most expensive agentic AI mistakes you can make are not engineering failures. The model worked. The integration held. The agent did what it was designed to do.

The problem was the problem itself.

The use case was never a good fit, and the team discovered this after six months of development, a production deployment, and an invoice that was difficult to explain to finance.

This happens predictably and often. Not because product managers are careless, but because the evaluation frameworks for agentic AI are different from anything they have used before. Deciding whether to build a mobile app, a new API, or a data pipeline involves a familiar set of questions: who is the user, what is the job to be done, what does success look like? Those questions are necessary but not sufficient for agentic systems. Two additional frameworks are needed before the first line of code is written: a suitability assessment and a cost model. Most teams skip both, and pay for it later.

---

## Is This Problem Right for an Agent?

Not every task benefits from agency. The clearest signal of a misfiled use case is a team describing an agentic solution to a problem that occurs once a quarter, or that requires a level of contextual judgment no amount of tool access can replicate, or that is already solved adequately by something simpler and cheaper.

A problem is well suited for an agent when four conditions hold.

First, the decision repeats at volume. An agent creates value by handling many instances of the same decision type across time. A one-time strategic call, however complex, does not benefit from agency. The test question: how many times per day or week does this decision get made in the organization today?

Second, the outcome is measurable. If you cannot define what a correct decision looks like, you cannot evaluate the agent, detect when it drifts, or calibrate user trust over time. Outcomes that depend on stakeholder politics, relationship history, or unstated organizational preferences are not measurable in the sense an agent requires. The test question: can you score a sample of past decisions as right or wrong without significant disagreement among the people who made them?

Third, the tool use is bounded. Agents with broad system access will eventually touch something you did not intend. The value of an agent scales with the precision of its tool boundaries, not the breadth of its permissions. The test question: can you enumerate every system the agent needs to access to complete the task, and nothing beyond?

Fourth, the consequences are recoverable. Wrong decisions happen at a predictable rate. The suitability question is whether the cost of a wrong decision, at the rate this agent will produce them, is one the organization can absorb without structural damage. The test question: what does the worst-case failure look like, and what does recovery actually cost?

---

## Where Agents Fail by Design

The research on agentic AI performance converges on a consistent pattern. Agents succeed at tactical decisions: high-volume, bounded, measurable, with feedback loops that allow evaluation and calibration. Recommendation ranking, document routing, alert triage, scheduling optimization, data extraction. They fail at strategic decisions: goals requiring judgment, private organizational knowledge, novel situations without precedent, and decisions where being wrong has asymmetric consequences.

This failure is not random and it is not a model quality problem. It is a problem type problem. Deploying an agent into a strategic decision domain produces confident wrong answers at volume, which is materially worse than the human process it replaced.

The private knowledge gap is the most underappreciated dimension of this. An agent trained on organizational data cannot replicate the judgment of a person who knows the relationship history, the political constraints, or the unwritten rules that govern a given decision. Sales outreach to a specific account, executive communications, strategic vendor negotiations, performance conversations all fall into this category. Teams that automate these workflows are not saving time. They are trading human judgment for machine confidence on exactly the decisions where confidence without judgment is the core failure mode.

---

## The Cost Model Most PMs Never Build

Here is the question that separates teams that deploy agents successfully from teams that quietly decommission them three months later: at what task volume does this agent break even against the best available alternative, and is that volume realistic within the planning horizon?

Most agentic AI business cases are built on capability assumptions. The agent can do this task. It can do it faster. It can scale. What they omit is the cost structure, which is fundamentally different from every other technology investment a PM has evaluated before. And the evidence on this is now clear: Gartner estimates that more than 40 percent of agentic AI projects will be canceled by the end of 2027 due to escalating costs and unclear business value. McKinsey's 2025 AI survey found that fewer than 10 percent of organizations have scaled agents in any single business function. Ninety-five percent of AI pilots fail to produce measurable financial impact. These are not failure rates from poor execution. They are the predictable outcome of cost models that were never built.

Agentic AI has three cost layers that need to be modeled before the build decision.

The floor price is the minimum cost the system incurs regardless of business value delivered. Recent industry analysis on production agentic deployments shows first-year costs in the $175,000 to $450,000 range for enterprise systems, with evaluation and monitoring alone running $60,000 to $120,000, often larger than the inference cost. This floor exists whether the agent handles two tasks per day or two thousand. Most business cases are modeled on optimistic volume assumptions. Almost none model what the system costs when volume comes in at half of projection. Organizations routinely underestimate total cost of ownership by roughly 40 to 60 percent because they anchor on the vendor quote and miss the compounding expenses: orchestration, monitoring, security review cycles, human oversight, and the ongoing maintenance triggered by model updates every three to six months. A useful correction: take whatever number is in the business case and multiply it by 1.4 to 1.6 before presenting it to a finance audience.

The per-task operational cost is where the comparison becomes concrete. A customer service representative costs approximately $4.60 per interaction when salary, benefits, and overhead are included. Salesforce Agentforce handles similar interactions for $0.10 to $1.50 depending on task complexity and billing method. That gap is real and it is the foundation of the strongest business cases for agentic AI. But it only holds for tasks that are high-volume, bounded, and measurable enough for the agent to complete reliably end-to-end. The unit economics collapse the moment significant human review is required on every output. KPMG's Q1 2026 survey reported that roughly 63 percent of enterprises require human validation of agent outputs, up from about 22 percent the previous quarter. Human oversight does not disappear because you deployed an agent. It gets restructured into a recurring labor cost that must be included in the per-task model.

The cost trajectory is where most of the surprises live. Agentic AI costs scale with task volume and with task complexity in ways that headcount does not. You hire one person and the payroll cost is fixed regardless of how many decisions they make that month. An agent handling ten times the volume costs roughly ten times as much to run. And task complexity compounds the problem: in multi-agent architectures, internal analyses and published benchmarks converge on a pattern where roughly 37 percent of total token consumption is coordination overhead, the compute required just to re-establish context and hand off instructions between agents. A four-agent system consumes approximately 3.5 times as many tokens as a single-agent implementation for the same outcome, before any retries or error handling. The crossover point where the agent becomes cheaper per task than the alternative only exists at a specific volume and complexity threshold. That threshold needs to be modeled before the team commits.

A concrete frame for the break-even question: deploying an enterprise agentic workflow in a single HR function often lands in the $450,000 to $650,000 first-year range in real deployments. To achieve a 12-month return on investment, the organization needs to displace the work of six to ten full-time employees through efficiency gains. That is not an argument against building. It is an argument for knowing the number before the project starts, and for choosing the function where that displacement is achievable and measurable. The teams that model this before building find the right use cases. The teams that discover it on the invoice have a different conversation.

---

## The Right Comparison

The correct comparison for an agentic solution is not "agent versus doing nothing." It is "agent versus the current best alternative," which is often a human, a traditional automation, or a simpler AI integration that costs a fraction of a full agentic system.

For many workflows, the right answer is not an agent. It is a simpler system that quietly does the job.

The most documented version of this pattern is in enterprise customer service. Companies launch with a vision of an end-to-end agent that handles support cases across channels, calls tools, and closes tickets without human involvement. During pilot, three cost drivers appear that were not in the original model. Multi-step planning, retries, and tool calls drive 10 to 50 times more tokens per task than a single-shot model, pushing variable cost per resolved ticket above what a simpler chatbot or RPA workflow would have cost. Orchestration overhead accumulates: approval gates, audit trails, monitoring, and governance layers that the safety requirements demand. And integrating the agent with legacy ticketing systems, knowledge bases, and identity infrastructure turns the quick win into a multi-year process redesign that burns budget before any savings appear. When the team runs the head-to-head comparison, the fully agentic path carries a higher cost per resolved ticket with no measurable improvement in resolution rate or customer satisfaction. The board or CFO cancels the agent initiative and standardizes on the constrained assistant plus RPA pattern that should have been the baseline comparison from the start.

Traditional automation handles deterministic, rule-based processes at very low per-task cost with no inference cost. For simple routing, the marginal cost of a traditional system is under $0.001 per task. An agentic system handling the same routing runs $0.10 to $0.20, plus coordination overhead. For more complex workflows like scheduling, traditional automation costs under $0.01 per task; an agent costs $0.60 to $1.20. Traditional automation is five to ten times more cost-efficient for routine, deterministic tasks. If the task can be solved with scripted logic or RPA, an agent is the wrong tool. The cost differential is not marginal. It is structural.

Simple AI integrations, classification, extraction, summarization without action, cost significantly less per task than full agentic workflows and are sufficient for a large share of problems that teams are currently over-engineering into agents. The question is not whether AI is the right technology. It is whether the action component of the agent adds enough value to justify the cost differential over a simpler integration. Most teams never ask that question explicitly. They should.

The Klarna case shows what optimizing the wrong objective function looks like in production. Klarna, the company that lets you split online purchases into installments, built an AI assistant that by early 2024 was handling the workload of roughly 700 agents, with cost per transaction falling from $0.32 to $0.19. The model worked. By mid-2025 the company rebalanced toward human support, not because the AI failed but because over-indexing on cost per interaction had degraded quality in edge cases and complex interactions. CEO Siemiatkowski's explanation was direct: "Cost was too predominant an evaluation factor... what you end up having is lower quality." Klarna did not misjudge AI's capability. It misjudged the total cost of quality degradation, the irreversibility of bad customer interactions, and the role of human judgment in tail cases. The task type was high-volume, bounded, and measurable. The suitability criteria looked right. What the evaluation missed was the fourth condition: the consequences of getting edge cases wrong were harder to recover from than the model assumed. The system worked. The evaluation framework did not.

---

## Before You Commit

Healthcare happens to be the field where AI is being stress-tested under the most demanding conditions, with the highest stakes, the most rigorous evaluation requirements, and the least tolerance for confident wrong answers. Which is why it keeps producing the frameworks that other industries eventually adopt. In clinical practice, treatment selection begins with a candidacy assessment: indication, contraindication, risk-benefit ratio at the patient level. The procedure may be excellent. The question is whether this patient, at this moment, is the right candidate.

The same logic applies to agentic AI. The four conditions above are the suitability assessment. If any of them cannot be answered with confidence, the problem is not ready for an agent. If all four hold, one cost question remains: at what task volume does this agent break even against the current best alternative, and will you realistically reach that volume within twelve months?

If neither question has a clear answer, the team is not ready to build. They are ready to do more scoping. That distinction matters, because an agent deployed into the wrong problem does not just fail to create value. It creates a specific kind of damage: automated confidence applied at scale to decisions that required judgment. That is harder to recover from than a project that was never started.

The agent is a powerful tool. The work is choosing the right problem for it.

---

*This article is part of an ongoing series on AI product design, healthcare data, and the human side of technology adoption.*
