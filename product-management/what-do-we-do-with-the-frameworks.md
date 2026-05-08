# What Do We Do With the Frameworks?

*The PM toolkit was built for a world where the human is smarter than the tool. That assumption is expiring.*

---

Over the course of twenty years, I interviewed hundreds of customers in settings that had nothing in common except the presence of someone willing to talk to a product manager. Conference floors at TechEd, where you smile for eight straight hours until your face stops cooperating. A chemical plant meeting room in Germany where the safety video played on a loop in the corridor outside. A warehouse full of energy drinks somewhere in Central Europe, run by a logistics director who kept glancing at his phone. Glass-walled innovation suites where the team sat in circular furniture and the whiteboard was always freshly erased.

In each of them, I asked the questions the methodology requires: not what do you want, but what are you actually trying to do, and what would a good day look like if we got this right. I ran dozens of design thinking workshops, drew user journey maps in every tool the industry ever produced, and wrote Jobs to Be Done statements with the quiet confidence of someone who has done it enough times to recognize a good one. All of it was genuinely useful.

And yet, sitting here in early 2026, thinking about what it means to design agentic AI systems, I find myself uncertain whether the toolkit I spent twenty years assembling is adequate for the problem now in front of me. Not because the tools are wrong. Because the assumptions buried inside them may no longer hold.

Every product framework we use was built on a single unstated assumption: the human is the expert and the software is the instrument. That assumption is now negotiable.

The classic PM frameworks still apply, but at a different layer than they were built for. The bigger shift is in what a product definition now has to contain: not just features, but authority, boundaries, and what happens when the system is wrong.

---

### The Innovator's Dilemma and Its Limits

Christensen's insight was that disruptive technologies start simple and cheap, serve overshot customers the incumbents ignore, and eventually eat the market from below. The framework is brilliant and has correctly predicted dozens of technology transitions.

Agentic AI does not fit this pattern cleanly in most enterprise deployments. It is not starting simple. It is not coming from below: the companies deploying it are often the incumbents, adding it to mature products with deep customer relationships. Some agentic AI does come from below, particularly in back-office automation where low-cost tools are replacing expensive manual processes, and in those cases the Christensen pattern holds reasonably well. But in the enterprise deployments attracting the most capital, the disruption looks different.

A more precise frame comes from economists Agrawal, Gans, and Goldfarb in "Prediction Machines": AI is, at its core, a dramatic drop in the cost of prediction. When something gets dramatically cheaper, the value shifts to whatever complements it. A logistics company that once paid analysts to predict which shipments would be delayed now has that prediction at near-zero cost. What becomes scarce, and therefore valuable, is the clean, structured, domain-specific data that makes the prediction accurate, and the judgment about what to do with the result. The prediction is the commodity. The data is the asset. This is part of why the Innovator's Dilemma maps imperfectly onto AI: what is being disrupted is not a product category, but a cognitive input, and the value is accruing to whoever controls the data of record.

---

### Crossing the Chasm Requires a New Kind of Product

Moore's insight was that the gap between early adopters and the pragmatist majority is wider than it looks, because pragmatists want a complete solution, not a promising technology. The "whole product" around the core innovation, integration, support, reference customers, is what crosses the chasm.

For AI agents in enterprise software, the whole product now includes something Moore did not have a name for: a governance framework. An accountability structure. A way for the organization to know what the agent is deciding, why, and who is responsible when it is wrong. These are not technical features and they are not a bolt-on; they are a central component of the value proposition for pragmatist buyers. The chasm in AI adoption is less about technology readiness than about institutional readiness. That is a different problem, and a different kind of PM work to solve it.

---

### Jobs to Be Done Needs a Second Layer

The one that troubles me most is Jobs to Be Done, the framework that holds that people do not buy products, they hire them to do a job. The job is stable even when the technology changes. Understanding the job gives you the durable insight; the product is just the current best solution.

This works well when the user knows what job they need done. It starts to strain when the AI system can discover jobs the user did not know they had. Consider a logistics coordinator using a routing tool. The job they can articulate is clear: get the freight from A to B at acceptable cost. JTBD applies well. But the agentic system can also discover that shipments from a particular supplier consistently arrive late when two specific carriers handle the last leg, a pattern invisible to the coordinator but obvious in the data. That is not a job the user articulated. It is a job the system found by reasoning over information no single person had time to analyze.

This does not mean JTBD fails. It means the framework needs a second layer: not just jobs users know they have, but jobs the AI discovers and proposes back to them. The underlying question, "whose job is it when the AI defines the job?", is one the framework was never designed to answer. It is also one of the more interesting product design questions in enterprise software right now.

User journey mapping assumes there is a human doing the journeying. When the agent does most of the steps, you are mapping a workflow, not an experience. The distinction matters.

---

### Journey Maps and the Collapse of the User Path

User journey maps trace a human's experience through a process: the emotional state at each stage, the pain points, the handoffs between channels. This is genuinely useful for finding where software can help.

When an agent handles most of the steps autonomously, the journey map collapses. The human's path shrinks to a short series of intervention points: approve this, review this flag, override this recommendation. Everything in between is the agent's workflow, which is a different kind of design problem. The map that matters is no longer the user's emotional journey through a process; it is a boundary map between what the agent does alone and what requires a human. Nobody has a standard notation for that yet, which may be why so many agentic products feel well-designed in demo and poorly designed in production.

---

### Benefits vs. Capabilities When the Benefits Are Unknown

The benefits-versus-capabilities principle has been around long enough to feel obvious: customers do not care about your capabilities, they care about what those capabilities do for them. Sell the outcome, not the feature.

This becomes philosophically interesting when the capabilities are not fully enumerable at the time of sale. An agentic system deployed in enterprise logistics will, over time, surface value that was not anticipated during design: correlations between supplier patterns and on-time delivery that only become visible when operational and financial data are analyzed together, demand signals that procurement never had access to. You cannot sell these as specific benefits because you do not know they exist yet. The product narrative shifts from a feature list to a platform and a pattern of discovery. For a CFO or COO buying it, the argument is not "here is what it does" but "here is the organizational capability you are acquiring." That requires a different kind of trust, and a different kind of PM to build the case.

The frameworks are not wrong. They were built for a world where the PM understands the problem better than the system does. That is no longer guaranteed. And that changes where PM judgment actually applies.

---

### Three Questions Every PM Should Answer Before Calling a Product an Agent

Before getting to what should change, it helps to name what is going wrong. The industry is quietly developing what might be called agent washing: products marketed as autonomous agents that are, on inspection, sophisticated rule-based automations with a language model at the front. The demo is impressive. The underlying product does not attach to any decision that matters economically. Gartner projects that over forty percent of agentic AI projects will be scrapped by 2027 as organizations realize the underlying specification problem was never solved. This is largely a failure of product management, though organizational incentives and the absence of clear regulatory standards also shape the outcome. The frameworks we have do not address it directly.

Three questions every PM should answer before shipping an agent:

1. Which specific decisions does the agent make, under what authority, and with what stop conditions?
2. How good is good enough, and what happens when the system is wrong? Who detects it, and how does the organization recover?
3. What does the user control, and how does that control change as the system earns autonomy over time?

These are product definition questions, not QA questions. Most current AI product documents spend three paragraphs on what the agent does autonomously and one sentence on error handling. That ratio is backwards. The "when wrong" specification belongs in the requirements document at the same level of detail as the happy path, because in a system making consequential decisions at speed, the unhappy path is not the edge case. It is the accountability surface.

---

### The Autonomy Ladder

Full automation is not a starting point. It is an earned state. The responsible design pattern has three stages, and skipping any of them is the structural cause of most agentic AI failures in production. Demos succeed because they avoid the edge cases. Production systems fail because nobody specified what the edge cases were, or who handles them.

Stage 1, augmentation: the agent surfaces information, flags patterns, and makes recommendations. The human decides. This is where every agentic product should start, without exception.

Stage 2, limited-scope automation with approval gates: the agent acts in defined, bounded domains after a human has reviewed its reasoning. The scope is narrow, the authority is explicit, and the stop conditions are documented before deployment.

Stage 3, semi-autonomous operation with guardrails: the agent operates across a wider scope, but only after failure modes have been documented in production, recovery mechanisms have been tested under real conditions, and the organization has demonstrated it can detect when the system is wrong before consequences become irreversible.

The PM's job in an agentic product is not to specify what the agent does. It is to specify when the agent earns the right to do more, and what it has to demonstrate before that happens.

---

### The Real Design Problem

None of this means the classic frameworks are obsolete. The Innovator's Dilemma still correctly describes why incumbents miss transitions. Crossing the Chasm still correctly describes the institutional trust gap that kills enterprise AI pilots in year two. Jobs to Be Done still anchors PM work to real human struggles rather than invented feature requests. Journey maps still reveal where humans are in pain. Benefits over capabilities still prevents product teams from disappearing into technical complexity nobody asked for.

What has changed is the layer at which these frameworks apply. They used to be tools for understanding the user and specifying the system. They are now more useful for understanding where the human still matters and where the agent takes over, which is a different and more consequential design question.

The design problem that none of the frameworks fully address is the boundary itself: how much authority does the system have, when does it surface its reasoning, what does a well-designed escalation look like, and how does the user stay in control of something that is more capable than they are in specific domains. The leaders who will navigate this shift are the ones who treat authority, accountability, and the "when wrong" spec as first-class design objects, not afterthoughts, and who understand that the most important boundary they are drawing is not the one between features, but the one between human judgment and machine autonomy.
