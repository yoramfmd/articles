---
title: Listen to the patient.
slug: medicine-knew-this-in-1975
published: 2026-03-16
excerpt: We evaluated AI health tools by removing the very mechanism that makes diagnosis work, measured what happened, and called it a safety problem. It is not just a safety problem. It is a design problem. Medicine knew this in 1975
url: https://data-decisions-and-clinics.com/medicine-knew-this-in-1975/
tags: Healthcare AI
source: ghost-api-pull-2026-08-04
---

---

The first clinical skill you learn as a medical student is how to talk to a patient. Not how to examine them. Not how to order tests. How to talk to them.

The textbook is "Bates' Guide to Physical Examination and History Taking", first published in 1974. It has been updated through more editions than I can count and is still the gold standard today. Still the first book you are told to buy. Still the framework every physician-in-training uses to learn how to conduct a proper patient interview: the structure of the encounter, the sequence of questions, the discipline of following a thread without leading the witness.

I remember buying it as a young medical student and feeling like I was learning a clinical superpower. Then I encountered my first 3am shift. The patient was an intoxicated tourist who spoke a dialect of Tagalog that no one in the department could understand. I thought about Bates' Guide. I thought about the proper sequence of history-taking. And I improvised anyway.

Ask any physician. They will tell you the same thing. The textbook techniques rarely survive the real ward at full fidelity. But the underlying principle always does: get the story. Because without the story, you have nothing.

### Medicine Proved This in 1975

Hampton and colleagues did the work to put a number on it. They followed 80 patients through a general medical outpatient clinic and asked the attending physician to record the most likely diagnosis at three specific moments: after taking the history, after performing the physical examination, and after reviewing the lab results.

In 66 of the 80 patients, the correct diagnosis was already present after the history alone. The physical examination changed the diagnosis in 7 cases. Laboratory tests in 7 more. The story the patient told was, in roughly 82% of encounters, already the diagnosis. In most cases, everything else was confirmation or refinement. In some, the exam or tests were decisive. But the history was where the reasoning began, and in most encounters, it was also where it ended.

Hampton published this in the British Medical Journal in 1975 and concluded that more time should be spent on history-taking, more emphasis placed on teaching students how to listen, and less on teaching them how to order tests. The paper was cited, celebrated, and largely ignored. We kept ordering tests. Fifty years later, we started building AI that assumed the tests were the point.

### The Interface Is a Clinical Instrument

The way an AI health system asks questions is not a neutral design choice. The interface is a cognitive filter. It determines what the patient can communicate and what the model is allowed to express. That distinction has been almost entirely absent from the healthcare AI debate.

A model with extensive medical knowledge can be forced into diagnostic failure by an interface that constrains its output or suppresses its ability to ask follow-up questions. The user experience design is not a wrapper around the clinical intelligence. It is part of the clinical intelligence.

In early 2024, a study published in Nature Medicine reported that ChatGPT Health under-triages 51.6% of medical emergencies, concluding that consumer AI health tools pose fundamental safety risks. The finding generated substantial media coverage and policy attention.

The evaluation method: clinician-authored vignettes, forced A/B/C/D response format, explicit suppression of clarifying questions, single-turn interaction, reasoning restricted to only the information provided in the message.

That design is not unreasonable as a test of current consumer tools, many of which do operate under similar constraints. The problem is what the methodology cannot measure: the ceiling. Once you suppress clarifying questions and force a letter choice, you are no longer measuring clinical reasoning. You are measuring performance under conditions that preclude clinical reasoning. No competent physician triages from a single structured message without follow-up. The study drew conclusions about AI triage capability from a design that removed the capability it was trying to assess.

### What Happens When You Restore the Conversation

This March, researchers at Macquarie University published a partial replication testing five frontier models under two conditions: the original constrained exam-style format, and a naturalistic condition using patient-style messages with no forced-choice format and no suppression of clarifying questions.

The results in their sample were specific and striking. Asthma, the scenario with the worst under-triage rate in the original study, improved from 48% to 80% when the format was naturalistic. DKA was correctly triaged 100% of the time in both conditions, suggesting that at least part of the failure in the original study was a product-layer artifact, not a reasoning deficit.

The most striking result came from isolating a single variable: forced A/B/C/D versus free-text response. In that study, three of five models scored between 0% and 24% under forced choice and 100% under free text. Same clinical scenarios. Same models. The only variable was whether the AI could answer in its own words.

These models were recommending emergency care correctly in natural language while the forced-choice format was registering under-triage. The AI identified the emergency. The interface prevented it from saying so. That is not a story about a model that cannot reason. It is a story about a mis-specified interface. The researchers called this "interface-induced failure," and the distinction matters: it is a different category of problem from model capability, and it requires a different category of solution.

### The Deeper Problem

The evaluation format is one layer. The interaction design is another.

Real clinical conversations are not single-turn exchanges. Empirical work on conversational health AI suggests that clinically meaningful interactions often require on the order of a dozen exchanges, with many falling between 12 and 17 messages, to surface a story complete enough to act on. Single-turn evaluations systematically underestimate what AI can do when it is actually allowed to conduct a conversation.

User research on existing symptom checker apps documents what clinicians already know. These tools frequently fail to ask about current medications, existing diagnoses, and prior surgeries. Patients with chronic or complex conditions cannot fit their reality into a preset multiple-choice list. The interface fails to elicit the story. The AI then reasons on an incomplete one and looks unreliable.

There is also something that text cannot capture that physical presence can. When a patient says "it is probably nothing serious," a physician in the room observes the patient's distress, their breathing, the way they are sitting. The clinical skepticism that overrides the patient's own framing is informed by everything that is not in the words. Research confirms that social anchoring in text-based AI interactions, when users frame their own symptoms as benign, significantly shifts recommendations toward lower-level care. In face-to-face encounters, physicians override this. The text interface often cannot.

There is a second layer to this problem that is harder to quantify but I suspect is already in the data somewhere. The quality of what the patient submits is degrading. As people increasingly rely on grammar checkers, autocorrect, and AI-assisted writing in daily life, their ability to produce an accurate, unmediated account of what they are experiencing, especially under stress or fear, is quietly eroding. The raw sensation gets filtered through a correction layer before it reaches the interface. The parent who types "my child is a bit fussy" because autocorrect tidied away "acting really weird" and "breathing funny" has already lost clinical signal before the AI sees a single word. The interface is not just suppressing the AI's ability to ask follow-up questions. The input it is working from is becoming a less reliable representation of the clinical reality at the other end.

Bates' Guide did not last fifty years because it taught medical students to fill out a form. It taught them to read the room.

### The Design Consequence

If you believe healthcare AI fails at triage because of model capability, you invest in better models. You push vendors to improve benchmark scores. You build oversight structures around the assumption that the AI will often get the clinical reasoning wrong.

If you understand that healthcare AI appears to fail because the evaluation format suppresses its reasoning mechanism, and that the interaction design determines how much of the patient story actually gets elicited, you build something different. Conversational architecture. Multi-turn interaction. Clarifying questions. Context accumulation across the encounter. You design the AI to behave the way medicine designed physicians to behave: get the story first, form the hypothesis, then ask the targeted question that confirms or refutes it.

These are not incremental differences. They produce different products, different regulatory framings, and different assumptions about where the clinical value lives.

I have spent fifteen years building customer-centric software solutions, and I have stood in the clinic and occasionally at 3am with patients whose stories did not arrive in a structured format. Both experiences point to the same conclusion: the interface between the human and the diagnostic intelligence is not a technical detail. It is the critical point. Getting it wrong does not produce a better model that fails slightly less. It produces a fundamentally different product from the one you intended to build.

### What the Book Already Told Us

Hampton's 1975 conclusion called for more emphasis on communication research and less on developing new laboratory services. He was writing about physicians. The same argument applies to AI today.

The patient story is the diagnostic instrument. Not the exam. Not the tests. Not the structured form in the waiting room. The conversation, the iterative exchange in which the clinician follows the thread, adjusts the hypothesis, asks the targeted follow-up, and reads what is not being said, is where the diagnosis lives.

We taught every medical student this from a book first published in 1974. It is still in print. Still the gold standard. Fifty years later, we are building AI health tools that prevent the AI from doing what the book taught us to do. And we are measuring the result and calling it a safety problem.

It is not just a safety problem. It is, at its core, a design problem.

The diagnosis was always in the conversation. We just have to let the AI have one.
