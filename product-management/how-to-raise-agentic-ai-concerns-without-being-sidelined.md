# How to Raise Agentic AI Concerns Without Being Sidelined

**Why raising agentic AI concerns gets the PM sidelined, and four concrete moves that change what the room is looking at.**

Every PM in this cycle has seen a version of the same pattern. The agent works on stage. The pilot stalls in production. And the person who flagged the risk first, weeks before the stall, is now tagged as "not bought in."

This is not a values problem. It is a delivery problem. The concern is usually correct. The delivery puts the PM on the wrong side of the room.

What separates the PMs whose concerns get absorbed from the PMs whose concerns get routed around is not sharper intuition. It is four concrete moves. Each one trades a gut-feeling objection for something the team can inspect, track, or measure.

None of this is theory invented for this piece. Most of it is in work I have been developing across this year's Agentic Experience Design writing. This is the version for PMs who need it Monday morning.

## The trap: why dissent fails in this cycle

The CEO mandate is real. Boards want an agent count. Demos close cycles. In that environment, a PM who raises architectural or governance concerns in open meetings is not perceived as rigorous. They are perceived as slow.

The conventional advice, "speak up early, escalate your concerns, bring data," assumes a room that is calibrated to receive the data. From where I sit, that room does not exist right now. The room is calibrated to ship.

So the move is not to argue harder. The move is to change what the room is looking at.

## Move 1: Build the artifact, not the argument

The most reliable way to shift a room is to put a document on the table that the room now has to respond to.

For agentic systems, the useful documents are not slide decks. They are four runtime artifacts I have argued every agentic product needs before release:

- **The autonomy boundary**: what the agent is allowed to decide without a human.
- **The approval moment**: where a human is required to intervene.
- **The audit surface**: what the agent's reasoning looks like to a reviewer after the fact.
- **The recovery workflow**: how the team undoes a wrong action.

Three things happen when you table these four documents, even half-drafted.

Engineering starts answering them, because they read as specification, not objection. Security and compliance attach to them, because the language matches their intake forms. And the "not bought in" framing collapses, because the PM is not asking for a pause. The PM is doing the work the launch requires.

A recent human-factors study of users on a production AI writing assistant documented how quickly users bypassed the agent's intended workflow when the approval moment was poorly designed. The failure was not the model. The failure was that no one had drawn the control surface. The artifact would have caught it.

Artifacts are not agreement. They are forced specificity. Use that.

## Move 2: Translate the concern into CEO math

The CEO is not asking a technical question. They are asking a capital-allocation question. If your concern does not land as a number, it does not land.

The durable frame is unit economics. Agentic systems have a cost structure that looks nothing like traditional software. A production enterprise agentic deployment typically enters at six figures in first-year cost before counting the human review time, the failed-transaction rework, or the coordination overhead between agents. Public work on multi-agent systems suggests a meaningful share of tokens goes to coordination rather than to the user-facing task.

The reference point every CEO already knows is Klarna. Klarna went further on agentic customer service than almost anyone. They publicly rebalanced back toward human agents in 2025 after their CEO acknowledged that the AI-heavy approach had not met quality expectations in key segments. The lesson is not "agents failed." The lesson is "agent count stopped being the right metric." When the company that went furthest pulled back, the unit-economics question became the adult question in the room.

Reframed for your room: not "this agent is risky," which the room hears as slow. Instead: "our per-successful-task cost is X, our per-handoff cost is Y, and those curves cross at volume Z. Below Z, this is a negative contribution feature." That is the sentence the CFO quotes back to the CEO. That is the sentence that moves.

The PM who brings the cost curve changes the conversation without once saying "slow down."

## Move 3: Replace "when does it ship" with "what's our rollback time"

Every agentic AI program is tracking a version of the same question: when does it ship. That question selects for one behavior, launching. It does not select for landing.

The question that changes the room is: "what is our rollback time when this agent takes a wrong action in production."

That single substitution forces the team to name the observation layer. Six instruments matter: task success rate, unintended action rate, override frequency, confidence calibration, rollback time, and incident recovery time. If the team cannot answer any of those, the team is not ready for production, and the gap becomes visible without anyone raising their voice.

Public incidents illustrate the point. New York City's MyCity chatbot, launched in late 2023 to help small business owners, was found by investigative reporting to give legally incorrect advice on core employment and tenant-rights questions, and it remained live after the flaws were publicly exposed, highlighting the difficulty of rapidly correcting or containing incorrect outputs once an agent is deployed. In 2024, McDonald's ended its multi-year AI drive-thru pilot with IBM after accuracy and operational challenges became visible in real-world use.

In both cases, the primary failure was not the model. It was the absence of a specified control surface and a fast-enough rollback. That is the category of failure every PM raising concerns today is actually flagging, whether they name it or not.

"When does it ship" optimizes for launch. "What's our rollback time" optimizes for survival. The PM who asks the second question is not a brake. They are doing the work.

## Move 4: Use governance as a procurement filter, not a pitch

Internal governance conversations rarely move a shipping team. External ones do.

In the regulated-sector procurement activity I am adjacent to, the direction is consistent: buyers are rewriting AI addendums to ask concrete questions about audit surface, rollback SLA, human-review architecture, and incident disclosure. Health systems, banks, and regulated manufacturers are noticeably further ahead on this than the rest of the enterprise market. The EU AI Act attaches legal obligation to several of these categories for high-risk systems, including medical-device AI, hiring decisions, and credit scoring.

The move is to bring the buyer's questionnaire into the room. "Here are the questions our next enterprise customer is going to put into the contract. Here is what we currently have an answer for. Here is what we do not." The team is no longer debating whether governance is a brake. They are looking at a customer requirement the product cannot close without.

Governance as a committee document is a tax. Governance as a revenue filter is a moat. Present it as the second thing, not the first.

## The question the room actually wants answered

Strip the politics away and every room shipping agentic AI right now is quietly asking one question: "when this fails in public, what happens to us."

That question is not cynical. It is the correct question. It is also the only question that aligns the CEO, the CFO, the head of engineering, the head of legal, and the PM.

A PM who answers that question, with artifacts, with unit economics, with the rollback-time metric, and with the buyer's questionnaire, is not the skeptic in the room. They are the person the room turns to when the press release breaks.

You do not need to slow the launch down. You need to make the launch answerable.

---

*This piece is part of the Product Management and Enterprise AI series, and extends the Agentic Experience Design work on autonomy boundary, approval moment, audit surface, and recovery workflow into the internal operating problem most PMs actually face: shipping responsibly in a room that is calibrated to ship fast.*

## Sources

1. Human-factors research on production AI writing assistants, recent CHI-community studies (user workflow bypass patterns when approval moments are poorly designed)
2. NYC MyCity small-business chatbot, investigative reporting by The Markup, March 2024 (legally incorrect advice; chatbot remained live after flaws were publicly exposed)
3. McDonald's AI drive-thru pilot with IBM, ended June 2024 after 100+ store rollout, following accuracy and operational challenges in real-world use
4. Klarna AI customer-service rebalancing, CEO public statements and investor communications, 2024 to 2025
5. EU AI Act, Regulation (EU) 2024/1689, high-risk system provisions (medical-device AI, hiring, credit scoring)
6. Agentic Experience Design series, Yoram Friedman, 2026 (four runtime design artifacts, six observation instruments)

---

*Yoram Friedman, MD is a physician and senior product manager at SAP Business Data Cloud. He holds three Harvard Medical School executive education certificates in healthcare digital transformation and AI.*
