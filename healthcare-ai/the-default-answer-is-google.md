# The Default Answer Is Google

She was in her early forties. Athletic build, the kind you earn. She sat down across from her primary care physician, set her phone face-up on the desk, and before he could finish asking what brought her in, she said: "My watch told me my heart is doing something irregular."

He waited for more.

"I don't feel anything," she said. "I haven't felt anything. I got the watch as a birthday gift about three weeks ago. Wednesday night it sent me a notification. It said I should get checked."

He asked the questions anyway. Any chest pain? No. Shortness of breath? No. Dizziness, palpitations, pressure, anything that made her stop what she was doing? No, no, no, no. She had run six kilometers that morning. She felt fine. She had come in because an algorithm told her to, and she trusted it enough to take a morning off work.

The ECG confirmed atrial fibrillation. Paroxysmal, likely. She had no idea.

The device had done something right. It had caught something real. And yet the entire architecture of the clinical encounter, the history, the symptom progression, the patient's own experience of her body, had been bypassed. She had not come in with a problem. She had come in with a finding. Those are different consultations, and medicine was not designed for the second one.

That was a few years ago. What Google ships on May 7, 2026 will make that consultation the norm.

---

## What Google actually launched

Read the product announcement carefully and a pattern emerges. The Fitness tab and the Sleep tab are wellness features. Workout planning, sleep consistency, recovery nudges. These are the features the marketing leads with, the features Stephen Curry endorses, the features that place the product firmly in the wellness category.

The Health tab is different.

The Health tab allows users to sync their personal medical records, ask the Coach to synthesize them, and receive "clear summaries of complex medical data." That is not wellness coaching. That is clinical interpretation. The distinction between summarizing a medical record and interpreting it is narrower than the product team may want to acknowledge. A synthesis of someone's cardiology notes, their medication history, their recent labs, and their wearable data, delivered as a clear, actionable summary, is not neutral. It reflects choices: what to foreground, what to omit, how to weight conflicting signals, what pattern to name. Those choices are medical judgment. They have always been medical judgment. Calling them a "summary" does not make them less so.

Google has shipped a judgment layer. The data layer, wearables, Apple Health, medical records, has existed for years. What is new is the interpretive layer that sits above it: the thing that decides what the data means, what the pattern suggests, and what the user should do about it. In clinical medicine, that layer has a name. It is called diagnosis. It requires a license. It carries liability. It is governed by a professional obligation that does not switch off between consultations.

The Google Health Coach carries none of those things. Not because Google was negligent. Because the product was carefully framed to sit below the line where those requirements attach.

---

## Three breaks in clinical practice

That consultation was unusual when it happened. It will not be unusual for much longer. The opening scene illustrates one of three breaks that consumer health AI creates in clinical practice. What Google shipped this week creates the other two.

**The first break is the symptom language gap.** Medical training is built on a specific kind of patient communication. Sharp pain that worsens with inspiration. Pressure that radiates to the left arm. Fatigue that has been building for six weeks. Physicians learn to elicit these descriptions because the language of symptoms is the language of differential diagnosis. The quality of the pain, its timing, its triggers, its character: these are not conversational details. They are clinical data points that have been refined over centuries of practice into a diagnostic instrument.

Wearable devices capture a different category of signal entirely. They find occult findings, things the patient never felt, never noticed, and cannot describe, because there was nothing to describe. Paroxysmal arrhythmias. Sleep apnea events. Subtle heart rate variability patterns. The physician trained to say "describe the feeling when it happens" is now sitting across from a patient who has never had a feeling. The symptom history is missing. Not because the patient is a poor historian. Because there is no history to give. The interview pivots — to risk factors, to family history, to prior episodes the patient may not have registered as significant. But the diagnostic instrument the encounter was built around, the symptom-driven differential, has nothing to work with.

This matters because of how clinical reasoning is actually structured. Medicine is built around hypothesis-first reasoning. Symptoms generate a differential diagnosis. Tests are ordered to validate or rule out the items on that list. The finding arrives in the context of a question that was asked before the test was run, and its meaning, its urgency, its weight, depends entirely on that prior question. A result is not evidence in isolation. It is evidence in relation to a hypothesis. Medicine does have finding-first protocols for certain imaging incidentalomas — Fleischner Society guidelines for incidental lung nodules, Lung-RADS, Bethesda for thyroid findings. These work because they are clinician-initiated, population-defined, and governed by structured frameworks with clear thresholds. No equivalent framework exists for consumer wearable findings, and none at all for findings that arrive pre-interpreted by an AI synthesis layer.

The Holter monitor, the twenty-four-hour continuous ECG that might have detected what her watch found, is a test physicians order in response to clinical suspicion. Palpitations. Near-syncope. Unexplained fatigue. It is also ordered after cryptogenic stroke, or in selected high-risk asymptomatic populations, but even then the order follows a defined clinical question about a defined patient. The test exists to answer a question the physician has already formed. Pre-test probability shapes how the result is read. The same strip means different things depending on why it was ordered.

Medicine does have finding-first frameworks. Fleischner for incidental pulmonary nodules. Lung-RADS for screening CT. Bethesda for thyroid nodules. The ACR Incidental Findings white papers for adrenal, renal, hepatic, and pancreatic findings. Each took years of professional society work. Each is signed by a named body. Each has a bounded scope, codified risk modifiers, versioned updates, and an output that is a management pathway, not an interpretation. The wearable-AI-coach pattern shares none of those properties. It is being deployed at consumer scale before any equivalent framework exists.

What arrived in that consultation room had no prior question attached to it. The device had run the investigation before anyone had a reason to order it. The physician is now left constructing clinical context backward, building a hypothesis to fit a finding that arrived uninvited. That is not diagnosis. It is rationalization after the fact. And the clinical system has no protocol for the difference.

**The second break is the synthesis inversion.** A physician seeing a patient for the first time performs two simultaneous acts: gathering data and interpreting it. These are not sequential steps. They are interwoven. The patient mentions a detail in passing. The physician notices it is incongruent with the working hypothesis and probes it. The history changes. The hypothesis changes. The questions change. The synthesis emerges from the interaction, shaped by what the physician is looking for and what the patient reveals in response to being looked for it.

When a patient arrives with a Google Health Coach summary of their medical records, the synthesis has already been performed. The physician receives a pre-processed output, a narrative shaped by choices the model made before the patient walked in. The physician did not ask those questions. The physician cannot see which signals the model weighted heavily and which it discarded. The interpretive choices are embedded in the summary, invisible.

This is not the same as receiving a radiology report or a cardiology consult. Those are specialist interpretations of specific studies within a defined scope, by a credentialed professional who can be questioned, who carries liability, and whose reasoning can be audited. A model-generated synthesis of an entire medical record is not bounded by scope, carries no professional liability, and cannot explain its reasoning in a form that allows the receiving physician to evaluate it.

The physician is now doing a differential diagnosis on the model's interpretation of the patient's data. If the model's synthesis was wrong, the physician may never encounter the signal that would have corrected it.

**The third break is the invisible interpretation layer.** This is the sharpest version of the concern, and the one most likely to be dismissed. The objection will be: physicians already receive pre-synthesized data constantly. Discharge summaries. Referral letters. Lab panels with flagged abnormals. Pre-synthesis is not new.

The objection is right about pre-synthesis. It is wrong about what is new. What is new is the scope, the invisibility, and the authority signal. A discharge summary has an author, a date, a clinical context, and a defined purpose. A referring physician's letter names what it knows and what it does not. These documents have boundaries. A model-generated synthesis of a patient's complete medical records, wearable data, and personal health history has no such boundary. It presents as comprehensive. It reads as authoritative. The user, and potentially the receiving physician, has no mechanism to interrogate what was left out, what was downweighted, or why a particular framing was chosen.

The interpretive choices are not visible. The summary is. Medicine has a term for reasoning from an incomplete or misleading picture toward a confident wrong conclusion. It is called premature closure. The Google Health Coach, in synthesizing the medical record before the clinical encounter begins, creates the structural conditions for premature closure at scale.

---

## The regulatory boundary that makes this possible

None of this is accidental. Google's announcement lists a SHARP evaluation framework — five stated priorities: safety, helpfulness, accuracy, relevance, personalization. No published methodology accompanies them, no scoring rubric, no validation results. The Consumer Health Advisory Panel of clinicians is real. The privacy commitments are real. The product team appears to have thought carefully about what they were building.

What they also appear to have thought carefully about is where to position the product. "Wellness coach," "health and wellness advisor," "personalized guidance": this language is not incidental. It is the language that places Google Health Coach outside the regulatory boundary where clinical claims attract FDA scrutiny. The Coverage Gradient — a pattern I have described in earlier pieces in this series — holds: regulatory intensity tracks clinical claims, not patient contact or patient risk. A product that interacts with a patient 24 hours a day, synthesizes their complete medical record, and advises them on findings from a cardiac monitor sits in the general wellness category as long as it does not make an explicit diagnostic claim.

The Health tab is unlikely ever to say "you have atrial fibrillation." It is more likely to say "your heart rate data shows a pattern that may warrant a conversation with your doctor." The practical implication for the patient's next step is similar: seek evaluation. The regulatory category is different.

This is not a criticism unique to Google. It is the structural condition of consumer health AI. The tools with the most patient contact and the most interpretive reach sit in the least-regulated space, because they are careful about the exact words they use. The framework was not designed for this. It was designed for a world where the thing recommending clinical action was software running in a hospital system, not a wellness subscription bundled with a search engine.

---

## The installed base problem

Gemini AI Pro and Ultra subscribers now receive Google Health Premium at no extra cost. That is not a health product launch. That is one of the largest health coaching deployments in history, delivered through a general-purpose AI subscription that millions of people already pay for.

Guidance from clinical professional bodies on how to receive a Google Health Coach summary does not exist. Protocols for what a physician should do when a patient arrives with a model-synthesized medical record have not been written. Medical education has not addressed how to conduct a consultation where the patient's primary source of health interpretation is a consumer AI product they have been using for three weeks.

The coach will be in the room before the literacy is. That is not a criticism of Google's timeline. It is a description of how technology adoption works when the installed base grows through a general-purpose subscription rather than through a clinical procurement process with training requirements and implementation support.

---

## The question your institution has not answered

The patient in the opening scene came in because a device caught something real. The clinical system managed it, eventually. But the encounter required adapting in real time to a kind of consultation that training had not prepared for: no symptoms, no history, a device finding, and a patient whose entire relationship to her own body had been mediated by an algorithm for three weeks.

That was one patient with one watch. What arrives next Tuesday is a patient with three weeks of Google Health Coach summaries, a synthesized view of her last two years of medical records, a set of insights about her sleep, her heart rate variability, her readiness score, and a notification that something in the pattern has changed.

What is your institution's protocol for that consultation?

If the answer is that the physician will figure it out, that is not a protocol. It is a delegation of an unresolved design problem to the person least positioned to solve it in the middle of a twelve-minute appointment.

The judgment layer just shipped. The question of who arbitrates when the coach's interpretation conflicts with the clinician's has a default answer now. The default answer is Google.

Patients have always had informal defaults for health interpretation — search engines, family members, pharmacists, their own pattern-matching. What is new is a default that is continuous, multimodal, integrated with wearable and medical-record data, and bundled with a subscription tens of millions already have. That is a different category of default. Whether it is the right one is a question medicine has been avoiding. It will not be able to avoid it much longer.

---

*This article is part of an ongoing series on healthcare AI, clinical workflow, and the systems that connect them.*

*With thanks to [Gilles Frydman](https://www.linkedin.com/in/gillesfrydman/) for bringing this announcement to my attention.*
