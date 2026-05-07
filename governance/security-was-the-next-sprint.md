# Security Was the Next Sprint

*Published: [date] | Tags: Product Management, Agentic AI*

---

There is a pattern in how enterprise agentic AI gets built right now.

The team identifies a use case. The use case is real. The model works. The demo is clean. The pressure to ship is enormous because three competitors announced agent counts last quarter and the board noticed.

Security comes up in the planning meeting. Someone says: we will harden it in the next sprint. Everyone nods. The sprint after that, the team is already three features behind. Security becomes the standing agenda item that moves every week. By the time the system has real users and real permissions, the hardening sprint has never arrived.

This is not negligence in the usual sense. It is rational behavior under a specific set of incentives. Shipping fast is visible. Security gaps are invisible until they are catastrophic. The organization rewards the visible thing, defers the invisible one, and discovers the cost later.

Two papers published this year put a number on what that deferral actually costs.

---

**What the research found**

Researchers at AWS and UC Berkeley tested 483 attack scenarios against every major frontier model, including GPT-4.1, Claude, and Gemini. They were looking at a specific attack class they call Sequential Tool Attack Chaining, or STAC. The idea is straightforward once you see it: instead of sending a malicious instruction in one step (which modern AI safety systems are reasonably good at flagging), you chain a sequence of tool calls where each individual step appears completely legitimate. The malicious outcome only becomes apparent at the final execution step.

The results are not subtle. Attack success rate exceeded 90% on GPT-4.1. Similar numbers held across all tested models. The best single defense they found, a harm-benefit reasoning prompt, cut the success rate by 28.8% initially, but degraded over multiple conversation turns.

The second paper, from a research team at Stanford, MIT CSAIL, CMU, and Elloe AI, audited 847 production agentic deployments. They mapped six vulnerability classes across those systems and found that tool privilege escalation was present in 95% of deployments. Memory poisoning was present in 94%. These are not exotic attack surfaces. They are the default configuration of most enterprise agentic systems as they are currently built and shipped.

The same paper documents what they call the OpenClaw incident. A single database exploit simultaneously compromised 770,000 live agents. Each agent had privileged access to its owner's machine, email, and files. The attack was not sophisticated. It found the key in the lock because the lock was designed to be convenient, not secure.

---

**Two cultural forces, one outcome**

The research describes what is technically possible. It does not explain why the doors are open. That explanation is cultural, and it has two parts.

The first is what I will call fermentation culture: the belief that you need to ship as many agents as fast as possible because speed is the moat. The race to announce 500 agents is real. Enterprise vendors are using agent count as a benchmark for competitive position. The measure that should matter, what those agents can do and what they can be made to do, is not the measure being tracked.

Fermentation is a useful metaphor. Fermented systems are alive and changing. They produce value. They also produce unpredictable byproducts if you do not design the container correctly. Most enterprise agent deployments right now are living systems without a designed container. The fermentation is happening. The vessel has not been built for what it contains.

The second force is MVP culture applied to security. Minimum Viable Product thinking was built for the feature layer: validate the hypothesis, ship something real users can test, iterate from there. It was never designed for the security layer, because security is not a hypothesis you can validate with a subset of users. It is a property of the whole system, and it either holds or it does not.

When a team says "we will secure it in the next sprint," they are applying MVP logic to a domain where that logic breaks. The MVP assumption is that the cost of the first version's defects is bounded, because only a small number of users are affected, and the feedback loop is fast. In agentic AI security, the cost is not bounded. An agent with overprivileged tool access and a poorly scoped autonomy boundary is not a beta feature. It is a surface that an attacker can walk across at scale, as the 770,000-agent incident illustrates.

---

**The design gap the research is actually naming**

I have been writing about the four runtime design artifacts that every agentic product requires before it ships: the autonomy boundary, the approval moment, the audit surface, and the recovery workflow.

The STAC paper is describing what happens when the autonomy boundary is too broad. The attack chains work because the agent has been given permission to use a wide range of tools in a wide range of contexts. There is no specification of which tool combinations are authorized for which task types, or what a sequence of actions would have to look like to trigger a review. The boundary was drawn at the task level, roughly: this agent may do procurement work. It was not drawn at the action level: this agent may use these tools, in these sequences, within these parameters, and any deviation flags for review.

The 95% tool privilege escalation rate from the 847-deployment audit is the same finding, stated differently. Most agents have been given more permission than they need for the task they are performing. The principle of least privilege, which is foundational security engineering, was not applied. Not because the teams did not know about it. Because applying it rigorously requires finishing the autonomy boundary design before shipping, and finishing the autonomy boundary design requires time that the fermentation culture does not leave.

The audit surface finding is equally direct. If an agent's actions are not reconstructable for a post-incident review, you cannot determine what happened, what data was accessed, what instructions were followed, or where the chain of tool calls diverged from the intended workflow. The STAC attack chains are designed to be invisible at every intermediate step. The only way to detect them is a complete action trace, not the agent's own description of what it did. Chain-of-thought reasoning and audit surface are not the same thing. The agent can describe its actions coherently while the underlying system state tells a completely different story.

---

**What the next sprint actually costs**

The product teams shipping agents under quarterly pressure are not wrong that speed matters. They are wrong about what speed is for.

Speed in the early phase is for learning, not for locking in technical debt at the trust layer. An agent that earns trust through visible, legible behavior, with a scoped autonomy boundary and an audit surface that works, can be extended. An agent that earns adoption through convenience and loses trust through a single incident of unexplained behavior cannot be recovered easily. The Dietvorst research on algorithm aversion is clear on this: a single visible failure erases more trust than many correct outputs accumulated. In agentic AI, the failure mode the research is documenting is not "the agent made a wrong decision." It is "the agent was made to execute a malicious action chain while appearing to function normally." That is a harder failure to recover from, because the users are not sure what the system did or whether it is safe to use again.

The security sprint that never arrives is not free. It is a deferred cost with compound interest, paid when the incident finally makes the invisible visible.

---

**What this means in practice**

The autonomy boundary design is not a security exercise separate from the product. It is part of the product. What the agent may do, in what sequences, with which tools, under what conditions, reviewed by whom, when that review is triggered, these decisions determine what the attack surface looks like. Teams that make these decisions explicitly before shipping have a smaller surface to defend. Teams that defer them have, by default, granted the agent broad permissions because broad permissions were the easiest path to the demo.

The 95% tool privilege escalation rate is not a measure of how many teams are negligent. It is a measure of how many teams shipped the path of least resistance and called it good enough.

Least privilege is not a constraint on the agent's usefulness. It is the precondition for the agent being trustworthy enough to remain in production after the first incident. An agent that is useful but cannot survive a post-incident review is not a shipped product. It is a deferred liability.

The next sprint will come for all of us. The question is whether it comes before the incident or after it.

---

*These questions sit at the center of what I write about in the Agentic Experience Design series: what it actually means to design a system that acts, not just recommends, and what the enterprise PM owes the people and systems that the agent will touch.*

*The two papers referenced are "From Glue to Glow: Sequential Tool Attack Chaining in Agentic AI" (Greshake et al., 2025) and "Toward an Immune System for Agentic AI" (Stanford/MIT CSAIL/CMU/Elloe AI, 2025).*

---

**Sources**

1. Greshake et al., "From Glue to Glow: Sequential Tool Attack Chaining in Agentic AI," arXiv 2509.25624v2 (2025). AWS/UC Berkeley. Attack success rate >90% on GPT-4.1 across 483 test scenarios.
2. "Toward an Immune System for Agentic AI," Stanford/MIT CSAIL/CMU/Elloe AI (2025). 847 production deployments audited. Tool privilege escalation 95%, memory poisoning 94%.
3. Dietvorst, Logg, and Loewenstein, "Algorithm aversion: People erroneously avoid algorithms after seeing them err," Journal of Experimental Psychology: General (2015).
4. "You Built the Agent. Nobody Designed the Experience," Yoram Friedman, LinkedIn, April 2026.
