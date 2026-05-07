# You Built the Agent. Nobody Designed the Experience.

*Series: Agentic Experience Design, Article 1*

---

For most of enterprise software history, the design question was clean: help a human find the right information and act on it.

The dashboard surfaced the signal. A good navigation pattern reduced the distance between data and decision. Years of usability research measured whether users could find what they needed. A/B tests optimized the path. Branding and design systems gave the surface consistency. The design artifact was the screen. The human was the actor. The system was the stage.

Classic AI shifted the dynamic slightly, but not structurally. The recommendation engine surfaced not just data but a proposed decision: this patient is at sepsis risk, this order is likely to churn, this route saves fourteen minutes. The human still decided. The human still acted. The design question expanded, barely: how do you display confidence? How do you communicate uncertainty without undermining adoption?

Then agentic AI arrived, and the contract broke.

An agentic system does not surface information and wait. It acts. Once software begins acting in the world on your behalf (booking meetings, sending drafts, canceling orders, escalating tickets), the problem is no longer display. It is supervision, permission, recovery, and control.

Designing agentic systems is like teaching a class of toddlers to behave. You set the rules. You arrange the room. You staff the supervision. But you cannot test every possible sequence of moves, because the agent is capable in ways you cannot fully enumerate and unreliable in ways you cannot fully predict. The design challenge is behavioral, not visual. You are not designing what the user sees. You are designing what the agent does, when it asks permission, what trace it leaves, and what happens when it gets something wrong.

---

## Start With the Mental Model

Before you design any aspect of an agentic experience, you have to answer a prior question: what kind of system is this?

A suggestion engine surfaces options and waits. A copilot acts on explicit instructions, step by step. An autonomous actor executes sequences of decisions without further approval. Many teams treat these as points on a continuum and leave the distinction implicit. That is where the mental model breaks: users who cannot tell which system they are operating will develop the wrong one, and a wrong mental model drives both overtrust and abandonment in equal measure. The expectation has to be set before the first interaction, not discovered through failure.

---

## Four Things Every Agentic Experience Requires at Runtime

Every agentic product involves four design decisions at the moment of action, whether the team makes them deliberately or not. Most teams make them by default, and default, for a system that acts on your behalf, is rarely deliberate enough.

The first is the autonomy boundary. Before the agent acts, something defines what it may do unilaterally and what requires a human decision. In most current deployments, this boundary is invisible to the user. They discover it by hitting it, or after the agent has already crossed it. The design requirement is to make the boundary legible, at the moment it matters, in terms the user can act on.

The second is the approval moment. When the boundary is approached, the handoff between agent decision and human judgment has to be designed. Not a confirmation dialog. Not "are you sure?" A well-designed approval moment gives the user what the agent knows, what it is uncertain about, what the consequences of proceeding look like, and what the alternatives are. It is a decision package, not a speed bump.

The third is the audit surface. After the agent acts, the user needs legibility. Not a model explanation. Research is clear that chain-of-thought reasoning is frequently unfaithful, meaning what the model says it did and what it actually did are not reliably the same. What the user needs is a decision trajectory: the sequence of observable actions and retrieved context that produced the outcome. And in enterprise settings, that trace must carry something additional: whose authority was delegated, under what policy, and who carries the outcome. "The agent did it" is not a defensible audit trail.

The fourth is the recovery workflow. When the agent is wrong, the experience must provide a path forward. An error message is not a recovery workflow. A path forward means a compensating action, a rollback option, or at minimum a clear accounting of what cannot be undone and why. Critically, the recovery affordance must be reachable mid-execution, not only after the agent has finished. Interrupting the agent while it is working should be as easy to design as starting it. Most teams treat override as an edge case; it is a primary interaction.

---

## What the ICU Figured Out Forty Years Ago

I spent time as a resident in a cardiac ICU. The design problem I am describing is not new. Clinical monitoring is the human-factors precedent for agentic design, and it has been generating evidence for decades.

The data is sobering. Eighty-five percent of ICU nurses report being overwhelmed by clinical alarms. Sixty percent of alarms go unresponded to. The Joint Commission issued a sentinel event alert on alarm fatigue. The Agency for Healthcare Research and Quality conducted a systematic evidence review. None of this happened because the alarms were wrong. It happened because the systems were designed with no model for the cost of interruption. Every threshold exceedance triggered a notification, with no calculation of what the nurse was currently doing, how urgent this particular alarm was relative to the previous twelve, or what the consequence of one more interruption would be.

Eric Horvitz, a physician and computer scientist who is now Microsoft's Chief Scientific Officer, formalized the correct model in 1999: whether to alert a human should balance the cost of interrupting now against the cost of waiting. That is a design parameter, not an instinct. Enterprise agentic AI teams are currently making this decision by instinct, one notification at a time. The likely result is that the first wave of enterprise agents drowns users in approvals, confirmations, and status updates. Most teams will respond by reducing confirmation requirements to reduce friction. That is exactly the wrong direction. The answer is to design the interruption, not eliminate it.

---

## Irreversibility Is Not an Edge Case

What makes agentic AI qualitatively different from automation is consequence compounding. A batch job runs the same operation on a defined dataset. An agent takes actions whose downstream effects are not fully predictable at the time of execution. Canceling a meeting, placing a procurement order, sending a customer communication, updating a record: these are not reversible in the way a screen state is reversible.

The design requirement: classify actions by consequence before they execute, not after. The Federal Aviation Administration uses a consequence taxonomy for aviation system design (minor, major, hazardous, catastrophic) that serves as a useful design analogy for enterprise agentic systems. A minor-consequence action can proceed with a brief plain-language summary of what the agent intends to do. A high-consequence action requires a mandatory pause, an alternatives presentation, and a structured approval. When the agent cannot complete a step, it should not fail silently or halt without explanation. The designed fallback is to surface the incomplete state, state what it cannot do and why, and hand control back to the human with enough context to continue. Silence is not a fallback mode. The consequence ladder is a decision tree. It requires only that teams build it before they ship.

Gmail's Undo Send is the template for post-action reversal: a brief window during which the system appears to have acted but has not yet committed. This is not a technical trick. It is a design philosophy: treat irreversibility as a constraint to design around, not a fact to accept after something goes wrong.

---

## You Are Not Building Trust. You Are Calibrating It.

Most enterprise teams measure trust acquisition: adoption rates, task completion, retention. The research says the goal is wrong.

The correct target is appropriate reliance: users who rely on the agent when it is reliable and who override it when it is not. Overreliance and underreliance are symmetric failure modes. The user who trusts an agent that is wrong and the user who ignores an agent that is right are both costing the organization real value, in opposite directions. Research on algorithm aversion shows that users who observe a single visible failure over-correct to disuse: trust destruction from one bad outcome exceeds the cumulative trust gain from many correct ones. Failure recovery is not a support problem. It is an experience design problem.

An agent that is right ninety percent of the time and makes its confidence legible builds durable trust. An agent that presents every output with equal certainty builds fragile trust, the kind that collapses on the first failure it cannot explain. Confidence legibility is a design surface. Most teams are not designing it.

The metrics follow from the design: override rate tells you whether users trust the agent's autonomy boundary; rollback time tells you whether recovery is actually usable; unintended action rate tells you whether the approval moment is catching what it should; and incident recovery time tells you whether the organizational response is a real workflow or an improvised one. If you did not design the surface, you cannot measure it.

---

## Agentic Experience Design Is Lifecycle Design

Agentic experience design is not only what the user sees at the moment of action. It is the governance of the agent's behavior across its entire operational life.

That lifecycle begins before the agent reaches a user. At design time, who can configure the agent, what actions it is permitted to take, and which workflows it may never touch are policy decisions, not defaults. Least-privilege access, role-based permissions, and human sign-off requirements for high-risk configuration changes belong here, before any user touches the system.

At build time, the agent should be tested for adversarial inputs before it is deployed. Prompt injection, tool abuse, credential leakage, and permission escalation are not theoretical threats. They are documented attack vectors specific to systems that can reason and act, and they are largely absent from current enterprise AI security programs. Red-teaming an agentic system before launch is not optional; it is the equivalent of safety testing before a medical device reaches a patient.

At deployment, authorization should be explicit. Agentic systems often behave as if delegation were broader than the user originally intended, because the boundary between what was approved and what the agent inferred was approved is invisible. Making that boundary visible at deployment, and reviewable afterward, is a governance requirement, not a UX nicety.

At runtime, monitoring is not optional. Agent behavior drifts. External data sources change. Model updates, which model providers push on their own schedules, can quietly shift how an agent interprets its instructions without any deployment event on your side. A model version change is a behavioral change; it should be treated as a deployment requiring governance review, not a transparent infrastructure update.

At incident, recovery is organizational, not just transactional. When an agent misbehaves, the response includes freezing the agent, attributing the failure to the right pipeline segment, notifying affected users, and reauthorizing before resuming. That sequence is a product experience. Most teams have not designed it.

The full arc: setup, configuration, testing, deployment, runtime monitoring, escalation, incident response, and retirement. Each phase requires deliberate design decisions. Teams that treat only the runtime interaction as "the experience" are designing half a system.

---

## The Design Question That Was Always There

The ICU did not solve alarm fatigue. It is an ongoing, documented patient safety crisis. But the field named the problem, built the research base, and produced design guidance that took the challenge seriously. Enterprise agentic AI is young. The design problem it is solving is not. Clinical monitoring, aviation, and industrial supervision have been accumulating human-factors evidence on supervisory control for decades. The interruption cost model, the consequence taxonomy, the alarm fatigue data: none of this had to be invented. It was sitting in research that most enterprise product teams have never opened. The question is whether teams find it before they ship, or after they have to explain what went wrong.

Agentic experience design is a control surface discipline. At runtime, it covers supervision, approval, audit, and recovery. Across the lifecycle, it covers policy, permissioning, security, compliance, monitoring, and incident response. Every team building an agentic product is already making these decisions. The teams that make them deliberately build systems that earn trust incrementally and recover gracefully when they fail. The teams that don't build something that acts on your behalf in ways you did not fully authorize, cannot fully trace, and struggle to stop.

That is not a UX problem. It is a design problem. And it starts at the moment someone decides to let the agent act.

---

*This article is part of an ongoing series on AI product design, healthcare data, and the human side of technology adoption.*
