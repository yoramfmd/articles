---
title: Stop Waiting for Clean Data
slug: stop-waiting-for-clean-data
published: 2026-02-25
excerpt: The healthcare data integration problem is 20 years old and not going away. So why are we still building AI that assumes clean data? A case for designing AI that works in the real world, not the one we keep promising to build.
---

### A Case for AI That Works in the Real World

**I've counted HL7 characters by hand.**

I know what a tilde (~) looks like in an EDI document at 2am when the batch job has been failing for three hours and nobody can figure out why. I've built integrations on BizTalk, TIBCO, Software AG, Informatica, IBM MQ, and SAP. I've moved data through fax messages, flat files, web services, OData feeds, ETL pipelines, streaming solutions, and more point-to-point connections than I care to remember. I've sat in rooms with some of the smartest integration architects in the industry, representing some of the most sophisticated technology organizations in the world, and I've watched us collectively pour two decades of serious engineering effort into the healthcare data problem.

I say this not to list credentials. I say it because what comes next needs to be heard from someone who genuinely tried.

The integration problem we did not solve in the past twenty years will not disappear in the next six months. It will not be dissolved by a new standard, a new vendor, a new mandate, or a new wave of AI enthusiasm. Data will not consolidate and harmonize itself magically just because Gartner placed AI at the peak of their hype cycle.

I've spent enough time on both sides of this problem, as a technologist who builds data infrastructure and as a physician who relies on it, to say that clearly and without apology.

It's time to stop waiting. And it's time to ask a different question.

### The Diagnosis: This Was Never Just a Technology Problem

Every generation of integration technology arrived with an implicit promise. BizTalk would finally connect the silos. Then enterprise service buses would. Then iPaaS platforms. Then data lakes. Then data mesh. Then FHIR mandates would force the issue. Each wave produced genuine progress in specific dimensions. None of them resolved the underlying fragmentation.

The reason is simple, and we don't say it loudly enough: **this is not primarily a technology problem.**

It is a structural problem. A competitive problem. An economic problem. A governance problem that happens to wear a technology costume.

Epic has no compelling business reason to make data easy to move to a competitor. A specialty practice operating on thin margins has no budget to rebuild integrations that technically function, even if they're brittle. A regional health system with a decade-long capital roadmap has higher priorities than harmonizing terminologies that nobody is currently complaining about. A few organizations have approached this with unified governance and sustained investment. Kaiser Permanente is the canonical example. The VA has historically operated at national scale under unified governance, even as it navigates a complex EHR modernization. These are the exceptions, not the template.

We solved the syntax problem repeatedly. We evolved the interface layer, HL7 v2 for messages, C-CDA for documents, and increasingly FHIR for APIs. Each improved something. None changed the incentives. And all three still coexist in production today, because new standards in healthcare add layers, they rarely replace what came before. A well-structured FHIR resource that exists in theory but is inaccessible in practice due to policy, business terms, or implementation friction is not interoperability. It is well-formatted isolation.

The diagnosis is that we have been treating a structural disease with technical medicine. The treatment helps at the margins. It does not cure the underlying condition.

### The Prognosis: Point-to-Point Is Here to Stay

Let me be direct about what the next several years will actually look like, not in an analyst report, but on the ground.

The community hospital down the street from you is still running three EHR versions. Their lab system still fires HL7 v2 messages. Their imaging archive still speaks DICOM over a proprietary connection. Their billing system exists in a world FHIR has never touched. This is not an edge case. Many organizations run mixed generations of systems, HL7 v2 feeds, and interfaces that predate modern APIs by a decade or more.

Regulation will help at the margins. The 21st Century Cures Act, information blocking rules, and TEFCA, which is designed to scale nationwide exchange across networks through a staged rollout, represent meaningful steps and deserve credit. They will gradually raise the floor. They will not transform the ceiling, and they move at the speed of federal rulemaking, implementation guidance, and enforcement appetite, which is to say, slowly.

AI will not fix fragmentation as a side effect of being deployed. If anything, the current wave of AI pilots is making the depth of the problem more visible than any audit ever did. When a model underperforms, teams finally go looking at what it was actually reasoning on, and what they find is sobering. Missing labs. Stale medication lists. Diagnoses coded for billing accuracy rather than clinical accuracy. Gaps that have existed for years, invisible until something tried to act on them.

The prognosis is not that nothing will improve. Incremental progress is real and worth pursuing. But the gap between where we are and the harmonized data foundation that most healthcare AI implicitly assumes will not close in the next six months, or the next two years, or possibly in the next decade for the majority of healthcare organizations operating outside of integrated systems.

That is not a reason for despair. It is a reason to stop building AI that requires a foundation we don't have.

The question is no longer *when will the data be ready for AI?*

The question is *what do we build on the foundation we actually have?*

### The PoC Trap: Where the Problem Gets Expensive

Here is something that doesn't get said loudly enough. The data fragmentation problem is not just a foundation problem. It is actively destroying value right now, in ways that don't show up in strategy decks.

Across the industry, healthcare AI pilots are succeeding in controlled conditions and then collapsing at production. The clean, curated dataset that made the demo sing does not exist in the community hospital. The model that performed beautifully on Epic's Cosmos dataset meets a three-EHR environment with a legacy lab system, a billing platform from 2009, and a pharmacy feed that goes down on weekends. So the implementation team builds local adaptations. Custom mappings. Workarounds for missing fields. Fallback logic for when the FHIR endpoint returns nothing useful.

Each of those adaptations is an integration project. Each integration project is also an expense that was allocated, debated, and quietly cancelled a decade ago, because nobody in the C-suite wants to fund plumbing. Integration work has never been glamorous enough to survive a budget cycle when there are shinier priorities in the room. And now every dollar in the building is chasing AI. Find me the CFO and COO who will stand up in the next planning meeting and say: before we scale our AI program, we need to fund the underlying data infrastructure it depends on. That person does not exist in most organizations, and everyone in the room knows it. So the integration debt accumulates silently, and the AI program sits on top of it, and nobody connects the two until the pilot fails in production.

This is the part nobody wants to say out loud in the boardroom: deploying AI on top of fragmented infrastructure, without addressing the fragmentation, does not reduce technical debt. It adds to it. The PoC becomes a production system that requires its own integration team, its own exception handling, its own version of the same point-to-point connections we already have. We have not escaped the problem. We have rebranded it.

This is not a reason to stop building. It is a reason to build differently, with honest expectations, and with architectures that treat fragmentation as a permanent condition rather than a temporary inconvenience.

### A Spectrum of Alternatives: From the Practical to the Speculative

I want to be clear about what this section is and is not. It is not a roadmap. It is not a recommendation. I do not believe one solution exists, and I do not believe the same solution applies to every care delivery context. Some of these ideas are buildable today. Some require structural or regulatory shifts that may take years. Some are deliberately speculative, included not because I think they will happen but because the conversation needs to expand beyond the options currently on the table.

The goal here is not conclusions. The goal is provocation.

**Tier 1: Build differently today**

These directions do not require new standards, new legislation, or new vendor behavior. They require different design choices.

Clinical quorum bundles instead of complete records. A senior physician seeing a new consult does not have a complete longitudinal record. They reason under uncertainty, flag what they don't know, and make a calibrated recommendation. That is not a failure mode. That is medicine. We have held AI to a standard we never applied to clinicians. The alternative is to define, for each specific decision, the minimum coherent evidence set required to act safely. To start a statin, you need age, a recent LDL, cardiovascular risk factors, current medications, and known contraindications. Not 400 fields. Not a full imaging history. Just enough, assembled from whatever sources actually exist.

Coverage-aware AI. We obsess over harmonization. We rarely model visibility. What if every AI output included an explicit coverage report: labs available for the past 18 months, medications for the past 60 days, external pharmacy fills not detected. Models trained with coverage-aware features would degrade gracefully rather than confidently producing wrong answers. In fragmented care, visibility may be more predictive of safety than any single data element.

Decouple retrieval from reasoning. Today most agent architectures tightly couple retrieval, reasoning, and output. An alternative is to separate them: a deterministic retrieval layer, a context assembler that attaches provenance and missingness metadata, and a reasoning engine that sees the data alongside its coverage. The AI never directly queries the EHR. It reasons on a structured, audited context object. That shifts accountability and makes governance tractable.

Purpose-scoped data products. You do not need to harmonize everything to harmonize something. A 30-day readmission product, a medication adherence product, a care gap product, each built from partial sources and governed for its specific use case. The goal is not a perfect lake. The goal is enough coherence for this decision, for this user, under this consent model.

**Tier 2: Change the rules of the game**

These directions require structural or regulatory movement. None of them are guaranteed. All of them are more likely than finishing enterprise harmonization in the next three years.

Pay for data liquidity. We solved e-prescribing not through better XML but through reimbursement pressure. What if CMS quality measures rewarded verifiable data exchange completeness? What if payers offered bonus reimbursement for interoperable event publication? Data movement would accelerate faster than any new API specification.

Certify AI on incomplete data. Today we validate models on curated datasets. What if certification required demonstrated performance under simulated missingness, explicit uncertainty reporting, and cross-EHR degradation testing? We stress test aircraft under turbulence. Changing that certification requirement would change vendor behavior overnight.

Shared infrastructure for identity and terminology. Patient matching is the silent blocker that persists regardless of how elegant the FHIR server is. A nationally trusted, privacy-preserving identity resolution backbone combined with open, consortium-maintained terminology services would not centralize clinical data. It would centralize the glue that makes disparate data joinable.

Contractual interoperability as a procurement lever. Health systems could include no-data-blocking clauses, real-time API access requirements, and export SLAs in every vendor contract. Renewal contingent on measurable data exchange performance. This attacks the economic incentive problem directly, using purchasing power that already exists.

**Tier 3: The uncomfortable and the speculative**

These ideas may be wrong. Some may only make sense in specific contexts. They are included because the binary of "wait for perfect integration" versus "deploy fragile AI and hope" is not the only choice available, and the field needs more imagination about what the third path looks like.

Accept architectural asymmetry. Closed integrated systems will achieve near-real-time harmonized AI. Fragmented networks will not. Instead of forcing convergence, design differentiated architectures optimized for each care delivery model. This is not giving up. It is engineering for reality.

Make patients active reconciliation validators. An AI-generated timeline shown to a patient, asking whether their medication list is current, whether they received care elsewhere, whether their allergies are accurate, turns the patient into a reconciliation loop that scales in ways clinician reconciliation never has. The human in the loop is the one person who has actually experienced all of their own care.

Let AI outputs become a new data layer. A medication reconciliation confidence score. A care gap likelihood flag. A missing data alert. These outputs become new data products feeding planning and governance. AI stops being purely a consumer of the integration mess and starts becoming part of the infrastructure for managing it.

Train models to expect adversarial data. Healthcare data is not just incomplete. It is structurally distorted. Billing codes optimized for reimbursement. Problem lists never reconciled after the acute episode. Models trained on real claims-plus-EHR misalignment would be more robust in production than models trained on gold-standard research datasets. This is standard practice in robust ML research. It is almost completely absent from clinical AI development.

### What I Know and What I Don't

I know what it feels like to hunt a missing tilde at 2am while a batch job burns. I also know what it feels like to stand at a patient's bedside and make a decision on whatever data happened to be available, which was never all of it, and was sometimes embarrassingly little of it. I have been the person who built these systems. I have been the person who had to trust them with someone's life. That is not a metaphor. That is my actual career.

What I know: the integration problem is real, structural, expensive, and not going away on any timeline that matches what is currently being promised to healthcare boards and investors.

What I don't know: how to fix it. I am not sure anyone does, not fully, not at the scale of US healthcare, not in this decade.

What I believe: the people who make real progress will not be the ones who waited for clean data. They will be the ones who built honestly for the world as it is, who designed for incompleteness instead of assuming it away, and who were willing to say out loud what the CFO and COO in the room already knew but nobody wanted to put in the deck.

Patients are not waiting for us to finish the architecture debate. That should make us uncomfortable enough to move.
