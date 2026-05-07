---
title: The Voice
slug: the-voice
published: 2026-01-09
excerpt: At 11pm, patients don't need a model. They need an answer. AI is already filling that gap, not because it's better, but because it's there. The risk isn't just accuracy. It's a new layer of care with no training, no accountability, and no clinician in the loop.
url: https://data-decisions-and-clinics.ghost.io/the-voice/
---

# The Voice

Early in my career I worked for a private EMS service, providing on-call physician consultations by phone. Patients would call when they felt unwell, before any clinician had anchored on a diagnosis, before any framing had occurred. I would listen, watch a 3-lead ECG tracing come through remotely, assemble a clinical picture from fragments, and decide whether to dispatch a mobile ICU to their home.

The voice told you almost everything. Not just the words, but the rhythm, the breathing between sentences, the pace at which someone could speak. A patient who paused mid-sentence to catch their breath was telling me something the vital signs would confirm only later. A voice that was too calm for the symptoms being described was its own kind of signal. You could hear whether someone needed a team at their door in the next twenty minutes before you had processed a single data point. Those calls happened at all hours. The patient had one option: call the number and hope someone competent was at the other end.

That was the 11pm problem as I first encountered it, from the physician's side.

I left the hospital after those residency years and spent the better part of a decade working as a product manager at SAP. Shortly before COVID-19 arrived, I left again because I wanted to work on something in healthcare. I was lucky to spend time working on a product that was supposed to be there at 11pm: a mobile application that tracked blood pressure, delivered cardiac coaching, sent medication reminders, and sat in a patient's pocket between the moments when anyone with a medical degree was available. For thousands of patients managing hypertension and diabetes, the app was the most frequent clinical interaction in their week.

I noticed something I could not stop thinking about. Patients trusted the app. Not because it was a physician. Because it was there. When the clinic was closed and the nurse line was hold music, the app was available. It answered. It did not judge. It did not rush them to the next appointment. For patients who had spent years feeling invisible to the healthcare system, a product that paid attention consistently was a different kind of relationship. Patients already trusted technology with their health, partly because the alternative was often worse. The question was what we owed them in return.

---

Most of the conversation about AI in medicine today centers on the physician. Cognitive load. Workflow integration. Decision support systems that surface the right information at the right moment. Governance frameworks that assign accountability when something goes wrong.

All of it assumes a physician somewhere in the loop. Present, credentialed, legally accountable, trained to distrust the header and look at the underlying data.

This article is about the place those conversations do not reach.

---

## The gap between visits

The hardest problem in clinical care has never been the visit. It has been the hours after the visit, when the patient goes home and something changes.

A blood pressure that was fine in the clinic spikes at midnight. A new symptom develops Thursday afternoon, mild enough to wait, concerning enough to lose sleep over. A side effect appears on day four of a new medication, after the prescription instructions were tossed in the trash a few days before.

The gap between visits has always been where medicine is weakest. The 24-hour nurse line existed to bridge it. The patient portal message existed to bridge it. The after-visit summary existed to bridge it. None of them fully did, because none of them were actually present at the moment the question arose. They were structures built to handle what happened after the patient had already decided it was worth pursuing. And the physicians those structures were meant to connect patients with were themselves increasingly unavailable, not because they had stopped caring, but because the volume of messages, refill requests, and portal questions from the hours the clinic was open had already consumed them.

The mobile health app was the first technology that could actually be present. Always on, always available, always in the pocket. Its limitation was that it could only respond to what it was designed for. A blood pressure app could track blood pressure. It could not answer the question the patient actually had at 11pm, which was: is this normal, should I be worried, and do I need to go to the emergency room right now?

That question, the 11pm question, is what large language models arrived equipped to answer.

---

## The experiment nobody chose

Before addressing what happens when the AI answers, it is worth pausing on what normalized the conversation.

When COVID-19 arrived and telehealth expanded almost overnight, I was watching as a product manager, not as a practicing clinician. What I saw made me skeptical. I had trained under physicians of an older school, professors who could walk into a room and diagnose cirrhosis from a patient's skin tone, or suspect uncontrolled diabetes before a word had been exchanged. The physical examination was not a ritual. It was information. The smell of the room, the way a patient moved, the quality of their breathing at rest: none of that travels through a camera, and I was not sure how medicine conducted through a screen could be real medicine at all.

I have since become a telehealth patient myself, which I find slightly ironic. My own physicians cannot examine me the way I was taught to examine patients. I notice what they are not able to check. The gap between what I know is missing and what gets documented is not small.

What I also noticed, watching the technology from a product perspective, was that telehealth worked better than I expected for a specific category of encounters: follow-ups, medication adjustments, mental health check-ins, chronic disease monitoring. Situations where the conversation is the visit, not the physical contact. By 2023, telehealth for many conditions had become the patient's preference, not the fallback.

That normalization matters for what came next. Patients had already accepted a screen between themselves and their doctor. The step from a physician on a screen to an AI on a screen was shorter than anyone had anticipated. The next abstraction was not a revolution. It was a continuation.

---

## The 11pm question

Many patients are now using large language models as their first-line health information source. The debate about whether this should happen is over. It is happening, and it has been happening since late 2022 at significant scale.

What makes this different from every prior evolution in the physician-patient relationship is the absence of the physician anywhere in the loop. At every previous inflection point, a trained clinician remained somewhere between the algorithm and the consequence. The radiologist reviewed the AI flag. The cardiologist looked past the header at the actual tracing. The anesthesiologist kept one hand on the override. The pathologist signed the report.

Here, there is no one. A patient describes their symptoms, the model synthesizes, and a clinical-sounding answer arrives in seconds. Fluent, confident, and without any awareness of the patient's medication list, their prior diagnoses, their family history, or the specific contraindication that would change the answer entirely.

The failure modes are not theoretical. An outdated treatment guideline presented as current. A drug interaction that does not exist, cited with the same fluency as one that does. The model does not know what it does not know. And unlike a physician, it has not been trained to say so.

Research consistently shows that most patients want to know when their doctor is using AI tools in their care. That expectation exists even in supervised clinical settings, where a physician remains present and accountable. In the unsupervised patient-facing setting, there is no disclosure infrastructure at all.

What has been built, over decades of clinical decision support and AI-assisted tooling, is an institutional infrastructure for the physician layer: training that teaches clinicians to verify and override, regulatory frameworks that define intended use, a culture that treats the algorithm as a tool rather than an oracle. None of that infrastructure exists for the patient layer. The patient has no training in skeptical consumption of AI health information. There is no regulatory framework that applies to a general-purpose model answering a health question late at night. There is no culture of distrust, because distrust requires knowing that distrust is warranted.

---

## From information to action

The conversation about patient-facing AI has so far been a conversation about information. What the AI says. Whether it is accurate. Whether the patient can evaluate it.

That conversation is already becoming obsolete.

The next layer is not the AI answering questions. It is the AI acting on behalf of the patient, inside the healthcare system, with the patient's credentials. In some health systems, patient-facing AI tools are beginning to generate messages to clinical teams, summarize records for second opinions, and flag potential medication issues before the patient has articulated a concern. Consumer health platforms are connecting physiological data from wearables to AI layers that generate personalized recommendations. Some applications are already scheduling appointments and requesting prescription refills; others are piloting capabilities that would allow the AI to initiate referrals without the patient composing a single sentence.

This is what might be called the tools-to-actors shift: the patient's AI is no longer a resource they consult, but an agent that acts on their behalf, inside clinical systems, in ways that interact with physician workflows, payer systems, and pharmacy records.

The accountability question that was already difficult when the AI was only providing information becomes significantly harder when the AI is also acting. A wrong answer late at night is a harm bounded by what the patient decides to do with it. An agent that sends the wrong message to the wrong clinical team, requests the wrong medication, or misrepresents the patient's condition in an automated prior authorization has introduced an error into the clinical record that may persist long after the patient realizes something went wrong.

---

## The layer nobody built

Consider the cardiologist reviewing an ECG with an AI-generated interpretation already printed at the top of the tracing. The algorithm offered a first read and the physician was expected to verify it. The liability was clear: the machine generated an interpretation, the physician bore the responsibility. That bargain was imperfect, but it had a structure. Someone was accountable. The chain was traceable.

The bargain assumed a physician.

In the setting this article describes, there is no physician in that chain. What medicine has never built is the equivalent infrastructure for the patient layer: a regulatory framework that applies to consumer AI health products, a training culture that teaches patients to calibrate their trust, a liability structure that can absorb what happens when the model gets it wrong and there is no physician signature anywhere.

This is not an argument against patient-facing AI. The case for it is strong and real. The patient who caught their atrial fibrillation on a smartwatch, the cardiac patient who managed their blood pressure through an app, the rural patient whose only accessible triage was a chatbot: these are not abstractions. They are people for whom the technology worked, at a moment when the alternative was worse.

There is a second problem inside this one. The benefits of patient-facing AI are not distributed evenly. Engagement with digital health tools drops significantly among patients who are not English-speaking, who are older, who have less familiarity with technology, or who have less reason to trust systems that have historically underserved them. The 11pm question does not disappear for those patients. It goes unanswered by different means. Any infrastructure built for the patient layer has to reckon with the fact that the patients who need it most are often the least likely to reach it in the first place.

The case is for building the patient layer with the same seriousness that medicine brought to every other layer. Not disclaimers. Infrastructure. Not terms of service. Training and accountability frameworks designed for the actual environment where patients encounter these tools, which is alone, at home, late at night, before they have decided they are sick enough to call anyone.

The voice that answers that question is no longer a physician's. And here is what makes this different from every other failure mode in clinical AI: the patient may not notice.

In every previous setting, a wrong answer had a human face attached to it. A physician who could be questioned, challenged, held accountable. The physician who gave the wrong advice was at least findable. Here, the model answers with the fluency of expertise and the warmth of presence, and the patient at 11pm feels heard. Whether they received accurate medical information is a separate question entirely.

Trust and accuracy have always been connected in medicine, through training, licensing, the threat of consequences. The model severs that connection quietly. It is available at every hour, it never rushes the patient to the next appointment, and it speaks with the same confidence whether it is right or wrong. The patient who trusted it last week will trust it again this week, because it was there when nothing else was.

If a machine can make you feel heard, it may not matter whether it understood what you said. That is not a technical problem. It is the one medicine has the least experience solving.

---

*This is part of the Signals Series — [data-decisions-and-clinics.ghost.io](https://data-decisions-and-clinics.ghost.io)*