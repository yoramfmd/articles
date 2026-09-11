---
title: The User Did Not Leave. She Split in Two.
slug: the-user-did-not-leave-she-split-in-two
published: 2026-08-10
excerpt: The operator did not vanish when the agent arrived. She split. What she knew became the agent's context and bounds. What she checked before committing became the supervisory surface. The only casualty was the dashboard, and most agents are being built to generate it.
url: https://data-decisions-and-clinics.com/the-user-did-not-leave-she-split-in-two/
tags: Product Management
source: ghost-api-pull-2026-08-16
---

I commissioned a picture last week for a session I am giving, and the brief took me three tries to get right.

I wanted a warehouse operations manager at her desk, in front of a screen showing the whole site. Inbound and outbound by dock door, stock by bin, the labor plan, a forecast band widening into next week. Behind the screen, drawn faint like a memory, everything that had to exist for that screen to be correct: the data center, the systems of record, the sensors and orders and invoices, the measures, the aggregations, the definitions of what counts as late. And behind her, drawn at exactly the same faintness, everything that had to exist for her to read it: the certification, the onboarding, the year she learned which supplier always ships early at quarter close.

The picture is a mirror. I am going to put it in front of a room full of people who believe their agent is replacing that dashboard.

It is not. It is replacing her.

Somebody will read that as a sentence about headcount. It is not one. She may well still be employed, and in most deployments I have watched she is. What gets taken over is her loop: the watching, the triage, the routine call. The line is about where the work went rather than who is on the payroll, and it matters because that loop was carrying things nobody had written down.

### What she was actually doing

Ask her what she does and she will say she watches the dashboard. That is not what she does.

The dashboard shows her that a pick failed twice on the same bin. She is the one who knows that a second failure on the same bin means the count is wrong, not the picker. The dashboard shows her a short shipment. She is the one who knows that under a certain value it gets received and reconciled later rather than held, and that the note explaining it has to be written a particular way because it will be read in an audit two years from now.

None of that was on the screen. The screen was a tool, and a tool makes a competent person faster. It never made anyone competent.

So when a team tells me they are building an agent to replace the dashboard, they have described the one part of the arrangement that was never doing the difficult work.

### Both channels are her estate

Here is the part I had wrong until recently, and it changes what you build.

I had been describing this as a person leaving and a gap opening behind her. That is too simple. She does not leave. She divides, and both halves land somewhere in the product.

Some of what she knew goes into the agent. The threshold with a number on it, the condition that means stop, the record that has to survive the case, the supplier who is not actually late. That is context, bounds and policy, and it is the first channel.

Some of it does not go anywhere. A good share of what she carried is tacit: recognizing that a pattern is off before she can say which number is wrong, knowing when the written policy is the wrong answer for this case. You can write down the rule. You cannot write down the recognition, and pretending the decomposition is complete is how a brief passes review with the hardest third of the job missing from it.

What she did when she looked up goes somewhere else. The moment she paused, the thing she checked before committing, the case she handed to someone senior. That becomes the supervisory surface, built for her occasional return rather than for her shift. That is the second channel.

Two channels, one estate. Everything in both of them was hers.

Which means the honest version of the sentence I have been using is not that an agentic solution is a product plus a supervisory system bolted on. It is that you are building two products out of one person, and neither of them is the screen she was looking at.

### The thing that actually dies

The casualty is narrower than the word dashboard suggests, and the loose version of the claim is wrong. What dies is not dashboards. It is the assumption that the person doing this work needs a broad, continuous surface in front of her to make every routine call. That surface had one reader, and it is a strange kind of death, because almost nothing about it is missed.

The infrastructure survives. The agent draws on the same semantic layer she did, and it needs that layer defined more rigorously rather than less, because it has no eye to catch a number that looks wrong on sight. The measures, the aggregations, the definitions, the lineage: all of it matters more than it did.

It also has to do something it was never asked to do. That layer was built to be read. It is now being acted on, which adds obligations nobody put in the original design: how fresh a number must be before an action can rest on it, what the agent may change rather than see, and what happens when two sources disagree and no person is there to notice. Correct was enough for a reader. It is not enough for an actor.

What dies is the rendering step. Decades of work went into turning a correct number into a picture a human could read at a glance, and the glance is what left the room.

The left half of my picture is not being replaced. It is being re-pointed.

And this is where I part company with most of what I am seeing built. A striking number of the agentic projects crossing my desk are pointed at generating reports and dashboards. Not consuming them. Generating them. Which is effort spent automating the production of an artifact whose reader was removed by the same project. That is what I happen to see rather than a survey, so take it as a pattern to check rather than a finding.

The check takes one minute. Name the output your agent produces, name the person who reads it, and ask whether that person is the one whose job the agent took.

### Four surfaces, and three are new

The confusion is worth untangling, because the word dashboard is now doing four different jobs.

There is the work surface, which is the one that died. Continuous and broad, covering the whole state space, because a person scanning it did not know in advance where the problem would be.

There is the supervisory surface, for whoever now arrives when the agent hands over. Not continuous and not broad. A few moments, each of them load-bearing, each answerable inside the time the workflow actually allows.

There is the agent observability surface, which is about the agent rather than about the warehouse. Task success, override frequency, how often a human reverses it, how long a rollback takes. Its reader is the product manager, not the operator.

And there is a fourth that I think is the most interesting thing in this whole argument. Call it the ad-hoc dashboard. It does not exist until the agent stops. It is generated at a single approval moment to show the supervisor what the agent was reasoning over on that specific case. It is the exact inverse of the surface that died: the work dashboard was broad because a scanning person did not know where the problem was, and this one is narrow and deep because the agent already knows why it stopped.

Teams build the first and call it the second or the fourth. It fails as both, and not because it is too small. It is too big, and shaped for a kind of attention nobody is paying anymore.

### Where the ad-hoc version goes wrong

Three ways, and all three are cheap to prevent.

If the agent chooses what to show, it is assembling an argument for its own recommendation and the supervisor is reviewing a case prepared by the party under review. The old dashboard was neutral by accident, because somebody else built it in advance for no particular decision. So the content should be ad-hoc and the shape should not. Specify the slots once per approval type, and let the agent fill them.

It has to show what the agent could not see. A surface built only from the reasoning trace confirms the agent's own frame, and catching what sits outside that frame is the entire reason a person is still in the loop.

And the surface is disposable while the record is not, which is a distinction I got wrong the first time I wrote this down. The screen can vanish the moment the case closes. What has to persist is a snapshot of what was shown: the evidence, the sources behind it, the policy version in force, the agent's recommendation and how sure it was, what else it considered, and what the human then did. Six months later the question is never what the agent decided. It is what the approver was looking at when they approved it, and re-rendering from today's data reconstructs a different picture than the one that person actually saw.

One more rule, because fluency is the failure mode here as everywhere else. The recommendation has to sit visually apart from the evidence. A conclusion laid out in the same typeface as the facts reads as one more fact, and the supervisor ends up ratifying a summary rather than judging a case.

### The part I cannot resolve

There is a version of this argument that goes too far, and I want to mark it before someone else does.

Not every reader left the room. Her manager did not leave. Finance did not leave, planning did not leave, the auditor did not leave. Those dashboards survive on their own merits and none of this touches them. The claim is narrower than it sounds: the dashboard built for the person the agent replaced has lost its reader. Every other surface in the landscape is a separate question and mostly fine.

I also cannot tell you where the supervisor's competence comes from once the shift work that built it is gone. She learned which supplier ships early by watching shipments for a year. The agent now watches the shipments.

One industry has an answer and it is not ours. Aviation requires pilots to demonstrate, on a schedule, that they can still fly the aircraft without the automation, and it requires it whether or not anything has gone wrong. Nothing equivalent exists in medicine, in software, or in operations. So the part of her that could not be encoded has no mechanism keeping it alive in the next person, and the same project that took over her loop is the one that removed the practice that built it. I do not have a fix. I have stopped believing it is somebody else's problem.

### What the picture is for

I asked for the two faint layers behind her to be drawn at exactly the same density, and I kept sending it back until they were.

That is the whole argument. The left side is what your vendor sold you and what your roadmap covers. The right side took a decade, cost real money, and appears in no architecture diagram anywhere.

She is facing the screen. Both histories are behind her, and she cannot see either one. Neither can the team that is about to remove her.

---

*Drawn from my Agentic AI for Product Leaders series, principally the whitepapers on the departed user, on prototyping the judgment, and on designing for the supervising user. The warehouse manager and her thresholds are an illustrative composite. The claim about what most agentic projects are currently pointed at is my own observation from the work in front of me, not a measured finding.*

[https://agenticaiproductmanagement.com/](https://agenticaiproductmanagement.com/)
