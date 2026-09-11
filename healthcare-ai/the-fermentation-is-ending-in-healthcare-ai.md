---
title: "The Fermentation Is Ending in Healthcare AI"
slug: the-fermentation-is-ending-in-healthcare-ai
published_at: 2026-06-14
custom_excerpt: "A Nature Medicine paper just benchmarked frontier LLMs against the best clinical AI tools on the market. The frontier models won, and it wasn't close. But the real story isn't the benchmark. It's what the result tells us about who controls clinical AI in five years."
tags: [healthai]
feature_image: https://storage.ghost.io/c/e6/05/e605b234-3cc8-4fe4-97bb-2bb55b18b8fb/content/images/2026/06/ChatGPT-Image-Jun-14--2026--04_51_17-PM.png
source: ghost
---

# The Fermentation Is Ending in Healthcare AI

# 

*A paper in Nature Medicine just told us something the benchmark charts are not designed to show.*


---

I wrote a few months ago about the AI model wars and what they are actually signaling. My argument was that the comparison charts are weather reports. The geology, the slow-moving structural forces that determine who survives and who does not, moves underneath them, mostly invisible until it is not.

A paper published this month in Nature Medicine by researchers at NYU Langone gave me a clearer view of the geology. And what I see is the end of fermentation in clinical AI, arriving faster than most of the companies competing in that space seem to understand.

Researchers who study industrial evolution call the chaotic period before a market structure crystallizes the era of ferment: many competing architectures exist simultaneously, entry rates are high, and no one has established which design will become the standard. Then a dominant design emerges. The shakeout follows. Most entrants disappear. The survivors are not the original innovators. They are the firms best positioned to deliver the dominant design at scale.

In clinical AI, I think we are watching that transition happen.


---

## What the study actually found

The short version: across every evaluation the study ran, general-purpose frontier models outperformed the specialized clinical AI tools. Not at the margins. By a wide and consistent gap, on benchmarks, on clinician-judged scenarios, and on real queries from practicing physicians.

The NYU team ran three evaluations using models at their default production settings. They tested GPT-5.2, Gemini 3.1 Pro, and Claude Opus 4.6 against OpenEvidence and UpToDate's Expert AI, two of the most widely cited and credentialed clinical AI products currently available. Google's AI Overview served as an additional control.

On MedQA, a 500-question USMLE-style benchmark: Gemini hit 97.4%, GPT 94.2%, Claude 90.2%. OpenEvidence came in at 89.6%, UpToDate at 88.4%.

On HealthBench, 500 clinical scenarios evaluated by clinician panels: GPT scored 88.0, Gemini 79.3, Claude 77.0. OpenEvidence: 62.6. UpToDate: 61.3.

On the real-physician-query evaluation, 100 actual clinical questions reviewed by 12 blinded US clinicians generating 1,800 individual annotations using a predefined rubric: the frontier models outperformed the clinical specialists again. OpenEvidence made 52 errors, most of them incomplete content, safety omissions, and disorganized responses. UpToDate refused to answer 19% of queries entirely, under the default coverage settings used in the study. GPT made 21 errors. Claude 19. Gemini 8.

That finding is real, with one caveat worth naming: HealthBench was built by OpenAI, graded by an OpenAI model, and ranks an OpenAI model first. The more credible arm is the real-physician-query evaluation, where that contamination concern does not apply. Twelve blinded clinicians, 1,800 annotations, a predefined rubric. It is also not the most important thing the study is telling us.


---

## This is not a benchmark story

OpenEvidence was built by clinicians, trained on peer-reviewed literature, and positioned as a tool physicians could trust in ways they cannot trust a general chatbot. UpToDate has been a standard of care reference for decades. These are not poorly funded startups. These are well-designed products built by experienced clinicians and engineers.

And they lost. Not narrowly. UpToDate refused nearly one in five queries. OpenEvidence made more than twice the errors of the weakest frontier model.

The gap between the specialized clinical AI products and the frontier general models is not a gap they will close with the next product cycle. It is a structural gap, and it is widening. The companies that built it are Anthropic, Google, and OpenAI. They have access to orders of magnitude more compute than almost any standalone clinical AI company can realistically procure. They have training data that spans every domain. They have teams that dwarf any healthcare-focused AI lab. And they are improving at a rate that compounds quarterly.

No single study can prove a structural transition. But taken together with the consistent direction of every major model evaluation over the past eighteen months, this paper looks less like a blip and more like a signal that the dominant design in clinical AI is crystallizing. And it is not a specialized clinical product. It is a general-purpose frontier model applied to clinical contexts.


---

## The workflow the study was actually testing

Before drawing conclusions about who wins and loses, it is worth being precise about what the study was measuring, because the workflow it tested is the current standard, and understanding it reveals where the real competitive threat comes from.

Here is how a physician uses these tools today. You finish an office visit. You go to your desk. You have a clinical question: a drug interaction, a dosing adjustment for a patient with declining renal function, what the current guideline says about a specific presentation. You open Epic or your EHR to document the encounter. Then you open a second application, UpToDate or OpenEvidence, type your question, and get an answer. Then you go back to Epic.

Two screens. Two contexts. A deliberate context switch between the place where the patient's information lives and the place where you get clinical guidance.

What OpenEvidence and UpToDate answered in the NYU study was a clinical question in a vacuum. They had no idea who the patient was. They did not know her creatinine clearance, her current medication list, her allergy profile, or the note you were halfway through drafting when you picked up the question. They answered a generic version of your query.

That is the current workflow. And that workflow is the vulnerability the study exposed, though not the one most commentators noticed.


---

## The threat the study inadvertently documented

The NYU team's real-physician-query evaluation used 12 blinded clinicians to review AI-generated responses to 100 genuine physician questions. The clinicians assessed completeness, accuracy, safety, and organization. They generated 1,800 individual annotations.

That evaluation design is structurally identical to the validation process you would run before deploying a proactive clinical decision support feature inside an EHR.

Epic and Cerner have something OpenEvidence does not: the patient's full chart. The medication list, the lab trends, the allergy flags, the visit transcript, and the note in progress, all in the same system the physician is already using. They also have millions of physicians who are logged into their platform for several hours every day, with no context switch required to reach them.

The move Epic can make, and is already beginning to make through its Microsoft/Azure OpenAI partnership, is to take a frontier model of the same class that outperformed OpenEvidence in the NYU study and embed it directly in the chart workflow. Not as a separate application. As a panel inside the interface the physician is already using, with full access to the patient record that the standalone tools could never see.

When that happens, the NYU study's findings become Epic's product validation. The frontier models that beat OpenEvidence on 100 real physician queries, reviewed by 12 blinded clinicians, will be answering those same queries inside Epic with the additional context of who the patient actually is. The specialized clinical reference tool, already outperformed on generic queries, will be outperformed by an even larger margin on patient-specific ones.


---

## Three stages, one trajectory

The displacement of standalone clinical AI tools by EHR-embedded AI follows a trajectory that the NYU study helps us locate in time.

Stage one is where we are now. Multiple tools, multiple screens, no shared context. The physician reasons, queries, decides. The AI is a reference, not a participant. The NYU study documented the performance of this stage and found it wanting.

Stage two is the near-term move. A single screen. The AI is inside the chart, with access to the patient's record, available as a conversational interface during the documentation workflow. The physician asks a question and gets an answer grounded in this patient, not a generic one. The context switch disappears. So does the reason to open OpenEvidence.

Stage three is the harder product problem: the AI surfaces suggestions before you ask. You open the chart after the visit and the reasoning is already there. "Given this patient's declining GFR over the last three visits and her current ACE inhibitor dose, consider reducing by X mg. ADA guideline section 4.3, most recent creatinine: 1.8." You review it, approve it, or override it. The cognitive initiation has moved to the AI. The physician remains in the loop, but the nature of the loop has changed fundamentally.

Stage three is where the real design and liability challenges live. The gating factor will be less "can the model do this" and more "can regulators, insurers, and hospital risk committees accept this pattern of delegation." The physician who approves forty-seven suggestions a day without reading them carefully is not in the loop in any meaningful sense, and the legal and governance frameworks for that situation do not yet exist.

Stage four, full autonomy for complex clinical reasoning, requires regulatory frameworks that have not been built. It is further away. But stage two is available today, and stage three is an engineering and legal question, not a research one.


---

## Why healthcare is the biggest blue ocean anyone is ignoring

The EHR platform story describes what happens to the clinical AI tools built for physicians inside the traditional system. It is not the whole picture.

Healthcare is not a market that AI has already penetrated. It is a market where AI has barely arrived, and where the size of the unmet need is unlike anything in any other sector.

A patient with a new diagnosis navigates the system alone, at the worst moment of her life, with no training for it. She gets fifteen minutes with a specialist she waited eight weeks to see. She leaves with instructions she partially understood and a follow-up in three months. Between appointments, she has no one to call.

An emerging market patient has no specialist within 200 kilometers. Her country's healthcare system is under-resourced. She speaks a language that most clinical AI tools were not trained on.

The KFF survey data makes the scale concrete: 32% of US adults are already using AI for health information or advice. The uninsured use it at nearly twice the rate of the insured. Among AI health users under 30, 38% cite no provider or lack of access to an appointment as a primary reason. One-third of AI health users with household incomes under $40,000 cite cost.

These are not early adopters experimenting with technology. These are people who have no alternative. The same performance gap that undermines specialized clinical reference tools for physicians explains why these patients are already defaulting to general frontier models: they are more helpful, available in more languages, at no cost, with no appointment required. The clinical AI industry was not building for them. It was building for physicians, for health systems, for payers. The frontier models showed up without being invited and are already more capable than the tools designed for the job. That is how blue oceans get claimed.


---

## Which positions are actually defensible

The consolidation argument has an obvious counterargument: niche players always survive in healthcare. The regulatory moat is real. Clinical validation requirements favor incumbents. Procurement cycles in health systems run eighteen months minimum.

All true. Those are friction arguments, not structural arguments. Friction slows the wave. It does not hold it back.

The positions that are defensible are the ones with assets the frontier models and EHR platforms cannot replicate. In domains where the core inputs are images, signals, or tightly controlled institutional data, specialized models retain a real performance and validation edge that general-purpose LLMs have not yet closed. A radiology AI that sits inside the radiologist's PACS workflow with ten years of institution-specific training data has a defensible position. A pathology AI trained on proprietary slide libraries from fifty health systems is not the same product as Claude reading a pathology report. Longitudinal patient cohorts for rare diseases, workflow integrations so deeply embedded in clinical operations that replacing them requires rebuilding the clinical process itself: these are assets.

The positions that are not defensible are the ones built on a single capability the frontier models now exceed. In text-based clinical question-answering and guideline-style reasoning, the dominant design is already a frontier model with workflow integration. A clinical Q&A tool is not a niche product anymore. It is a feature, and soon it will be a feature inside Epic. The NYU study did not find that general models are approaching clinical AI specialists. It found that they have already passed them on the metrics clinicians actually care about.

The most exposed companies are the ones whose pitch is "we are a safer, more trustworthy, more clinically appropriate version of ChatGPT." The NYU data does not support that positioning. On real physician queries, reviewed by real clinicians, the frontier models made fewer errors. The next study will not reverse that finding.

None of this means specialized clinical AI products vanish overnight. Regulatory approvals, contractual lock-in, and clinical habit will slow the transition. But the direction is not in doubt, and the companies that understand this early will use the remaining time to deepen whatever they have that cannot be replicated, rather than defend a capability position they will not hold.


---

## The fermentation is ending

I wrote before that the AI model wars will end with something structural, not with the model that scores highest on the benchmark chart published this week.

In clinical AI, the structural event may have already happened, and it came from two directions at once.

From above: frontier models that were not designed for healthcare have become more capable at clinical reasoning than the specialized tools that were. The NYU study documented this with a methodology rigorous enough to be published in Nature Medicine: blinded clinician review of real physician queries, 1,800 annotations, a predefined rubric.

From below: the EHR platforms that control the physician's workflow are positioned to embed those same frontier models directly into the interface, with full patient context that standalone tools can never access, reaching a user base already logged in for hours every day.

The era of ferment in clinical AI produced OpenEvidence, UpToDate Expert AI, and dozens of other well-designed products. The shakeout that follows fermentation is not gentle. Entry rates collapse. The survivors are not the original innovators. They are the firms best positioned to deliver the dominant design at scale, with the distribution and data advantages that let them do it efficiently.

In healthcare, those firms are not the specialized clinical AI companies. They are the frontier model developers who now set the capability ceiling, and the EHR platforms who control the workflow through which that capability reaches the clinician.

Healthcare represents the biggest blue ocean in the history of AI adoption. Most of the world's patients have never had access to clinical-grade intelligence of any kind. The tools arriving now are already better than what the specialized market produced, and the platform vendors are about to make them available at the point of care, inside the workflow, with full patient context, to every physician already using their system.

The fermentation is ending. The question is not whether consolidation comes. It is who is positioned on the right side of it when it does.


---

*Related reading: "The AI Model War Will Not Be Won by the Best Model" — on the structural forces determining the outcome of the AI technology wars and why the daily benchmark charts are weather, not geology.*

*Sources: Rao et al., "Performance of frontier large language models versus specialized clinical AI tools," Nature Medicine, 2026. KFF Tracking Poll on Health Information and Trust, March 2026.*
