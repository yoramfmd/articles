---
title: The Blueprint Was Already There
slug: the-blueprint-was-already-there
published: 2026-03-05
excerpt: This week I read three papers that made me happy. JAMA. NEJM. Nature Medicine. All randomized trials. All showing AI outperforming standard care. Then I read the methodology. None of them LLMs. The AI winning in top journals in 2026 was built before the hype cycle. The blueprint was always there.
url: https://data-decisions-and-clinics.com/the-blueprint-was-already-there/
tags: Healthcare AI
source: ghost-api-pull-2026-08-04
---

This week I read three papers that made me genuinely happy.

JAMA published the results of the PETRUSHKA trial: an AI system that personalizes antidepressant selection for patients with Major Depressive Disorder, reducing treatment failures compared to standard care. NEJM Catalyst published a validation of a machine learning model predicting hospital admissions for patients with End-Stage Kidney Disease seven days out, driving an 8% reduction in hospitalizations through targeted nurse intervention. Nature Medicine published a foundation model for haploidentical bone marrow transplant outcomes that outperformed every established clinical risk index for patient stratification.

Three papers. Three randomized studies. Real patients. Measurable outcomes. I have spent months writing about where healthcare AI fails. Reading these felt like the other side of that argument finally showing up in print.

Then I read the methodology sections.

PETRUSHKA is not an LLM. It is a meta-learner, an ensemble combining statistical and machine learning models trained on structured phenotypic data. The team published the trial protocol in 2019. The methodology paper appeared in BMC Psychiatry in 2022. The ESKD system runs two ML models on structured EMR data. The transplant model is gradient boosting with explainable AI techniques.

None of these systems have anything to do with the current wave of generative AI. They were conceived before ChatGPT existed. The AI appearing in top journals in 2026 as proof of progress was built in a completely different technological era.

My happiness didn't go away. But it changed shape. Because I recognized what I was looking at.

---

Walk into any modern hospital and you are already surrounded by some of the most sophisticated AI deployed in any industry. You just don't see it as AI because it doesn't announce itself.

Aidoc and Viz.ai scan CT images the moment they are acquired and flag hemorrhages, pulmonary emboli, and large vessel occlusions before a radiologist has opened the queue. Paige AI and PathAI analyze pathology slides for tumor detection and biomarker quantification with a consistency no human eye can match at volume. The Edwards Hypotension Prediction Index reads the shape of an arterial pressure waveform and tells the anesthesiologist, fifteen minutes in advance, that blood pressure is about to drop. Epic's deterioration indices watch vitals, labs, nursing notes, and telemetry simultaneously and fire when the trajectory turns dangerous. Nuance DAX listens to the clinical encounter and produces a structured note before the physician has left the room.

This is not a list of experiments. This is Tuesday morning in a modern hospital system.

The AI is already embedded in mission-critical workflows. Remove the Aidoc triage and the radiology queue reorganizes. Remove the sepsis model and the nursing response changes. Remove the HPI and the anesthesiologist loses a signal she now depends on to stay ahead of the physiology. These tools are not pilots. They are infrastructure. Healthcare AI is no longer a question of adoption. It is a question of what gets built on top of what is already there.

What most people writing about the "AI revolution in healthcare" have missed is that the revolution already happened. It happened quietly, over forty years, one narrow validated tool at a time. And the reason most clinicians don't think of it as AI is precisely why it worked.

---

Look at what every successful implementation has in common. Not just technically, but as a product.

A physician looking at the Edwards HPI sees a monitoring tool that predicts hypotension. A product manager looking at the same system sees something built on four answered questions before a line of code was written. Who is the user: the anesthesiologist, not the patient, not the administrator. What is the specific pain: hypotensive events are common and consequential, and by the time the number drops on the monitor the event is already underway. What does success look like in a number: reduction in intraoperative hypotension, measured prospectively across thousands of patients. What breaks if it doesn't work: a clinical team that has built workflows around the signal and now depends on it. Both readings are correct. The second is why the first was possible.

Viz.ai's stroke platform follows the same architecture. The use-case is not "improve stroke outcomes." It is specific: detect large vessel occlusion on CT angiography and alert the stroke team before the radiologist opens the queue. The pain point is not abstract. Time is brain: 1.9 million neurons die every minute of untreated stroke, and radiology queues do not automatically prioritize stroke studies. The measurable benefit is door-to-treatment time, tracked in minutes, with mortality and disability outcomes that follow directly. The target persona is the interventional radiologist and the stroke team, people who need to move fast and must trust the flag they are responding to.

PETRUSHKA is the same logic applied to psychiatry. The pain point is documented: roughly half of patients prescribed antidepressants for Major Depressive Disorder do not respond adequately to their first medication. The current approach is trial and error, sometimes taking years to find an effective treatment while the patient suffers each failed attempt. The use-case is not "improve depression outcomes." It is: match the patient to the right medication at first prescription, using structured phenotypic data, with the clinician making the final call. The target persona is the prescribing psychiatrist. The measurable benefit is reduction in treatment discontinuation. Defined. Tracked. Published.

The pattern is not just narrow scope. It is product discipline applied before the technology was built. A specific user with a specific pain. A specific intervention with a specific measurable outcome. Accountability sitting with a trained clinician who can override, escalate, or discard the recommendation.

This is what the pre-LLM systems got right. Not just the algorithm. The product thinking underneath it. And it is exactly what the current wave, in its race to deploy the most agents to the widest audience, keeps skipping.

---

Every major technology wave of the last thirty years has followed the same arc. Y2K, dot-com, SOA, Hadoop, cloud, IoT: a genuine capability arrives, investors and competitors pile in, timelines compress, and the shortcuts that were unthinkable twelve months earlier become table stakes. Nobody makes a conscious decision to skip the validation work. The environment simply makes the slower path look like a competitive disadvantage.

I have watched this from both sides: as a physician who trained on systems built with rigor, and as a product manager who has sat in rooms where the pressure to ship was real and the patience for clinical trials was not. The people who cut corners in the current wave are not reckless. They are operating in an environment where the hype cycle has inverted the normal relationship between evidence and deployment. Launch first. Validate later. If you don't, someone else will.

The result is visible in data published the same week as the three RCTs that made me happy.

A Nature Medicine study tested real patients using GPT-4o, Llama 3, and Command R+ to assess clinical scenarios and decide on a course of action. The models, tested alone, correctly identified the relevant medical condition in 94.9% of cases. Real patients using those same models scored 34.5%. The control group, with no AI at all, outperformed the AI-assisted group by a factor of 1.76.

Same journals. Same week. Opposite results.

The difference is not the underlying technology. It is three things that changed simultaneously when generative AI entered healthcare: the target user shifted from clinician to patient, the input shifted from structured domain data to unstructured natural language from someone anxious at 11pm, and the validation approach shifted from clinical trials to benchmark scores on medical licensing exams. The model that scored 94.9% in isolation scored 34.5% when a real person was the interface. The model didn't change. The deployment context did.

The pre-LLM systems never faced that context. They never had to. They were designed for the person who would be accountable if they were wrong, which was always a trained clinician, never a patient alone at home.

---

Here is what I keep coming back to.

The hospital is already full of AI that works. It works because it was built by people who understood the clinical workflow, designed for the person who would use it, validated slowly enough to know what they had, and deployed narrowly enough that failure was recoverable. The knowledge of how to do this is not theoretical. It is in production, running in hospitals, producing outcomes documented in the clinical literature.

We are at a turning point. Not the beginning of AI in healthcare. The beginning of the second layer. And the risk of the second layer is not that the technology is insufficient. The risk is that the people building it are in too much of a hurry to read what the first layer already wrote down.

PETRUSHKA was designed in 2019. The people who built it had no idea what 2024 would look like. They picked a narrow problem, designed for the clinician, structured their inputs, ran the trial across three countries for six years, and published in JAMA. It worked.

The blueprint for how to do this right was never missing. It has been running in hospitals for decades, embedded in equipment, invisible to anyone who wasn't looking for it.

The AI is already in the walls.

The only question is whether the people building the next layer have read the blueprints.

---

*Sources: Bean et al., "Reliability of LLMs as medical assistants for the general public," Nature Medicine, 2026. PETRUSHKA trial, JAMA, March 4, 2026 (protocol: Evidence Based Mental Health, 2020; methodology: BMC Psychiatry, 2022). ESKD hospitalization prediction, NEJM Catalyst, March 2026. Haploidentical transplant foundation model, npj Digital Medicine, March 2026.*
