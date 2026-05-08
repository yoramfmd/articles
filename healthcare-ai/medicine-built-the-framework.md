# Medicine Built the Framework. Just Not for This.

In 2005, the Fleischner Society published guidelines for managing incidental pulmonary nodules. A nodule found on a chest CT ordered for something else entirely (a pre-op workup, a trauma scan, a PE rule-out) now had a structured response pathway. Nodule size, solid versus subsolid character, patient risk factors: each combination mapped to a defined management recommendation. Follow up in three months. Biopsy now. Discharge with reassurance. The framework converted a finding-without-context into a clinical action with accountability attached.

It took years to build. It has named authors, a named professional society, a bounded scope, and a versioned update history. When the 2017 revision superseded the 2005 version, it said so explicitly, cited what changed and why, and gave clinicians a clear handoff point.

Medicine repeated this work for thyroid nodules (Bethesda, 2007). For screening lung CT (Lung-RADS, 2014). For adrenal, renal, hepatic, and pancreatic incidentalomas (the ACR Incidental Findings white paper series). Each framework exists because the profession recognized a specific problem: when a finding arrives without a prior hypothesis, clinicians manage it inconsistently, and inconsistency at scale produces harm. The solution was governance. Structured, accountable, bounded governance.

The profession understood, in other words, that finding-first reasoning is hard. Finding-first reasoning is what happens when a clinical discovery precedes the question that would have generated it: the finding arrives without a prior hypothesis, and the clinician must construct the response from scratch. It built the scaffolding carefully.

---

Now consider what consumer health AI is deploying, and why it raises the same governance problem medicine already solved once, at a scale and scope those frameworks were never designed to handle.

A patient syncs their medical records to a health coaching app. The app synthesizes two years of labs, imaging, wearable data, and clinical notes into a personalized summary. The summary identifies patterns, flags changes, and suggests follow-up. The patient arrives at their next appointment carrying that synthesis as their primary frame for understanding their own health.

This is finding-first reasoning at consumer scale. The finding, or rather the interpretation of dozens of findings, arrives before any clinical hypothesis has been formed. The physician receives a pre-processed output and must now reason about the model's interpretation of the patient's data rather than the data itself.

Every structured response framework medicine built for incidental findings shares five properties: named authorship from a professional body, bounded scope covering one class of finding, codified risk modifiers derived from published evidence, a management pathway as output rather than an interpretation, and a public versioning history so clinicians know what changed and when.

The consumer AI synthesis pattern generally meets none of them. No named professional body. Unbounded scope across the entire medical record. Risk weighting that is opaque and continuously updated without public documentation. Output that is framed as interpretation and recommendation, not as a management pathway with explicit thresholds. No version history visible to the receiving clinician. Some FDA-regulated tools carry manufacturer labeling and change-control documentation, but that is regulatory compliance, not the clinician-facing governance structure that Fleischner and Bethesda represent. The gap is specifically the absence of a professional-society-driven framework a physician can actually use at the bedside.

This is not a criticism of the technology. The Fleischner guidelines are not more rigorous because pulmonary nodules are more important than the patterns a health AI surfaces. They are more rigorous because a professional society decided that rigor was required and did the work. Nobody has made that decision for consumer health AI synthesis.

---

The governance gap is not symmetrical across use cases. A wearable that flags a possible arrhythmia and routes the patient to a physician is operating close to how Lung-RADS operates: a screening-derived finding, a defined next step, a bounded clinical question. The framework analogy holds reasonably well, even if no equivalent professional body has formally built it.

A platform that synthesizes a patient's complete medical record, wearable data, and health history into a continuous interpretive layer is doing something categorically different. Its scope is unbounded. Its output touches every organ system, every prior diagnosis, every medication, every trend. No incidentaloma framework covers that. None was ever designed to.

The question is not whether this technology should exist. Consumer AI health tools, from wearables to coaching apps, already reach tens of millions of users, and an increasing subset is beginning to integrate EHR data into synthesized longitudinal views. The question is who builds the governance framework that makes it safe to receive in a clinical context.

For incidental pulmonary nodules, the Fleischner Society did the work. For screening lung CT, the ACR did the work. For consumer health AI synthesis, no professional society has yet produced the equivalent: a clinician-facing, evidence-based management framework that a physician can actually use when a patient arrives with a synthesized view of their own medical record. The American College of Cardiology has not claimed it. The AMA has not claimed it. The FDA regulates software as a medical device, but regulatory compliance is not the same as clinical guidance, and what is missing is not a product label but a practice standard.

The installed base is growing faster than the standing of any candidate to fill that gap. Medicine has solved this class of problem before. It has not yet decided to solve it again.

---

*This article is part of an ongoing series exploring how AI is integrating into medical practice and the systems built around it.*
