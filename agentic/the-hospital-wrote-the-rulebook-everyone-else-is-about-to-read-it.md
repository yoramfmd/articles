---
title: "The Hospital Wrote the Rulebook. Everyone Else Is About to Read It."
slug: the-hospital-wrote-the-rulebook-everyone-else-is-about-to-read-it
published_at: 2026-08-22
custom_excerpt: "Healthcare asks who is accountable for a machine's mistake before it asks what the machine can do, because it has no choice. On 18 August a federal regulator applied that question to generative AI. The framework it produced is not new. It is clinical governance, written down for everyone else."
tags: [agentic, healthai, pm]
feature_image: https://storage.ghost.io/c/e6/05/e605b234-3cc8-4fe4-97bb-2bb55b18b8fb/content/images/2026/08/ChatGPT-Image-Aug-22--2026--04_11_15-PM.png
source: ghost
---

# The Hospital Wrote the Rulebook. Everyone Else Is About to Read It.

# 

On 18 August the FDA's device center published a discussion paper on how to regulate generative AI in medical devices. Thirty-one pages, twenty-six open questions, and an explicit note on page one that it is not guidance and not policy. A regulator thinking out loud in public.

I read it the same week, expecting a document about medical devices. It is not really that. It is the clearest statement I have seen of how to govern any system that acts on your behalf, and almost none of it is about medicine.

That is the part worth sitting with, and it is not a story about the FDA being clever.

### Healthcare asks the accountability question first because it cannot avoid it

In March I argued that the north star for AI is not Silicon Valley, it is the hospital, and that the constraints clinical AI operates under "are the quality standard that every other industry will eventually need to meet, whether by choice or by regulatory force."

I did not expect the receipt to arrive in five months.

The reason healthcare gets to these answers first has nothing to do with being more thoughtful. It is structural. In a hospital there is always a named person who signs. There is a license that can be suspended, a malpractice system that assigns liability to a human being regardless of what the machine said, and a mandatory reporting duty when something goes wrong. Before anyone asks what a clinical tool can do, someone has already asked who answers when it is wrong, because the answer determines whether the tool can be used at all.

Enterprise software has none of that machinery. A workflow tool that quietly makes a bad call produces a support ticket, not a deposition. So the question of who is accountable was never forced, and an industry that is not forced to answer a hard question does not answer it.

That is changing, and the discussion paper is what the change looks like when it is written down.

### The same ideas, arrived at independently

What makes the paper interesting is not that it agrees with a position I hold. It is where the agreement lands.

The paper's whole risk framework rests on two variables: how independently the system acts, and how bad it is to rely on a wrong answer. That is an autonomy ladder crossed with a consequence classification. I published a piece in April on a health system that climbed the autonomy ladder without designing the rungs, and one in June arguing that autonomy is earned rather than scheduled, that movement up requires demonstrated performance at the rung below rather than a review count or a go-live date. The paper's competency model is explicitly modeled on clinical training: supervised practice "with progressively greater independence."

The paper asks how to test a system whose behavior drifts across a long conversation, where each individual turn looks in-scope and the cumulative interaction is not. It asks how a manufacturer detects a change to a third-party model initiated by somebody else entirely. It asks whether postmarket monitoring can be run by machine supervisors, and then, in the same sentence, asks about "the evaluation and reliability of the supervisory agent itself."

I wrote about silent degradation in deployed clinical AI in April, and about drift across the substrate an agent is built from. I wrote in April that one green checkmark on a non-deterministic system tells you it passed once, not that it passes. In July I wrote that authority handed to an agent has to be handed over the way an attending physician hands over to a night nurse: not as a description of good practice but as an order set, with thresholds and the vital sign that means stop and call.

The paper's safety element S.2 asks whether a system recognizes when a request exceeds its scope and refuses. Its agentic element asks for "compliance with human-oversight checkpoints before irreversible or high-consequence actions." That is the order set, in a regulator's vocabulary.

None of this is borrowed in either direction. The paper does not cite me and I had not seen it. Two parties working the same problem from opposite ends arrived at the same structure, which is the only kind of agreement that means anything.

### The line I would put on a wall

Buried in the risk section is a sentence that should end an argument I have watched teams have for two years.

A patient-facing function, the paper says, "may not become any less directive because it includes a 'talk to your doctor' or an 'I am not a medical professional' statement."

Every product team that has shipped an assistant knows this argument. Legal asks for a disclaimer. The disclaimer goes on. Everyone agrees the risk has been handled. It has not been handled. The output still tells the user what to do, and appending a sentence about consulting a professional changes the liability posture without changing a single thing about how the user behaves.

A regulator has now said in writing that the disclaimer does not lower the risk. That transfers directly, and it has nothing to do with medicine.

### Where the paper is thin, and it is the same place everyone is thin

I would rather be useful than triumphant, so here is the gap.

The framework treats "acts with continuous human supervision" as a lower-risk position on its activity axis. It never asks what that supervision costs in reviewer-hours, or whether it survives contact with a busy Tuesday. Automation bias appears exactly once in thirty-one pages, as a property of how an output is worded, rather than as the systemic failure of the oversight the entire framework leans on. Lisanne Bainbridge described this in 1983 and it has been replicated ever since.

I wrote in May that we may be the last generation that can supervise AI, because supervision is a skill that decays precisely when the system is good enough that you stop practicing. A framework that counts human review as a mitigation, without pricing the review or measuring whether it is still happening, is counting on something it has not checked.

That is a real hole and it is worth saying so. It is also fixable, and the comment docket is open until 19 October.

### What this means if you do not work in healthcare

You are going to inherit this vocabulary. Not because the FDA regulates your product, but because the questions are the same questions and healthcare has already paid for the answers.

The four books I have written on agentic product management were built on exactly the material in that paper, from the other direction. *Agentic AI for Busy Product Managers* is the ladder and the boundary. *Why Agentic AI Products Fail* is the gap between a demonstration and a product, which is the gap between the paper's benchmarking and its clinical confirmation. *The Agentic AI Team* is the accountability question made concrete, including who owns the evaluation and why it cannot be the person who built the thing, which the paper independently insists on when it requires adjudicators "structurally independent from the device sponsor." *The Agentic AI Practitioner*, out next month, is what a person actually does on a Monday.

I did not write them about healthcare. I wrote them out of healthcare, which is a different claim and a stronger one.

There is a habit in technology of treating regulated industries as the slow ones. The regulated industry is not slow. It is the one that already ran the experiment, took the casualties, and wrote down what it learned, while everybody else was still describing the technology as too new for rules.

Clinical medicine spent decades answering a question that enterprise software has mostly been able to avoid: when a system participates in a decision, who owns the outcome. It answered with named accountability, graduated authority, supervised practice, standing orders, incident review, and recertification. Every one of those has an analogue in the discussion paper, and every one of them has an analogue in the agentic product you are shipping this quarter.

The hospital did not write that rulebook for you. It wrote it because people died when it did not have one.

Read it anyway.


---

*This article is part of an ongoing series on product management, enterprise AI, and the systems that connect them.*


---

## Sources and dates

**The discussion paper.** FDA, Center for Devices and Radiological Health, Digital Health Center of Excellence. *Considerations for the Regulation of Generative AI-Enabled Medical Devices: Discussion Paper and Request for Feedback.* Published 18 August 2026. Docket FDA-2026-N-7874; comments close 19 October 2026.

**Prior work referenced, with publication dates from the platform export:**

*The North Star for AI Isn't Silicon Valley. It's the Hospital.* 18 March 2026. *AI Evals: What the Checkmarks Actually Prove.* 10 April 2026. *Silent Degradation: What a Deployed Clinical AI Looks Like at Month Eighteen.* 7 April 2026. *Utah Climbed the Autonomy Ladder. Nobody Designed the Rungs.* 30 April 2026. *The Last Generation That Can Supervise AI.* 1 May 2026. *The New PM Job: Designing the Supervisory Layer.* May 2026. *AI Product Management: Autonomy Is Earned, Not Scheduled.* 5 June 2026. *Your Engineers Are Writing the Policy Now.* 21 July 2026.

Bainbridge, L. *Ironies of Automation.* Automatica 19(6), 1983, 775 to 779. DOI 10.1016/0005-1098(83)90046-8.
