---
title: "Your Engineers Are Writing the Policy Now"
slug: your-engineers-are-writing-the-policy-now
published_at: 2026-07-21
custom_excerpt: "Engineering changed its unit of work to intent, policy, and boundaries. Product and design mostly still ship user stories and screens. So the policy gets written by the last person to touch the ticket, in a prompt, at midnight. The control plane has inputs, and nobody upstream owns them."
tags: [pm]
feature_image: https://storage.ghost.io/c/e6/05/e605b234-3cc8-4fe4-97bb-2bb55b18b8fb/content/images/2026/07/ChatGPT-Image-Jul-21--2026--02_57_09-PM.png
source: ghost
---

# Your Engineers Are Writing the Policy Now

# 

It is late, and an engineer is turning a goal into an agent. The ticket she was handed reads the way tickets have read for twenty years. As a support agent, I want to see the customer's complaint history so I can resolve the complaint fairly.

She is not building a screen for a support agent. She is building the thing that resolves the complaint. So she opens the model and writes the parts the ticket never mentioned. What the compensation limit is. Which records the agent may change and which it may only read. When a payment needs a human signature. What has to be kept as proof once the case closes. None of it was in the story, because the story described a person who would have known it. She is not writing code. She is writing policy.

The system she is building has to be told, before it runs, by someone. Tonight that someone is her.

Jesper Lowgren wrote the sharpest account of the runtime half of this problem that I have read, and if you build agentic systems you should read it. His argument is that when we let an agent work from a goal instead of a sequence, the path does not disappear. Part of it moves into runtime, and it takes a surprising amount of governance with it, the kind that used to be baked into the process itself: which actions were available, when they could happen, where a human was expected. A prompt cannot carry that. Policy changes, authority varies by role and value and time, and evidence has to be captured independently of whatever the model says it did. So you govern the space the agent operates in rather than the path it takes. His title names it the control plane, and he is right. Architecture has to run now, not just describe.

I want to take the part he left upstream.

## The control plane has inputs

A control plane governs action against a set of declared conditions. Intent, so a real outcome can be told apart from plausible activity. Authority, so every consequential action traces to a mandate. Policy that binds at the moment the decision is made. Scope and risk. Stable meanings for the business terms. Evidence.

Read that list again as a product manager rather than an architect. Every item on it is a decision. Someone decides what the outcome is and how you know it was reached. Someone decides how much the agent may spend before a human has to sign. Someone decides which evidence is admissible and which version of the policy applies. The control plane does not invent those conditions. It enforces them. They have to arrive from somewhere.

For most of that history they arrived implicitly. The process carried them, and the human in the seat supplied the rest at runtime. The user story never had to state the compensation limit, because a person who knew the limit was going to read the screen and decide. The judgment lived in the human, and the human was in the loop by default.

Take the human out of the loop and the judgment has to exist in writing before the agent runs. That is the whole shift, and it lands on the deliverable.

## The deliverable that did not change

Engineering is already crossing over. Spec-driven development, the outcome spec, the eval, the boundary, the escalation rule. The unit of work for a team building an agent is no longer a sequence of steps. It is a statement of intent and the limits around it. Watch a strong team in Claude Code or Codex and you will see them writing outcomes and constraints, not procedures.

Product and design mostly have not. The product manager still writes a user story. The designer still hands over screens. Both describe what a human would do, in a product where a human increasingly does not do it. The story reaches the engineer carrying none of the conditions the control plane needs, and the engineer, the one turning it into a system that runs, supplies them. Intent, policy, risk, and evidence, decided in a prompt by the one role that was never meant to own them.

That is the collaboration gap, and it is not a tooling problem. Every team has tools. The gap is that the deliverables each role hands the next were built for a world where the human supplied the missing judgment at runtime, and that world is closing. Everyone is moving at once, which hides it. The developers are burning tokens, product and design are auditing which tools they are allowed to open. Some teams point AI at building deterministic workflows while others plan agentic products with the old planning methods, and both call it the same initiative. Somewhere in the middle a spec is supposed to pass cleanly between them, and it does not, because the thing being passed still describes a user instead of an agent.

Medicine solved a version of this a long time ago. The person with the judgment cannot stand at every bedside at every moment, so the judgment is not handed over as a description of what the attending would do. It is handed over as an order set and a protocol: the parameters, the thresholds, when to escalate, what to document. The nurse acts inside a boundary that was declared in advance by the person who holds the authority, not narrated as a task after the fact. An agent needs exactly that, and it needs the roles who hold the judgment to be the ones who write it down.

## What each role now owes the next

The fix is not a new ceremony. It is a change in what each deliverable carries, so the team downstream can build on it instead of reverse-engineering it.

The product manager owns the outcome and its boundary, not the click path: what counts as resolved, what the agent may decide alone, where the money stops, what must never happen. The designer owns the approval moment and the re-entry point, where the human comes back into the loop, what they see when they do, and whether the workflow makes supervision real or only theoretically available. The domain expert owns the policy and the admissible evidence. They hold a veto, because the person who has carried the compensation rules in their head for fifteen years is the one who can say which version applies. The architect owns scope: which boundary is a prompt the agent can be talked out of, and which is a wall it cannot cross.

Those are not four documents. They assemble into one. My third book, The Agentic AI Team, calls it the Executable Brief: the build document the engineering team works against, derived from the decision the room already made, with intent, boundary, policy, and evidence stated, versioned, and testable instead of implied. The user story becomes an input to it, not a substitute for it.

Someone will say engineers have always filled gaps in the spec, and that is true, and for years it was fine. The gap used to be a UI detail or an edge case, and an engineer closing it cost a bug ticket. The gap now is who may authorize a payment and what proof shows the case was handled lawfully. The cost of an underspecified deliverable moved from a defect to a consequence someone absorbs. A blank an engineer could reasonably fill has become a decision that requires the authority to make it.

## The question upstream of Jesper's question

Jesper ends where the runtime has to answer: if the agent took an action nobody explicitly designed, on what grounds was it permitted.

The team has to answer a question that sits upstream of that one. Who was supposed to write the grounds down, and what did they hand the engineer instead. If the answer is a user story and a set of screens, then the grounds were written at midnight by the person least positioned to own them, and no control plane, however well built, can enforce a policy that nobody upstream ever decided.

Your agents are getting better. Jesper asked whether your architecture is getting stronger. The prior question, the one at the place where technology meets people, is whether every role on your team is still shipping a deliverable built for a user who has already left the room.


---

*This article is part of an ongoing series on AI product design, healthcare data, and the human side of technology adoption.*

*It builds on Jesper Lowgren's "The prompt is not the system. The control plane is." (LinkedIn, July 2026). The Executable Brief and the seat-by-seat ownership model are developed in my third book, The Agentic AI Team.*
