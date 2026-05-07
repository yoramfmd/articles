# The Parallel Health System

In my last piece, I described a patient arriving at a consultation with a differential diagnosis her AI had already generated. I want to be more specific about what she might actually be bringing.

Not a Google search. Not a symptom checker. A month of continuous glucose data. A pharmacogenomics report that explains why three medications her previous physician prescribed were likely ineffective given her enzyme profile. A whole-body MRI she booked online, interpreted by an AI-enhanced radiology service, with a radiologist-reviewed report waiting on her phone.

She did not need a referral for any of it. In many states, patients can access most of this pathway without a physician visit at any step.

What has emerged, largely outside the conversation happening in medical conference rooms, is a parallel health infrastructure. Comprehensive, increasingly sophisticated, and already in wide use.

---

## The Wearable Layer: Continuous Data Without a Prescription

The foundation of this ecosystem is the consumer wearable, and it has moved well beyond step counting.

Smartwatches with ECG capability from multiple manufacturers have received FDA clearance for atrial fibrillation detection. Apple pioneered this in 2018; Samsung, Withings, Garmin, and Google Fitbit have since followed with their own cleared cardiac features. Standalone consumer ECG devices are available for direct purchase, generating shareable ECG strip files that clinicians can review or AI systems can ingest directly. Sleep apnea detection features from Apple and Samsung have received FDA marketing authorization as over-the-counter devices. The Google Pixel Watch 3 received FDA clearance in 2025 for loss-of-pulse detection, a feature capable of prompting emergency dispatch during cardiac arrest.

Metabolic monitoring has followed the same trajectory. Dexcom Stelo became the first FDA-cleared over-the-counter CGM in 2024, available without a prescription for adults not using insulin. Abbott followed with FDA clearance for two OTC CGM systems, Lingo and Libre Rio, the same year. A patient can now wear a CGM patch, generate two weeks of interstitial glucose data, and arrive at a clinical encounter with a metabolic profile that would previously have required a physician order and specialist interpretation.

The wearable layer captures what the body is doing continuously. The diagnostic layer goes further: it can explain what it means.

---

## The Diagnostic Layer: Labs, Tests, and Genetics

A patient today can assemble a comprehensive diagnostic picture without scheduling a clinic appointment. The starting point is familiar to almost everyone.

The pregnancy test on a pharmacy shelf was, for many people, the first experience of diagnosing something without a physician involved. That model has since expanded into virtually every diagnostic category. Over-the-counter self-tests now cover ovulation, menopause, cholesterol, HIV, STIs, COVID and influenza, colon cancer screening, and UTI detection. These are true consumer products: purchased off the shelf, administered at home, no physician touchpoint required.

From there, the scope expands into two distinct models worth separating. The first is direct consumer ordering from national laboratory networks. Quest and Labcorp both operate consumer-facing platforms allowing individuals to order clinical-grade blood panels without a prior physician consultation. This is the domain of Direct Access Testing (DAT): consumer-initiated laboratory testing that bypasses the traditional physician order. Where state law permits it, the pathway is genuinely direct. Available panels span metabolic and diabetes markers, cardiovascular biomarkers, thyroid and hormone levels, and neurological markers including amyloid beta panels for early Alzheimer's risk stratification.

The second model operates in states where direct ordering is restricted. Companies like Everlywell and LetsGetChecked use an independent physician network overlay: a licensed physician reviews the request and issues the order without a clinic visit. The result, from the patient's perspective, is functionally a no-friction pathway, even when a physician is technically in the loop. The mechanism varies; the access experience does not.

Genetic testing extends the reach further. Services have offered carrier screening, genetic health risk reports covering variants associated with hereditary cancer risk and late-onset conditions, and pharmacogenomics reports describing how an individual's enzyme profile affects drug metabolism. Availability varies by product and jurisdiction, and this market segment has experienced significant disruption recently. What matters clinically is unchanged: a patient arriving with her pharmacogenomics data is not asking her physician to interpret a symptom. She is presenting information that should shape every prescribing decision for the rest of her life.

Blood panels and genetic reports describe chemistry and genetics. The imaging layer adds anatomy.

---

## The Imaging Layer: Referral-Free Radiology

Perhaps the most striking development in this ecosystem is the availability of advanced imaging without a referral.

A small but growing set of cash-pay, no-referral imaging services has made whole-body MRI accessible to consumers willing to pay out of pocket. Prenuvo, one of the larger providers, offers tiered scan packages starting around $1,199, covering the head, neck, abdomen, and pelvis without ionizing radiation. Ezra, recently acquired by Function Health, has reduced its full-body MRI pricing substantially and now positions itself as a high-volume screening service. Both operate by employing internal medical groups whose clinicians review questionnaires and issue the required imaging orders, removing the external physician gatekeeping while remaining compliant with state licensing requirements. Coronary artery calcium scans are widely marketed on a self-pay, no-referral basis. Screening mammography is formally recognized as self-referred under FDA guidance, and Medicare does not require a prescription for coverage.

The clinical establishment's position is clear and defensible. The American College of Radiology does not endorse whole-body screening for asymptomatic patients. The concerns about incidentalomas, false positives, unnecessary follow-up, and patient anxiety are real. What that position does not change is the behavior: thousands of individuals are booking these services monthly, receiving AI-interpreted reports, and making decisions about next steps, often before consulting any clinician at all.

---

## The Middle Tier: Bridging Self-Serve and Clinical Care

The gap all three layers above share is the same one: they can generate data and surface findings, but they cannot act on them in the ways a licensed clinical encounter can. That is what the middle tier is for.

MinuteClinic, One Medical, and a growing network of urgent care chains and telehealth platforms offer accessible clinical entry points without requiring insurance, a referral, or weeks of wait time. A positive syphilis antibody test needs confirmatory workup. A whole-body MRI finding needs clinical context. A pharmacogenomics report needs someone to translate it into an actual prescribing decision. This tier can do all of that, at a transparent price point, often the same day.

Amazon's play here is worth reading as a product strategy as much as a health initiative. The AI is the entry point. Prime members receive five free direct-message care visits with a One Medical provider. A $99 per year One Medical membership and Amazon Pharmacy integration sit underneath. Whether or not the product was designed as a conversion path, that is what the stack describes: a low-friction entry, a clinical touchpoint, and a pharmacy relationship at the exit.

CVS has assembled a comparable stack through different acquisitions: MinuteClinic, Aetna, and Oak Street Health for the primary care layer. What Amazon brings that neither has fully replicated is a consumer surface hundreds of millions of people interact with daily, layered over clinical infrastructure and pharmacy logistics.

---

## The Regulatory Patchwork and the Equity Gap

This ecosystem is real, but it is not equal, and the legal and regulatory context is part of the story.

State law governs laboratory test ordering, and the variation is significant. Roughly half of US states permit consumers to authorize their own lab tests directly. A second cluster restricts direct access to specific test categories. A third group, including Connecticut, Georgia, Michigan, Pennsylvania, and Tennessee, requires a physician order even for basic blood work, meaning a telehealth bridge is legally necessary to access tests that patients two states over can order unilaterally. Access to the same clinical information varies entirely by zip code.

The privacy landscape is equally uneven. HIPAA covers healthcare providers and their business associates, but as a matter of current law it does not extend to most consumer health apps, wearables, or DTC lab platforms. A patient integrating CGM data, genetic reports, and imaging findings through an AI health tool is operating almost entirely outside HIPAA's protections.

Cost remains the most direct barrier. Cash-pay whole-body MRI services currently range from a few hundred to several thousand dollars depending on provider and scope. The patients who most need alternative access pathways, the uninsured, the lower-income, those without a regular care relationship, are largely priced out of the premium end of this ecosystem. Access is expanding, but it is expanding unevenly.

---

## The Data Problem Nobody Is Solving

Every tool in the patient's toolkit generates data in its own format, stored in its own system, governed by its own terms. The CGM data lives on Dexcom's platform. The ECG traces are in Apple Health. The genetic report is on a genetics service's servers. The lab results are in Quest's portal. The imaging report is a PDF from the radiology provider. There is no semantic layer connecting them. The AI interpreting any one data stream has no awareness of the others.

The documentation gap makes the governance problem concrete. When a patient arrives with an AI-generated differential, three months of CGM data, and a radiologist-reviewed MRI report, what does the clinical encounter record? The note says "patient seen." There is no ICD code for what actually happened. No billing modifier for "AI-informed encounter."

At the rate this ecosystem is growing, the ICD-10 classification system is going to need a new chapter:

- Z99.AI1: Disposition: Clinical outcome of AI review
- Z99.AI10: AI output reviewed, clinician in agreement
- Z99.AI11: AI output reviewed, partially agreed, with modification
- Z99.AI12: AI output reviewed, clinician disagrees and redirects care
- Z99.AI13: AI output challenged, required clinical debiasing
- Z99.AI14: AI-informed care confirmed, treatment or prescription initiated

There is a serious version of this joke. Clinical documentation exists to record what influenced a care decision, who made it, and why. If AI is shaping those decisions and the documentation framework has no way to capture it, the gap is not administrative inconvenience. It is a liability problem, an audit problem, and an outcomes research problem. You cannot study what you do not record. You cannot govern what you cannot see.

The central question is not whether a parallel health system exists. It does. The question is who builds the infrastructure that makes it coherent, safe, and usable across tools, jurisdictions, and patient populations, before the fragmentation itself becomes the harm.

---

*Sources: "Referral-free and prescription-free medical follow-up services in the United States," research summary, 2025. "Mapping the Ecosystem of Direct-Access Medical Services and Self-Directed Health Technologies for Health AI Optimization," research summary, 2025.*
