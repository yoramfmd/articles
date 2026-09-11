---
title: Not a Revolution. A Diagnosis
slug: not-a-revolution-a-diagnosis
published: 2026-03-14
excerpt: Two studies this week, one from Google and one from Microsoft, are being celebrated as evidence that healthcare AI has arrived. Read them together and they reveal something more uncomfortable: AI is filling a gap that healthcare created long before any of us started building AI for health.
url: https://data-decisions-and-clinics.com/not-a-revolution-a-diagnosis/
tags: Healthcare AI
source: ghost-api-pull-2026-08-04
---

---

Two studies landed this week. Both are being celebrated in my feed. One from Google, one from Microsoft. Both are worth reading carefully, because together they are saying something the headlines are mostly missing.

Google published the results of a first-of-its-kind prospective clinical study at Beth Israel Deaconess Medical Center. Their conversational medical AI, AMIE, conducted pre-visit clinical history taking with 100 patients before their primary care appointments. Zero safety stops from supervising physicians. Differential diagnoses rated on par with treating PCPs by blinded clinical evaluators. The final diagnosis was in AMIE's top seven possibilities in 90% of cases.

Microsoft published an analysis of over 500,000 health conversations people had with Copilot in January 2026. Symptom questions spike at night. Emotional wellbeing queries rise after hours. On mobile, people ask about symptoms at twice the rate they do on desktop. One in seven symptom conversations is on behalf of someone else, a child, a parent, a partner.

Everyone is discussing the AMIE diagnostic accuracy numbers. Some are noting the scale of Microsoft's data. Very few are asking what these two studies reveal when you read them together.

### What the Microsoft Data Is Actually Saying

The Microsoft report includes one sentence that deserves more attention than it is getting: people turn to AI when they cannot easily reach a clinician, a pharmacist, or even friends and family.

That sentence is not a celebration of AI capability. It is a description of healthcare failure.

Primary care reimbursement does not pay for the 11pm call. It pays for the scheduled visit. After-hours coverage gets routed to outsourced triage lines or emergency departments. Most health systems have not built the infrastructure to be present where their patients actually are, at the hours they actually get sick. The nocturnal gap is not an oversight. It is the predictable result of how we designed and paid for the system.

I have been on both sides of this corridor: years practicing medicine, then years building enterprise software for healthcare organizations. In both, I saw the same pattern: people do not turn to inferior substitutes when better options are available. They turn to inferior substitutes when better options are absent. The person asking Copilot about their child's fever at 11pm is not choosing AI over their pediatrician. Their pediatrician is not available at 11pm.

I have lived that search. My son had a well-documented preference for getting sick at midnight, with a particular fondness for federal holidays. What you reach for at those hours is not your pediatrician. It is whatever is available.

The nocturnal pattern in the Microsoft data is not a feature of AI adoption. It is a symptom of a healthcare system that has operating hours. The caregiver asking about an aging parent's medication at midnight is not an edge case. She is the norm. One in seven symptom conversations in the Microsoft data is on behalf of someone else.

The demand was already there. It existed before any of us started building AI for health. What changed is that now there is something to absorb that demand, however imperfectly.

### What the Google Data Is Actually Showing

The AMIE study is the more rigorous piece of science. It will also be the most misread.

The headline numbers are real. Zero safety stops. Diagnostic quality on par with PCPs by blinded evaluation. Patient trust increasing after the interaction, not decreasing. Pre-registration, IRB approval, prospective design. This is more methodological rigor than most of what passes for clinical AI evidence.

But the finding I keep thinking about is not the diagnostic accuracy. It is this: PCPs who reviewed AMIE's pre-visit transcripts said it shifted the visit dynamic from data gathering to data verification.

I remember my pre-anesthesia assessment meetings at the clinic. The first fifteen minutes of almost any appointment are consumed by history the patient has told before, in some form, to some other provider. AMIE did that work beforehand. The physician arrived knowing what was already known and could spend the appointment on what actually required clinical judgment.

That is a different argument than "AI matches physician accuracy." It is an argument about what physicians should be spending their time on. History taking at scale is not where physician cognitive load belongs. Integrating ambiguous findings, weighing competing diagnoses in a patient you can see and examine, deciding what is worth investigating and what is not: that is where it belongs.

AMIE had no EHR access, no physical exam, no visual assessment of the patient. PCPs outperformed it on the practicality and cost-effectiveness of management plans. The study authors note this directly. What was demonstrated is not that AI can replace the clinical encounter. It is that AI can do useful preparatory work before the clinical encounter, in a supervised setting, for non-emergency episodic presentations.

That scope matters. Not because it diminishes the result. Because it defines what actually needs to happen next.

### The Gap Between the Two Studies

Microsoft mapped the demand: millions of conversations, in the hours when healthcare isn't available, for conditions and situations where people have run out of other options.

Google mapped a controlled proof of concept: what supervised conversational AI can do in a specific, favorable clinical scenario.

The distance between those two things is the entire challenge.

If you are running a health system, the question this week's data forces is not which AI vendor to evaluate. It is whether you are comfortable letting AI absorb demand your organization was never designed, staffed, or paid to meet.

The 11pm mobile query from a caregiver about an aging parent's symptoms is not a supervised pre-visit chat at an academic medical center. It has no physician watching in real time. It has no safety stop protocol. The patient may not be described accurately. The symptom may not be a new episodic complaint. The clinical stakes may look nothing like what AMIE was tested on.

I have been in enough product roadmap meetings to recognize what happens next. Someone takes the 90% accuracy figure and assumes it generalizes. It does not generalize automatically. It generalizes when someone does the rigorous work of validating it in the conditions where the actual demand exists.

Those conditions are harder. They are less controlled. They are exactly the conditions Microsoft just documented: night, mobile, caregiver, alone, no professional in the room.

The question is not whether AI will fill those gaps. It already is. The question is whether we will build it for the conditions that actually exist, rather than the conditions that make for good benchmark numbers.

We have never been short of impressive benchmark numbers. We have always been short of systems built for the 11pm caregiver who has already tried everything else.

---

**References:**

Schaekermann M, Karthikesalingam A et al., "A prospective clinical feasibility study of a conversational diagnostic AI in an ambulatory primary care clinic," Google Research / Beth Israel Deaconess Medical Center, published March 11, 2026. [https://research.google/blog/exploring-the-feasibility-of-conversational-diagnostic-ai-in-a-real-world-clinical-study/](https://research.google/blog/exploring-the-feasibility-of-conversational-diagnostic-ai-in-a-real-world-clinical-study/)

Tolmachev P, Costa-Gomes B, Sounderajah V, "Health Check: How People Use Copilot for Health," Microsoft AI, published March 10, 2026. [https://microsoft.ai/news/health-check-how-people-use-copilot-for-health/](https://microsoft.ai/news/health-check-how-people-use-copilot-for-health/)
