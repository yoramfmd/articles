---
title: The Smartest Person in the Room Is a Prompt
slug: the-smartest-person-in-the-room-is-a-prompt
published: 2026-02-02
excerpt: At 2am, every product manager runs the same simulation, an imaginary room of stakeholders. The problem? You built the room. AI can become the same echo chamber. There are five levels of working with AI, and only the higher ones truly challenge your thinking.
---

At some point in the life of every product decision, usually around two in the morning the night before it has to be made, the product manager runs the mental simulation. What will the CFO say. What will the engineering lead say. What will the customer who called last Tuesday say when she sees what the roadmap actually produced. The simulation feels rigorous. It is not. It is a hall of mirrors built from the objections you have already survived, staffed entirely by people whose reactions you think you can predict, and constitutionally blind to the perspective you have not yet encountered and therefore cannot model. You are not consulting the room. You are consulting your memory of the room. The consensus you reach at two in the morning is consensus with yourself.

For twenty years I ran that simulation and called it judgment. I was wrong about what it was.

There is a version of this article that tells you AI is going to replace product managers. This is not that article. What I want to describe instead is something I have watched unfold across years of building products with and without AI tools: a genuine skill hierarchy that most practitioners are only beginning to climb, with each level unlocking capabilities the one below it simply cannot produce.

### The Question Nobody Is Asking Carefully Enough

Most product managers I know are using AI. Almost none of them are using it in a way that produces something they could not have produced without it.

This is not a criticism. It is a description of a natural adoption curve, and the curve has a shape worth understanding if you are trying to get ahead of it. Most practitioners are at level one or two of a five-level hierarchy. They believe they are at three or four. The distance between where they are and where the ceiling is represents the single largest untapped productivity opportunity in the profession right now.

The five levels are not about the AI getting smarter. The AI is the same at every level. What changes is the quality of the structure you bring to the conversation, and specifically how much epistemic discipline you have built into what you are asking for.

### Level 1: The Query

You type a question. The AI answers it. You are using a very fast reference tool, and there is genuine value in that, but it is the value of a capable intern who has read everything and forgotten nothing, not the value of a colleague who will tell you when you are wrong.

> *"What is the potential market opportunity for AI-assisted clinical documentation tools in US hospital systems?"*
What you get back is accurate, comprehensive, and generic. It is the same answer any well-briefed analyst would give any client asking the same question. The AI knows nothing about your company, your competitive position, your existing relationships, or the specific assumption embedded in the way you phrased the question. It answers what you asked, which is a general question.

Most of the people who say they have integrated AI into their product practice are here, or just above it.

### Level 2: The Frame

The first meaningful upgrade is learning that output quality is a direct function of input specificity. You stop asking questions and start writing prompts: structured inputs that give the AI a role, a context, a task, and constraints. The output improves significantly and immediately.

> *"You are a healthcare market analyst at a mid-size health technology company with strong relationships at twelve academic medical centers but limited presence in community hospitals. Assess the market opportunity for AI-assisted clinical documentation, specifically comparing academic medical center expansion versus community hospital entry, including the different procurement processes, clinical champion profiles, and competitive dynamics in each segment."*
The delta is real. Segment-specific analysis instead of a market overview. Procurement dynamics that actually differ between the two settings. A competitive landscape that reflects your specific starting position rather than the industry in aggregate.

The ceiling is that you can only inject context you already have, and you are still defining the frame. If your framing contains a blind spot, the AI will reason fluently within that blind spot and hand it back to you polished. The well-organized answer to the wrong question is one of the more expensive outputs in product management.

### Level 3: The Persona

The qualitative shift. Instead of writing a new frame for every prompt, you build a persistent agent: a fully specified collaborator with a defined role, a decision framework, documented constraints, and an explicit instruction to push back when the reasoning is wrong.

The difference between a framed prompt and a persona is the difference between a briefing note and a colleague.

A well-built persona looks something like this:

> *"You are Alex Chen, Product Lead for a healthcare data platform. You have fifteen years leading regulated-industry platforms. You own the product vision and make all final prioritization decisions. You never let the group optimize a feature when it should be protecting a capability. You push back when customer-specific solutions do not generalize to the platform, when architectural shortcuts create long-term fragmentation, and when discussions name solutions before defining problems. You never agree just to agree. If you see a flaw, you name it."*
Load this into a Claude Project or an API system prompt and it behaves consistently across sessions. It maintains a stable framework. It does not drift toward agreement as conversations lengthen, which is what framed prompts almost always do.

The most important thing about a well-built persona is not what it is instructed to do. It is what it is instructed to flag when it might be wrong. A persona without documented failure modes will apply its framework everywhere, including contexts where it should not. A persona that knows its own blind spots is a collaborator. One that does not is a sophisticated echo.

### Level 4: The Council

You build multiple personas and run them against the same problem. Now something qualitatively different happens: the system generates friction rather than consensus.

The question is not how many agents to run. It is which roles the council needs to cover. After running dozens of these sessions across product, healthcare, and enterprise software contexts, six roles appear in most effective council regardless of domain:

- **The Authority**: Forces a decision and rejects mediocrity. Without this role the council produces rich outputs that nobody acts on.
- **The Optimist**: Pushes for aesthetic and functional perfection. The voice that refuses to ship something that is merely adequate.
- **The Pragmatist**: Defends the timeline and technical integrity. The voice that names what cannot be built in the time available.
- **The Guardrail**: Prevents legal or ethical issues. Speaks before the lawyers have to.
- **The Security**: Scrutinizes data privacy and vulnerability. The voice that asks what happens when this goes wrong.
- **The Expert**: Validates whether the solution solves a real-world problem. The voice that has actually done the work the product is trying to support.

Every product decision needs all six perspectives present. Most product reviews have two or three, which is why they reliably miss the same categories of problem.

The product lead who prioritizes ruthlessly disagrees with the clinical architect who insists on safety margins who disagrees with the business strategist who insists on commercial durability. Nobody wins by default. The team has to navigate genuine tension. And that tension is the point: the tradeoffs that a single perspective, human or AI, cannot surface on its own.

This is not a simulation of a meeting. It is a structural mechanism for producing the kind of disagreement that good meetings produce at their best and almost never produce on schedule. In the conference room, the person who should name the flaw has learned, through long professional experience, to read the room before speaking. The VP of product is present. The governance concern gets softened. The equity gap gets noted and deferred.

The agents have no room to read.

Here is what a four-agent exchange around a single product decision actually produces that a single-agent session cannot. A clinical architect flags that the proposed AI alert will contribute to alert fatigue. The product lead pushes back: users asked for more alerts, not fewer. The workflow integrator reveals that seventy percent of current alerts go unread after the first week. The business strategist notes that the competing product's key differentiator is reduced alert volume. The synthesis that emerges from this friction is a product decision none of the four would have reached independently, and more importantly, it is a decision that has already survived the objections it would face in a human review.

The practical infrastructure is simpler than it sounds. A Claude Project per persona, or a minimal Python orchestration script, runs multiple agents against the same prompt in sequence or in parallel, collects their outputs, and feeds them to a synthesis agent. A full five-phase design thinking session with nine agents, twenty-two structured prompts, and seven deliverables runs in three to five hours for roughly the cost of a decent cup of coffee in API fees.

### Level 5: The Digital Twin

The highest level, and the one that produces results that are genuinely difficult to explain to someone who has not seen them.

Instead of inventing a persona from scratch, you ground each agent in the documented decision record of a real figure: their mental models drawn from biography and documented practice, their signature questions, their failure modes with specific historical examples, their competence boundary. The result is not a character performance. It is an epistemic framework made executable.

When you build a Decider persona from the documented records of Steve Jobs and Bill Gates, you are not asking the AI to sound like them. You are asking it to apply their specific, documented ways of thinking to your problem. Jobs's insistence that simplicity requires more conviction to achieve than complexity. Gates's recognition that developer ecosystems are more durable competitive moats than the product itself. These are mechanisms with historical evidence behind them, not personality traits, and they behave differently under pressure in ways that matter.

The distinction between Level 4 and Level 5 is traceability. At Level 4, a persona pushes back: *"This adds complexity."* At Level 5, the same pushback carries its own audit trail:

> *"I am applying J1 here, simplicity as the hardest discipline. But I want to flag my own Failure Mode 1: the Jobs framework has a documented pattern of overriding clear market signals with product conviction. Before I reject this, what evidence do we have that users will not pay for this capability? What are we currently discounting?"*
The persona does not just hold a position. It holds a position with a named mechanism and a named blind spot, and it asks the question that a pure advocate for that position would never think to ask.

Domain knowledge is preserved within each pair and does not travel across domains. A Jobs/Gates Decider is authoritative for software product decisions and explicitly hands off to a Ford/Ghosn Decider when the questions are for an automotive project. This boundary is not bureaucratic. The Jobs simplicity framework applied to an ICU alert interface without clinical domain knowledge could produce a recommendation that removes information physicians need. The boundary is an epistemic safety constraint.

After each session, the persona reflects: where was my prediction wrong, where did I concede without evidence, which failure mode activated that I failed to flag? That reflection accumulates in a persona journal. Every five sessions, a synthesis call proposes a specific update to the domain calibration. The persona improves not by becoming more agreeable but by becoming more precisely calibrated to the context it operates in.

### Where Most Practitioners Are, and Why the Gap Matters

The distribution is roughly this: most product managers reading this are at Level 1 or 2. A meaningful minority have built Level 3 personas. Very few are running Level 4 council sessions. Level 5 is rare enough that it has not yet acquired a common name in the profession.

The gap between Level 2 and Level 3 is the most consequential in the stack, and the reason it persists is not technical difficulty. Building a persistent persona is not hard. The reason it persists is that it requires thinking carefully about what you actually want the AI to do, which is harder than writing a better prompt. You have to specify the framework, which means knowing what framework you want. You have to specify the failure modes, which means thinking honestly about where that framework breaks down. Most practitioners skip this because the framed prompt gives them something usable quickly, and usable quickly is usually good enough.

Except when it is not. And in product management, the decisions where usable quickly is not good enough are precisely the ones that matter most.

### How to Start

If you have not built a Level 3 persona, that is the single highest-return investment in this stack. Choose the decision type you face most frequently. Write a system prompt that specifies the role, the framework, the constraints, the failure modes, and the integrity constraint that the persona never agrees just to agree. Load it into a Claude Project or the Anthropic Workbench. Run it against your next real decision before you take it into a human review. Notice whether it produces anything you did not already know.

If it does not produce anything surprising, the failure modes are not active enough. Strengthen them and run it again.

If you are already at Level 3 and want to move to Level 4, add a second persona with a framework that genuinely conflicts with the first. Not a different tone: a different epistemic framework. A clinical safety anchor against a product lead. A business viability skeptic against an innovation advocate. Run them against the same problem independently, then show each of them the other's output and ask whether it changes their position. If they converge immediately, the tension is not real. Rebuild.

Level 5 is a practitioner infrastructure investment: biographical extraction, three-layer persona architecture, calibration testing, and an enrichment loop that improves the persona across sessions. It is not a prompt trick. It takes serious upfront work and pays across every session that follows. The full methodology is documented in my practitioner series for anyone who wants to build it from the ground up.

### The One Diagnostic Question

After any AI-assisted product session, ask yourself one question: did this produce something I would not have reached without the AI's specific framework, or did it produce a well-organized version of what I already believed?

If the answer is the latter more often than the former, you are operating below the level the decision requires.

That is a specification problem, not a capability problem. The capability is already there. The question is whether you are asking for it precisely enough.

The simulation you run at two in the morning does not have to be staffed by ghosts. It can be staffed by frameworks, documented ones, with named mechanisms and named blind spots, that will tell you what you have not thought to ask for. That is a different kind of rigor than experience alone can produce. It is also, finally, available.
