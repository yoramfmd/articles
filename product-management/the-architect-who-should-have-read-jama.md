---
title: "The Architect Who Should Have Read JAMA"
slug: the-architect-who-should-have-read-jama
published_at: 2026-02-27T01:20:00.000Z
custom_excerpt: "In healthcare AI, policy shifts now appear first in journals like JAMA and NEJM, then quietly become grant conditions and RFP requirements. Many tech teams miss this signal. The winners will be those who translate medical literature into architecture before it becomes mandatory."
tags: [pm]
feature_image: https://storage.ghost.io/c/e6/05/e605b234-3cc8-4fe4-97bb-2bb55b18b8fb/content/images/2026/02/ChatGPT-Image-Feb-17--2026--11_05_17-PM.png
source: ghost
---

There is a meeting that happens regularly in healthcare technology companies, and it almost always ends the same way.

A cloud architect presents a well-designed system: HIPAA-compliant storage, OAuth 2.0 authentication, a FHIR API layer, solid audit logging. The security team nods. The engineering lead nods. 

Then someone from the clinical side of the table says something like this:

"I was reading last month's issue of NEJM AI. There's a paper on ambient scribe deployment that describes a governance framework hospitals are expected to implement when they adopt AI tools. It includes a validation dashboard and a protocol for detecting model degradation. Does our platform support that?"

Silence. Not because the architect didn't think about governance. Because the clinical person is holding a peer-reviewed paper as a de facto requirements document, and the architect has never seen it.

This is the gap that is widening in healthcare AI. And it has a specific, underappreciated cause.

---

### The Pattern Nobody Is Monitoring

In March 2025, JAMA published an article co-authored by the FDA Commissioner, the CDC Director, the NIH Director, and the National Coordinator for Health IT. It described three federally mandated building blocks for US healthcare data exchange: USCDI, FHIR, and TEFCA. Buried in the table near the end was a single row that most technology teams missed entirely"

*The ARPA-H PRECISE-AI program, which funds AI model degradation monitoring at hospitals, explicitly requires that all solutions adhere to FHIR, USCDI, and TEFCA standards. Not as a preference. As a grant condition.*

This means a federally funded hospital cannot use your AI monitoring platform if it does not support those standards. That requirement did not exist two years ago. It exists now because of a policy decision announced in a clinical journal that most cloud architects never saw.

Let that sink in for a moment.

This is the pattern: policy intent appears in medical literature. It enters federal grant conditions and accreditation requirements. It lands in hospital RFPs twelve to eighteen months later. The architects who built systems in 2023 without FHIR-native interfaces are now facing expensive retrofits. The architects who read the JAMA table in 2025 can design for 2027 requirements today.

JAMA is not the only source. In February 2025, BMJ published FUTURE-AI, a consensus framework from 117 experts across 50 countries establishing six principles for trustworthy clinical AI: Fairness, Universality, Traceability, Usability, Robustness, and Explainability. The Joint Commission and the Coalition for Health AI are already referencing it when defining responsible AI deployment. NEJM AI published a pragmatic trial framework for ambient AI governance that health systems are using to write procurement requirements. Nature Medicine published a perspective arguing that medical AI models must demonstrate the ability to adapt across populations and care settings without retraining, establishing "context switching" as an emerging standard for what deployable AI must do.

None of these appeared in the AWS architecture blog. None were in a vendor whitepaper. They were in clinical journals, written for CMIOs and clinical informaticists, with a direct pipeline into the RFPs your sales team will see next year.

---

### What This Means for Your Architecture

The literature problem sits on top of technical challenges that are already under appreciated. Three of them matter most.

**Syntactic interoperability is not semantic interoperability.** FHIR solves the packaging problem. Two hospitals can both send data in FHIR format and still produce incompatible data for AI training, because one maps hemoglobin to LOINC at the assay level and the other at the panel level, because one captures units in g/dL and another in mmol/L, because local coding practices introduce variation that no exchange standard eliminates. The JAMA DHHS article acknowledged this directly: even when the building blocks function as intended, "data may not have the same meaning in the receiving system as it did in the sending one." Solving this requires a semantic harmonization layer above FHIR. Most architectures don't have one.

**You need two data models, not one.** FHIR is optimized for real-time patient-level exchange. OMOP is optimized for population-level analytics and AI model training. They are complementary, not competing, but reconciling them requires deliberate design in your canonical data layer. The decision about how you normalize and store data at ingestion determines whether both are achievable. Treating this as a later problem is how you end up with a FHIR server that cannot feed a training pipeline and an OMOP warehouse that cannot support real-time clinical decision support.

**Provenance is a clinical requirement, not just a compliance checkbox.** When an AI system influences a clinical decision, the organization needs to trace the chain from source data through transformation through inference. FHIR has a Provenance resource for exactly this. Designing for it from the start is straightforward. Retrofitting it into a running data pipeline is not.

---

### What the JAMA Article Actually Requires of Your Platform

1. For architects who want to move from principle to checklist, the JAMA DHHS article is more specific than its abstract suggests. Reading it as a requirements document, rather than a policy statement, produces the following obligations for any platform operating in the US healthcare market.

2. The platform must ingest, store, expose, and exchange all USCDI-defined data elements using standardized mechanisms. This is the data layer baseline: demographics, vitals, medications, diagnoses, lab results, all accessible through structured, standardized requests.

3. The system must support FHIR-based APIs aligned to the US Core Implementation Guide for representation and exchange of those data elements. FHIR compliance alone is not sufficient. The Implementation Guide specifies exactly how USCDI elements are expressed as FHIR profiles, and alignment to it is what makes data meaningful across institutions, not just technically transferable.

4. The platform must enable interoperability with TEFCA-aligned nationwide health information exchange networks to support secure, authorized data exchange. This is the network layer requirement. Supporting FHIR internally is not enough if the platform cannot connect to the trust fabric through which hospitals actually exchange data at scale.

5. The architecture must support extensibility for USCDI+ domain-specific implementation guides, including research, oncology, quality measurement, and public health domains. USCDI is a minimum baseline. USCDI+ is where specific use cases, cancer staging, clinical trial data extraction, public health reporting, are being defined. A platform that cannot extend to these domains will be excluded from an expanding set of federally funded programs.

6. The system must support secure data exchange that protects patient privacy and improves data security in alignment with federal interoperability standards. Privacy and security are not a separate workstream. They are a property of the exchange layer itself.

7. The platform must support standardized extraction and exchange of health data for secondary uses including scientific research, public health, quality improvement, and care coordination. This is the AI and analytics requirement stated in federal language. The same data infrastructure that supports clinical care must also support the research and population health use cases that AI models depend on.

8. Finally, the system must align interoperability components with DHHS Health IT alignment policies, federal rulemaking, and federally endorsed standards where applicable. This is the future-proofing requirement. Standards will evolve. USCDI is updated annually. TEFCA is expanding to include research use cases. A platform that treats its current compliance posture as permanent will fall out of alignment as the building blocks develop.

None of these requirements appear in a vendor certification checklist. They are distributed across a JAMA article, a federal rule-making notice, and a grant program specification. That is precisely the point.

---

### The Enterprise Parallel Nobody Draws

Here is the insight the cloud-native healthcare AI world has largely missed.

The semantic harmonization problem that JAMA identifies is structurally identical to the master data reconciliation problem that enterprise software has solved repeatedly in manufacturing, retail, and finance. When two large companies merge, their ERP systems contain decades of accumulated local codes: different part numbers for the same component, different vendor IDs for the same supplier, different chart of accounts for the same categories. Reconciling them into a unified canonical model is one of the oldest problems in enterprise software. It has established methodology, tooling, and governance frameworks.

Healthcare calls the same problem by different names: LOINC mapping, SNOMED normalization, patient identity matching. The underlying challenge is identical. Two systems that each correctly represent the same real-world concept, producing data that is incompatible for cross-system reasoning.

The architects who recognize this analogy will build better healthcare data platforms than those treating healthcare as a greenfield problem with no prior art. The relevant expertise exists. It lives in a different industry's literature.

---

### What Your Team Actually Needs

The skillset required here is hybrid in a way that has no clean precedent. You need someone who reads JAMA the way a regulatory affairs team reads FDA draft guidance: scanning for early signals of requirements that will become mandatory. Not a clinician, necessarily, though clinical knowledge helps. A product intelligence function applied to an unusual source.

You need someone who understands that a SNOMED CT hierarchy is a reasoning substrate, not a lookup table, and that how you store and traverse it determines whether your AI agents can perform clinical inference or only keyword matching.

You need someone who can look at a FHIR Provenance resource and a master data governance framework from an ERP implementation and recognize they are solving the same problem at different abstraction levels.

That role does not yet have a job title. It is emerging at the intersection of clinical informatics, enterprise data architecture, and product management. Healthcare technology teams that find a way to create it, whether as a dedicated hire, a structured collaboration between clinical and engineering functions, or a product manager who commits to reading outside their usual sources, will have a meaningful advantage over those that don't.

Building healthcare AI infrastructure is hard not because the technology is intractable, but because the requirements come from more places, in more languages, with more consequence for errors, than almost any other domain in software.

The architects who understand that JAMA is part of their reading list will build systems that are compliant before compliance is required. The ones who don't will keep being surprised by requirements they should have seen coming.

---

### References

1. Abbasi AB, Layden J, Gordon W, et al. A Unified Approach to Health Data Exchange: A Report From the US DHHS. *JAMA.* 2025;333(12):1074-1079. doi:10.1001/jama.2025.0068

2. FUTURE-AI Consortium. FUTURE-AI: international consensus guideline for trustworthy and deployable artificial intelligence in healthcare. *BMJ.* 2025;388:e081554. doi:10.1136/bmj-2024-081554

3. Afshar M, Resnik F, Baumann MR, et al. A Novel Playbook for Pragmatic Trial Operations to Monitor and Evaluate Ambient Artificial Intelligence in Clinical Practice. *NEJM AI.* 2025;2(9). doi:10.1056/AIdbp2401267

4. Koret R, Bhatt DL, Bhattacharya J, et al. Scaling medical AI across clinical contexts. *Nature Medicine.* 2025. doi:10.1038/s41591-025-04184-7

5. Advanced Research Projects Agency for Health (ARPA-H). PRECISE-AI: Performance and Reliability Evaluation for Continuous Modifications and Useability of Artificial Intelligence. Program requirements available at: [https://arpa-h.gov](https://arpa-h.gov/)

6. US Department of Health and Human Services. DHHS Data Strategy and 2024-2030 Federal Health IT Strategic Plan. Referenced in: Abbasi et al., *JAMA* 2025.