# The Sequence Inverted

The neurology resident was tired. It was late in the ward round, the list was long, and the CT results had just come back on the patient in bed seven. Ischemic changes, left hemisphere. The attending glanced at the report, nodded, then walked to the bedside and stroked the sole of the patient's foot with the handle of a reflex hammer. The big toe extended upward. Babinski positive.

He wrote it in the notes and moved on.

Nobody said anything. Not the resident, not the medical students standing in a loose semicircle at the foot of the bed. The sign had been performed. The box had been ticked. But something in the sequence had shifted so quietly that it passed without comment: the Babinski had been done after the CT.

In the architecture of clinical reasoning as it was originally designed, that is the wrong order. The Babinski reflex was not meant to confirm a result. It was meant to generate a hypothesis. A patient complains of weakness on one side, or their gait is off, or a family member noticed something subtle at dinner. The physician examines them. The toe goes up. Now there is a question with enough clinical weight to justify imaging. The CT answers the question the Babinski asked. The sequence runs from body to machine, from observation to investigation, from hypothesis to test.

What happened in that ward round ran the sequence backward.

---

This is not a story about a bad physician or a failing hospital. The attending was competent. The CT was appropriate. The Babinski was noted correctly. Nothing went wrong in any way that a morbidity and mortality conference would flag. What happened was something quieter and more consequential: a clinical sign that had been designed as the start of a reasoning chain was used as a footnote at its end. The inversion was invisible because it had become normal.

That normalization did not happen overnight, and it did not happen because of AI. It happened across three distinct disruptions, each of which moved the sequence a little further from the model it was built on. Understanding those disruptions, and what is now accelerating them, is the only way to see clearly what is at stake.

---

## The first disruption: the body was already losing its primacy

Long before the pandemic, before telemedicine, before large language models summarized medical records, the physical examination was in decline.

Historical estimates suggest that bedside teaching in internal medicine fell from roughly three quarters of clinical teaching time in the mid-twentieth century to well under twenty percent by the 1990s. Time-motion studies of residents find that direct patient contact, including examination, accounts for somewhere between nine and thirteen percent of a shift. Physicians examine patients over gowns. They take less than six minutes. They skip components. And the mechanism is not laziness or indifference; it is the structure of the system they are working inside.

Modern healthcare is measured. Physicians are tracked on throughput, documentation completeness, appointment duration, and patient satisfaction scores. In that environment, a thorough physical examination is economically irrational. It takes time that the system has not allocated. The fifteen-minute appointment slot does not accommodate what the professors of internal medicine used to do: a full head-to-toe examination, unhurried, systematic, the kind that began with watching how a patient walked into the room and ended with percussion of every field. That level of examination was already becoming rare before most current residents were in medical school. For many trainees, it exists only as description, not as observed practice.

The New England Journal of Medicine was publishing concerned commentary about this trend by 2006. It was not a new observation even then. It was a formal acknowledgment of something that clinicians had been watching happen for decades.

What this created was a training system that grafted newer tools onto a foundation that had quietly thinned. The resident who never watched a master clinician perform a complete neurological examination does not know what they are not doing. The deficit is invisible to the person who carries it, because the reference point was never established.

There is a counterargument worth taking seriously here. The shift toward imaging and laboratory investigation was not purely a loss of discipline. Many classic physical signs have modest sensitivity, variable inter-rater reliability, and limited specificity. Evidence-based medicine spent decades demonstrating that some bedside maneuvers are less diagnostically reliable than clinicians had assumed. Part of what replaced the physical examination replaced it because it was genuinely more accurate. That is not decay. That is calibration.

The argument of this article is not that the physical examination was infallible or that its displacement was uniformly bad. The argument is that the reasoning process it trained, forming a hypothesis from direct observation before reaching for the machine, is harder to train when the machine arrives first. Those are different claims. The second one is harder to refute.

But the erosion was uneven, because some specialties had already reorganized clinical reasoning around instruments rather than direct examination, and the pattern of disruption differs depending on where a discipline started.

Internal medicine and general surgery placed the history and physical at the center. Other disciplines had already redistributed that weight long before the systemic decline began. In ophthalmology, the patient history is brief and the slit lamp is primary. An ophthalmologist without a slit lamp is, in a meaningful sense, as limited as the patient they are trying to evaluate. The device is not a supplement to clinical observation; it is the clinical observation. Radiology went further: the discipline eliminated the body from the equation almost entirely and made the image the primary object of reasoning. Pathology did the same with tissue. These are not failures of clinical reasoning. They are disciplines that understood early that certain questions could only be answered through specific instruments, and they built their reasoning models around that reality.

What is worth noting is where incidental findings come from. They come from radiology and pathology, the disciplines that removed the body from the front of the reasoning chain. The pulmonary nodule found on a chest CT ordered for a different reason. The adrenal mass discovered during an abdominal scan for flank pain. The thyroid lesion seen incidentally on a carotid ultrasound. These are not findings that began with a hypothesis. They are findings that arrived without one.

Medicine recognized this problem and built structured response frameworks for it. The Fleischner Society guidelines, the Bethesda system for thyroid nodules, the ACR Incidental Findings white papers: each took years of professional society work, each has named authorship, bounded scope, codified risk modifiers, and a management pathway as its output. Each converts a finding-without-context into a defined clinical response. These frameworks exist because finding-first reasoning is hard and has always been hard. Medicine knew this. It built the scaffolding carefully, over time, with explicit accountability.

What it did not know was that the scaffolding was about to be bypassed at consumer scale.

---

## The second disruption: telehealth removed the body from the room

COVID-19 did not create the trend. It compressed it. What had been a slow drift away from the bedside became, in the spring of 2020, an overnight structural change: the patient was no longer physically present, and the physician had to work with what remained.

What remained was the history. Voice, and sometimes video. The patient's account of their own symptoms, delivered through a screen, without the possibility of auscultation, percussion, or palpation. Without the smell of the room, the color of the skin under fluorescent light, the subtle asymmetry in the face that a conversation might reveal, the grip strength tested by a handshake.

The clinical literature that emerged from this period is instructive, and it cuts against the most intuitive prediction. The obvious assumption was that physicians, deprived of the physical examination, would compensate by ordering more tests. More labs. More imaging. If you cannot examine, you escalate to the machine.

The data does not support that assumption. Multiple studies found that imaging-ordering rates were lower after telemedicine visits than after in-person visits, in some analyses by nearly thirty percent. Several Medicare-focused analyses reported lower downstream lab and imaging utilization and modestly lower short-term spending for telehealth-initiated episodes. The pattern is consistent enough across settings and payers to be a real finding, not a methodological artifact. One contributing factor is case mix: telehealth attracts lower-acuity presentations, and lower-acuity patients need fewer tests. But even after accounting for this, the compensatory-ordering hypothesis does not hold.

What the data does support is something more troubling: telehealth produces a more fragile diagnostic chain. A 2023 cohort study found that roughly forty-two percent of tests and referrals ordered during telehealth visits were completed within the designated time frame, compared to nearly sixty percent for in-person visits. Less was ordered, and less of what was ordered was followed through. The physician managed the encounter, documented appropriately, and the thread between the visit and its resolution was more likely to go slack.

This is the telehealth diagnostic paradox. It is not over-ordering. It is incomplete follow-through. The test does not happen more often; it happens less reliably. The loop does not close.

The encounter structure, meanwhile, was not redesigned. The Association of American Medical Colleges created telehealth competency domains covering communication, data collection, technology, ethics, and equity. That domain structure is an implicit acknowledgment that clinical information gathering itself had changed. But the underlying model, the sequence of history to hypothesis to examination to test, was not replaced with a new architecture. It was adapted, worked around, taught as a set of substitutions and escalation rules. The script was modified. The underlying logic was not.

The result was that physicians entered the pandemic already working on a thinner examination base, adapted to that constraint in real time under enormous pressure, and emerged into a hybrid world where the old model was technically still operative but practically hollowed out. The body had been losing its primacy before COVID. COVID made the loss structural.

---

## The third disruption: the synthesis now arrives before the encounter

The first two disruptions changed when the physical examination happened and how much weight it carried. The third disruption is different in kind: it changes who forms the first interpretation.

In the traditional clinical encounter, the physician is the first synthesizer. The patient presents raw material: symptoms, timeline, history, concerns. The physician gathers it, organizes it, forms a working hypothesis, selects confirmatory tests, revises. The synthesis emerges from the interaction. It is not delivered to the physician. It is performed by the physician.

Consumer health AI has introduced a step before that step. Patients arrive having already processed their data through an interpretive layer. A wearable has flagged a pattern. A health coach has summarized two years of medical records and generated insights. An app has analyzed sleep architecture and heart rate variability and produced a readiness score with embedded clinical framing. The patient walks into the room carrying a pre-formed synthesis, and the physician must now decide what to do with it.

This is not the same as the internet-informed patient of the 2000s. A patient who arrived with a printed article was carrying a hypothesis, sometimes a confident one, but it was a hypothesis derived from symptom description, not from their own physiological data. The physician could challenge the framing by eliciting the symptom history in their own sequence, testing the patient's interpretation against the clinical picture.

A patient carrying a synthesis derived from their own medical records, their own wearable data, and their own longitudinal health patterns is carrying something different. The synthesis is personalized. It is anchored to real data about this specific person. The physician cannot dismiss it as generic. They must engage with it, which means they must audit it before they can reason independently.

That auditing is new cognitive work. Research on automation bias, the tendency to over-rely on algorithmic outputs and reduce independent judgment, shows that the risk is real, measurable, and not resolved by clinical experience. Studies consistently find that clinicians across experience levels are susceptible to accepting erroneous AI suggestions, and that time pressure tends to worsen the severity of bias even when it does not change its frequency.

AI can also expand the differential, surface rare diagnoses, and reduce certain forms of premature closure. That is a real benefit and it should be named plainly. The concern is not that AI is uniformly harmful to clinical reasoning. The concern is that the physician trained to form their own synthesis now faces a prior synthesis, invisible in its reasoning, authoritative in its presentation, and embedded in the patient's understanding of their own condition before the appointment begins. If the prior synthesis was wrong, the physician must work against the grain of everything the patient believes about themselves to surface the correction. If it was right but incomplete, the physician must identify the gap in a picture that looks complete.

The BMJ has discussed models of "triadic care" for this configuration: clinician, patient, and AI jointly shaping the encounter. That framing is useful but understates the asymmetry. The AI arrived first. It shaped the patient's understanding before the clinician entered the room. The triad has a prior.

What medicine does not yet have is a framework for how a physician should reason in the presence of a pre-formed AI synthesis. The structured frameworks for incidental imaging findings exist because professional societies recognized that finding-first reasoning without governance was dangerous and built the scaffolding. Nobody has built the equivalent for a patient who arrives with an AI-generated synthesis of their last two years of medical records.

---

## What the signs are telling us

Babinski. Romberg. Chvostek. Trousseau. Brudzinski. Kussmaul.

These are not obscure historical curiosities. They are named clinical signs, each attached to a specific physical observation that required a trained clinician to be present, attentive, and interpreting in real time. Each one was designed as a before-the-test signal. It was the reason the test got ordered, not a confirmation of what the test already found.

The Romberg test detects proprioceptive failure: the patient cannot maintain balance with eyes closed. A physician who notices an abnormal gait, or a patient who reports falls, stands them up, closes their eyes, watches. The test generates the question that imaging will answer. Brudzinski's sign: meningeal irritation causes involuntary hip flexion when the neck is flexed. The sign is why the lumbar puncture is ordered, not a footnote after the CSF results return. Chvostek and Trousseau detect hypocalcemia through physical provocation before a metabolic panel is run. Kussmaul breathing is the visible, audible compensation of a body in severe metabolic acidosis: the physician who recognizes it walks into a room already knowing the direction of the diagnosis. They do not need the pH result to understand the urgency.

Each of these signs embodies the same epistemic structure. The body speaks first. The observation generates the hypothesis. The test answers a question that has already been formed.

In today's clinical environment, these signs are increasingly performed after the fact. The calcium comes back low on a routine panel; the physician taps the cheek. The CT shows ischemic changes; the sole is stroked. The blood gas confirms acidosis; the breathing pattern is documented. The signs are still being performed. Their place in the sequence has shifted.

This is not a failure. It is an adaptation, rational under the constraints of how medicine now operates. When the laboratory result arrives in the EHR before the physician has had time to complete the examination, the sequence naturally reorganizes around the available signal. The machine is faster. The machine is always available. The machine does not require the physician to be in the room.

What is lost in the adaptation is not the diagnostic accuracy of any individual encounter. What is lost is the training of a reasoning process: the iterative practice of forming a hypothesis from physical observation and then testing it. That practice, repeated across thousands of patients over years of training, is how a physician learns to think before the result arrives. If the result always arrives first, the practice forms differently, and potentially less robustly.

The resident who performs Babinski after the CT is not a worse physician than one who might have performed it before. But they are training a different skill: interpreting a result in context, rather than forming a question from observation. Those are related skills. They are not the same skill. And the second one, the one being trained less, is the one that catches what the machine did not look for.

---

## The lag that nobody has addressed

Three disruptions have reshaped the conditions of clinical reasoning. The pre-COVID erosion of bedside teaching removed the physical examination from the center of training. Telehealth decoupled the physician from the patient's body and restructured the encounter around history, escalation decisions, and remote data. Consumer health AI has introduced a pre-formed synthesis into the consultation before the physician has formed their own.

Each disruption changed the information conditions of diagnosis. None of them produced a formal successor to the reasoning model that was being disrupted.

The AAMC created telehealth competency domains. Medical schools built virtual OSCE assessments. Professional societies issued guidance on diagnostic safety in virtual care. All of this is real and useful. None of it constitutes a new clinical epistemology. It is accommodation around a hollowing structure.

The clinical encounter still runs, formally, on the hypothetico-deductive model: symptoms generate a differential, tests validate or rule out its items, the physician synthesizes raw signal into meaning. That model was designed for a world where the physician had privileged access to the patient's body and was the first interpreter of their condition. Neither of those conditions reliably holds anymore.

The specialty variation makes this sharper. In ophthalmology, where the slit lamp was always primary, AI augmentation extends an instrument that was already the main tool. The disruption is additive. In internal medicine, where the history and physical were foundational, AI augmentation potentially substitutes for the reasoning that those tools were meant to train. The disruption is structural. The difference matters for how each discipline will need to respond.

In radiology, where finding-first medicine was already native, consumer health AI represents a different kind of threat: the proliferation of finding-first encounters beyond the bounded institutional contexts where structured response frameworks exist. Radiology built its incidentaloma frameworks over decades, with professional society oversight, named authorship, and defined management pathways. Consumer AI generates finding-first encounters at population scale, across every organ system, without any of that scaffolding. The scale is new. The governance is absent.

The framework gap is not a technical problem. The technology exists. The gap is a governance and design problem: who decides what the appropriate response pathway is when a finding arrives pre-interpreted by a consumer AI product? Who has standing to build that framework? The fact that nobody has clearly claimed the responsibility is itself a finding worth naming.

---

One physician who recognized this tension early was Professor Jacob Bar-Ziv, a radiologist at a major Israeli teaching hospital. He refused to read a study without a full clinical history. He would not look at a film until he understood why it had been ordered, what the referring physician suspected, what the patient had reported. In a discipline that had structurally removed the body from the reasoning process, he insisted on reconstructing it from context before he engaged with the image.

That insistence was already countercultural in his time. Radiology had been moving toward the image as the primary object for decades, the clinical history a courtesy field on the requisition form that busy radiologists learned to read in seconds or skip entirely. His students found it slow. They found it inconvenient. They also found, over time, that it made them better diagnosticians, because it trained the habit of forming a question before reading an answer.

The system that replaced him runs differently. Digital imaging made remote reading possible, then economically rational, then dominant. Teleradiology services now cover overnight shifts, rural hospitals, overflow volume. A chest CT ordered in a hospital in London may be read by a radiologist in Mumbai or Phoenix. The report arrives in the EHR before the ordering physician has left the floor. The image has been interpreted. The clinical history, if it was entered at all, was a text field in a requisition form.

Now add the next layer. AI reads the image first. Not as a second opinion, not as a flag for the radiologist to verify, but as the first pass: the system that processes the scan, identifies the findings, assigns preliminary classifications, and presents the radiologist with a pre-structured report to review and sign. The radiologist is no longer the first interpreter. They are the auditor of an interpretation they did not form, produced by a system they did not train, about a patient they have never met, whose history they may not have read, in a hospital they will never visit.

Bar-Ziv insisted on the full clinical context because he understood that a finding means different things depending on the question that preceded it. The same shadow on a film is a post-inflammatory scar in a patient who had TB at twenty and a malignant nodule requiring biopsy in a patient with a smoking history and unexplained weight loss. The image does not contain that difference. The context does.

The current architecture has removed the context from one end and the presence from the other. The AI that reads first has no patient in front of it. The radiologist who reviews second may be in a different time zone. The ordering physician who receives the report may not have been present for either step. What Bar-Ziv understood as inseparable, the clinical question and the image that answered it, has been distributed across three parties, two of whom have never been in the same room as the patient, and one of whom is not a person at all.

That is not a failure of any individual in the chain. It is the logical endpoint of a system optimized for throughput and coverage, where the integration of context with image, the thing Bar-Ziv refused to separate, was never assigned to anyone.

Babinski. Romberg. Chvostek. Trousseau. Brudzinski. Kussmaul.

These names are not yet archaic. Ask any senior physician and they will recite the signs without hesitation. But ask when they last performed one before the result was already in, before the CT had returned, before the lab had flagged the abnormal, before the AI summary had framed the clinical picture, and the answer will be more complicated.

The signs still work. The sequence that gave them their meaning is the thing that is quietly disappearing.

---

*This article is part of an ongoing series exploring how AI is integrating into medical practice and the systems built around it.*
