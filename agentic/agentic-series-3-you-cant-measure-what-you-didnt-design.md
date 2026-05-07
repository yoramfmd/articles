# You Can't Measure What You Didn't Design

*Series: Agentic Experience Design, Article 3*

---

The call came from a supplier. She had been receiving order notifications all week and wanted to confirm the delivery schedule. Someone on the procurement team pulled up the dashboard: 340 transactions, 100 percent completion, every entry marked confirmed.

She was still on the line.

Not one order had arrived. The agent had been confirming work it never did, for six months.

The completion metric was real. The work wasn't.

---

## The Phase Nobody Ships

There is a version of product lifecycle management that most PMs know in theory and almost none practice.

The traditional model was not a straight line. It was a loop. You discover a problem, define the solution, design and build, then launch. But launch was never supposed to be the last step. It was the checkpoint where the work shifted from building to learning. The observation phase followed: you watched the product in the wild, monitored what was actually happening, fixed what was broken, and collected the feedback that would seed the next release. Then the cycle started again.

The product lifecycle was designed as a closed loop. What happened over the past fifteen years is that one half of it quietly disappeared.

Agile culture accelerated the build cycle. MVP culture reframed speed as virtue. Continuous delivery made shipping feel like the unit of success. None of these were wrong in principle. But in practice, they compressed the loop by eliminating the back half. Ship fast. Celebrate the launch. Move to the next roadmap item. The observation phase became a retrospective bullet point, not a product phase.

Most enterprise product teams do not have a named, resourced, designed observation phase. They have a support queue, a NPS survey sent at 30 days, and a dashboard built for the launch presentation that nobody updated after week two.

---

## Why This Failure Gets Catastrophic With Agents

For a SaaS product, the cost of not monitoring is measured in missed opportunities. A feature nobody uses. A workflow with friction nobody reported. A drop in retention that took a quarter to diagnose. The tool sits and waits. It does nothing wrong while no one is watching.

Agents are fundamentally different. An agent that is not monitored does not sit and wait. It continues to act. Every day without a corrective loop is a day the agent operates according to its last known configuration, inside its last-understood autonomy boundary, guided by instructions that may no longer match what users actually intend.

A SaaS product with no observation phase is a product that stagnates. An agentic product with no observation phase is a product that compounds its errors autonomously, at scale, until a supplier calls.

---

## The Six Months

The six months between launch and the supplier's call were not a measurement gap. They were the predictable outcome of something more fundamental: trust building naturally, in the absence of a system designed to hold supervision stable.

In the first weeks after launch, the procurement team was paying close attention. Spot checks came back clean. Early results looked correct. A manager who had been approving every batch above a certain threshold stopped scheduling the weekly review, because three months of clean data made weekly reviews feel like unnecessary overhead. Someone adjusted the approval threshold upward because the agent had never made a mistake at the original level. None of these decisions were announced or logged. Each was a rational response to observed reliability, made by a reasonable person in the moment.

By month six, the autonomy level the team had actually granted the agent bore no resemblance to what was designed at launch. The agent was not running at the level that was authorized. It was running at the level the team had drifted into, through a series of small trust updates that were never made visible.

Aviation researchers identified this pattern fifty years ago and gave it a name: automation complacency. As a system's reliability increases, operator vigilance decreases. Not because operators become careless, but because sustained reliability is cognitively indistinguishable from reliability you should trust unconditionally. You cannot feel the difference between "I am appropriately confident in this system" and "I have stopped checking" without an external signal that tells you which state you are in.

Most people have experienced a consumer version of this progression. When Tesla introduced Autopilot, the intended experience was simple: activate the feature, keep your hands on the wheel, and let the system assist. That instruction held for exactly as long as the system felt unfamiliar. Then it performed well. The hands stayed on the wheel but the grip loosened. Then the hands came off because nothing bad happened. Then the eyes moved to a phone, because other things needed attention. Then, in documented cases, the driver was asleep. The destination was set. The system was steering. The gap between Level 2 assistance and full autonomy was bridged not by a design decision but by accumulated trust in the absence of a corrective signal.

In 2024, the NHTSA investigation reported 467 crashes involving Autopilot, resulting in 54 injuries and 14 deaths.

Tesla's regulatory and engineering response is instructive: hand-detection sensors, driver-facing cameras, periodic re-engagement prompts that force a response before the system continues. The company learned that "keep your hands on the wheel" was not a sustainable design constraint. The product had to hold the safety requirement, because the instruction alone would not hold it over time. The supervision level had to be maintained by the system, not delegated to the driver's self-discipline.

Enterprise agentic products are in the same position. An agent that performs well in early weeks trains its users to reduce supervision. Each small reduction feels rational. None is announced. The accumulated result is an agent operating at a level of autonomy that nobody authorized, inside an observation phase nobody maintained.

---

## What the Old Metrics Were Actually Measuring

The dashboard built for the launch presentation tracked the right things for the wrong product.

Daily active users measures whether users found the tool worth returning to. Session length measures whether the workflow held attention long enough to complete. Task completion rate measures whether the interaction was designed well enough for a human to reach the destination. These metrics presuppose a system where the human is the actor. The product surfaces information. The human decides. The human acts.

In an agentic system, the agent acts. The human delegates. The questions that matter are fundamentally different: did the agent do what the user actually intended, within the bounds they actually authorized, and when it got something wrong, could the user tell, could they stop it, and could they recover?

Those questions do not appear in a session-length chart.

---

## The Six Instruments of the Observation Phase

The metrics an agentic product requires map directly onto the four phases of the lifecycle loop most teams are not running: observe, monitor, fix, and feed back into the next release.

**Observe**

**1. Task success rate.** One of the most deceptive metrics on the list. Most teams track whether the agent completed the task. The correct version measures whether it completed the task the user actually intended. The procurement agent in this article's opening had a 100 percent completion rate and a 0 percent task success rate. There is a failure mode researchers call a background failure: the agent finishes, no error state registers, and the result is wrong.

**2. Unintended action rate.** The metric that surfaces background failures, but only if the autonomy boundary was designed to be legible and logged. Teams that did not design the boundary cannot measure whether it was crossed.

**Monitor**

**3. Override frequency.** The metric most teams misread. A high rate looks like a trust failure; sometimes it is. But a rate that is persistently too low, in a domain with genuine uncertainty, is equally worth investigating. It may mean users cannot override easily. It may mean they have stopped paying attention. It may mean they have decided, correctly or not, that the agent is reliable enough not to check. Three distinct product problems, three different responses. Tracked over time, override frequency is also the signal that shows supervision eroding before the agent drifts past its authorized boundary.

**4. Confidence calibration.** The monitor metric with the longest lead time and the sharpest failure consequence. A well-calibrated agent expresses high certainty on things it gets right and surfaces uncertainty on things it gets wrong. An overconfident agent builds fragile trust: adoption that holds until the first visible failure, then collapses faster than it was built. Calibration is not a model property you inherit from the vendor. It is a design surface you build around the model output.

**Fix**

**5. Rollback time.** This metric only exists if a recovery workflow was designed as a product surface. If the response to a consequential error is an email thread and a manual correction, rollback time is measured in days and logged nowhere. If a compensating workflow was built, staged, and accessible from launch, rollback time is measured in minutes and becomes a sprint target.

**6. Incident recovery time.** The organizational equivalent of rollback time. When an agent misbehaves at scale, the response involves freezing the agent, attributing the failure, notifying affected users, and reauthorizing before resuming. If that sequence was not designed, incident recovery time measures the speed of improvisation. Most teams have not designed it.

**Into the next sprint**

Every one of these six metrics is a sprint input, not just a performance indicator. Override frequency trending upward in a specific workflow means the autonomy boundary needs recalibration. Calibration diverging from actual accuracy means the feedback mechanism between user corrections and model behavior is broken. Incident recovery time that has not improved across three incidents means the recovery surface was designed once and never iterated. The observation phase does not close at the quarterly review. It closes when the finding lands in the next sprint.

---

## The Metric Is the Test of the Design

There is a forcing function in the measurement problem that exposes the design gap directly.

If a team cannot produce the override frequency metric, the override surface was not designed to be legible or logged. If they cannot produce rollback time, recovery was not treated as a product surface. If they cannot produce a confidence calibration curve, confidence was not surfaced to the user in a measurable form. The absence of the metric is not a data infrastructure problem. It confirms that the corresponding phase of the product lifecycle was never built.

This is the reversal that agentic products require from teams trained on SaaS instrumentation. In traditional SaaS thinking, you design the product and instrument it afterward. In agentic product design, the metric is the design requirement stated in advance. You design the approval moment because you need to measure override frequency. You design the recovery workflow because rollback time must become a sprint target. You design the audit surface because traceability is a product commitment, not a logging exercise. The observation phase and the build phase are the same decision, made at different moments in the cycle.

---

## The PM Owns the Loop

Product lifecycle management is a PM responsibility. Not the launch. The loop.

Engineering builds the instrumentation. The PM defines what to instrument, why each metric matters to the next release, and what decision each signal should enable. That means owning the six metrics before the first production incident, not as a retrospective task. It means reviewing override frequency alongside completion rate in every sprint review. It means setting the rollback time target before launch, because the target is what forces the recovery workflow to be designed and not deferred.

The organizations furthest along on this treated the observation phase as a design brief, not a postmortem. Bank of New York (BNY) Eliza platform, with over a hundred digital employees operating in regulated financial services, maintains human oversight at the policy and exception level. The governance design, what triggers review, what the recovery path looks like, who sees what when, preceded the deployment decision. The PM closed the loop before anyone shipped.

---

## The Question That Precedes the Dashboard

The signals exist whether or not teams design them. Override behavior is recorded in support tickets. Recovery time appears in incident postmortems. Miscalibrated confidence shows up in churn, after a failure nobody saw coming, measured in months.

The question is not whether the data exists. It is whether the product lifecycle is designed to see it, act on it, and turn it into the next sprint.

You do not leave a group of toddlers unobserved in a room, regardless of the setting or their behavior record. Not because you expect the worst. Because observation is not a trust judgment. It is a design requirement.

The same logic applies to any system that acts autonomously in the world. Launch is not the end of the product lifecycle. It is the moment the observation phase begins.

---

*This article is part of an ongoing series on AI product design, healthcare data, and the human side of technology adoption.*
