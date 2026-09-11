---
title: "Silent Degradation: What a Deployed Clinical AI Looks Like at Month Eighteen"
slug: silent-degradation-what-a-deployed-clinical-ai-looks-like-at-month-eighteen
published_at: 2026-04-07
custom_excerpt: "Your agent shipped. Your team moved on. Silent degradation is what happens next, and nobody is watching for it. The most-deployed clinical AI in American hospitals ran at half its advertised accuracy for six years before anyone audited it. Three disciplines before the next ship."
tags: [agentic]
feature_image: https://storage.ghost.io/c/e6/05/e605b234-3cc8-4fe4-97bb-2bb55b18b8fb/content/images/2026/04/ChatGPT-Image-Apr-20--2026--02_34_12-PM.png
source: ghost
---

# Silent Degradation: What a Deployed Clinical AI Looks Like at Month Eighteen

---

In 2021, a research team at the University of Michigan published an audit of the most widely deployed sepsis prediction algorithm in American hospitals. What they found should have been a bigger story than it was.

Epic Systems had marketed the Epic Sepsis Model with a claimed area under the curve of 0.76 to 0.83, a respectable number for a screening tool. The Michigan audit, across 27,697 patients and 38,455 hospitalizations, measured an actual AUC of 0.63. Sensitivity sat at 33 percent. Positive predictive value, 12 percent. The algorithm had been live across hundreds of hospitals for six to eight years. No regulator had audited it. Epic had not. The customers had not. The audit that finally measured it was an academic exercise. Not a market signal, not a compliance trigger. Curiosity.

The number that matters for this piece is not 0.63. It is six to eight years. That is how long a widely deployed clinical AI can run at roughly half the claimed performance, across American hospitals, in a regulated industry, before a single external team notices.

If you ship agentic AI in any industry, this is your problem. The clinical case is sharper because the stakes are higher and the audit happened. The mechanism is not clinical. The mechanism applies to every production AI system you have shipped or are about to.

## The thing with no name

There is no widely used term for what happened to the Epic Sepsis Model. The closest words come from different disciplines, each describing one piece of the same phenomenon.

Medical informatics calls it alert fatigue. Human factors calls it automation complacency. Sociology calls it normalization of deviance. Psychology calls it habituation. Machine learning calls it drift, which is itself three different phenomena labeled with one word.

Every one of those names a cognitive failure, how humans process signals they can see. None of them names the three conditions underneath, which are not cognitive but epistemic and structural.

The first is ignorance. In 2021, most hospital staff using the Epic Sepsis Model did not know a deployed algorithm could silently lose half its accuracy over time. They had no working mental model for model drift, no vocabulary for training-data decay, no expectation that the vendor would tell them if either had happened. Ignorance here is not an insult. It is the technical statement that the phenomenon sat outside the conceptual space of the people using the tool.

The second is blind trust, which follows from ignorance the way gravity follows from mass. You defer to systems you do not understand, and in 2021 almost no clinician was in a position to understand a machine learning model. The trust was real, reasonable given the information available, and wrong.

The third is lack of transparency. Even a user with a correct mental model could not have audited the system's currency, because the vendor did not publish the question, let alone the answer. You cannot check a box that does not exist on the form.

None of the terms, cognitive or structural, captures the full shape of the failure mode, which is this. A deployed AI system running in production in a regulated industry for six to eight years, producing fluent and plausible output that was, on average, half as accurate as advertised, in a domain where that gap meant missed sepsis cases.

Call it silent degradation. That is what this piece is about.

## The scissors close from both sides

The reason silent degradation is worse than loud failure is that it is the product of at least four vectors closing on each other.

Human trust in the system rises with time in deployment, even when the system is getting worse. Users watch it appear to work, and appearance compounds into assumed reliability. At the same time, human vigilance falls. Warning fatigue at the interface layer, automation complacency at the workflow layer, automation bias at the decision layer. All three firing at once, each studied in isolation, none with an agentic LLM in the sample.

On the system side, the drift is not one thing. The model vendor silently updates the underlying model. The training cutoff moves. The context window changes. The tokenizer changes. The retrieval corpus shifts. The upstream tool API evolves. The system prompt accretes small improvements, each tested alone and never tested together. The guardrail policy tightens and the workflow that used to complete now pauses. Each substrate has its own drift rate. The agent composes all of them, and the composition amplifies rather than dampens.

Behind both of those, two vectors nobody talks about. The detection system itself degrades as the team rotates, the dashboard deprecates, the PM who knew which metrics mattered leaves, and the organizational memory of why the observation existed at all erodes. And the human workaround silently compensates. Users learn the AI's quirks, prompt around failures, ignore low-confidence outputs, double-check certain task types. Their metric, did I finish the task, keeps ticking green. The system's metric, did the AI do its job, was never being measured in the first place.

The scissors close. The middle is where the customer lives.

## Why agentic systems are not vertical systems

A fair reader pushes back here. Classical software drifts too. Schemas evolve, dependencies break, feature flags accumulate until nobody remembers which combinations are tested. That is true. The difference is not that vertical systems are stable. The difference is that vertical systems have thirty years of tooling, regression harnesses, golden datasets, and canary deploys, and when they break they usually throw an error.

Agentic systems fail differently. They do not throw errors. They produce fluent wrong answers. And they have a combinatorial execution surface that no vertical system has. A traditional tool has N code paths; you test them. An agent navigates a decision tree where each node is a probabilistic call to a model the vendor may silently change, calling tools whose APIs may silently change, against a retrieval corpus someone may silently update, on a context window whose compression heuristics may silently change. The product of eight drift rates, not the sum, is what determines whether the agent is doing its job.

Every stable vertical system has one substrate that can drift. Agentic systems have at least eight, each unobserved by default, and the failure mode is fluent-and-wrong, not loud-and-broken.

## The CME question

Here is the move that makes the problem visible to anyone who has ever interacted with a physician.

A physician is required to prove continuing medical education. It is auditable. State licensing boards log the credits. Specialty boards require recertification. The number of hours, the content, the date, all on record. When was your last renewal, in what, is a question a physician can answer.

Ask the same question of a deployed AI. When was the training data last refreshed. On what corpus. Curated by whom. Retractions pulled, yes or no. Clinical guideline updates propagated, yes or no. In most enterprise deployments, the vendor knows, maybe. The buyer, never.

CME is performative in places. Physicians click through modules. Board certifications lapse rarely, even for practice that is obviously out of date. The analogy still holds, because CME is not making a claim about knowledge currency. It is making a claim about accountability structure. The physician's currency is imperfect but auditable. The AI's currency is neither.

The concrete clinical examples are brutal. The 2020 Surgisphere Lancet paper on hydroxychloroquine was retracted within weeks. Any model trained on late-2020 web corpora reasoned from it, and the retraction never propagated. The FDA changes boxed warnings continuously. A model with a 2023 cutoff does not know about a 2024 label change that is now standard of care. AJCC 9th edition replaced 8th edition in 2023. A model trained before the transition will stage a tumor using retired criteria, fluently.

This is the same mechanism I argued in the Iceberg piece on a different axis. Context stays behind when data moves across space, which is how the Iceberg shows up in FHIR exchange. Context also stays behind when time moves past the training cutoff. Same problem, different dimension.

Retrieval augmentation mitigates this imperfectly. Layering a current corpus over a stale base model moves the problem without solving it. Now the question becomes who curates the retrieval corpus, how often, and whether retractions get pulled. That is a different silent-drift surface. The Epic Sepsis Model ran in production for six years while retracted clinical studies sat in its training substrate and nobody asked the question.

## The observation you are doing right now

Every LLM interface you use today ships with a disclaimer under the input box. "AI can make mistakes. Please double check responses." Or some version of it.

You have not, today. Neither has anyone else. The time cost of literally verifying every LLM output would consume hours per day, which is why the disclaimer works as a legal instrument and fails as a behavioral one. The foundational study in this space, Akhawe and Felt at USENIX 2013, measured 70 percent click-through on Chrome SSL warnings across 25 million impressions. That was for a warning that interrupted the workflow. The LLM disclaimer does not interrupt. It sits under the chat box. The mechanism suggests compliance would be lower, not higher, than 70 percent. No published study has measured it. That is a research gap the industry has carefully not filled.

The disclaimer is where silent degradation meets the user. Three failure modes fire at the same time. Warning fatigue says ignore the warning. Automation complacency says the output probably is right. Automation bias says even if I had doubts, I will defer. Nobody catches the degradation because nobody was looking.

## What Tesla shows us

Tesla Autopilot is the consumer-facing mirror of the Epic Sepsis Model. The difference is that the observation layer exists. NHTSA built it. Tesla did not.

As of April 2026, NHTSA's investigation into Full Self-Driving visibility failures has been escalated to an Engineering Analysis covering 3.2 million vehicles. Nine crashes, one fatality, one injury, with documentation that the system fails to detect sensor degradation under common roadway conditions. A separate investigation into FSD traffic violations is open. Tesla's self-reported safety figures use a miles-between-incidents denominator skewed toward highway driving, while NHTSA counts incidents across all conditions. The two approaches are not directly comparable, and no third-party audit has reconciled the gap.

The point is not that Tesla is uniquely bad. The point is that a regulator had to build the observation layer, and the regulator's data is what made degradation visible. In enterprise SaaS and clinical decision support, there is no NHTSA. There is academic curiosity, occasionally, years late.

## The eighteen-month problem

The counter-argument to everything above is that the industry is maturing. Vendors are building guardrails. The field will figure this out.

Part of this is right. Input-output moderation is maturing. Content filters, refusal training, jailbreak defense. Real, visible progress. Runtime observation of deployed agentic systems is not. Evaluation harnesses like HELM and BIG-bench are pre-deployment benchmarks, not production monitors. LangSmith and Braintrust solve trace inspection, not drift detection.

The history cuts the other way. Browser security has been maturing for twenty years and Akhawe and Felt still measured 70 percent click-through in 2013. Clinical decision support has been maturing for thirty years and override rates sit at 49 to 96 percent in 2024. Domain maturity addresses specific incidents. It does not solve the class of problem.

Underneath the maturity argument is a problem that kills it. The field is not maturing; it is replacing itself. Three generations of frontier LLMs have shipped in the last eighteen months. GPT-4 to 4o to 4.1 to 5. Claude 3 to 3.5 to 3.7 to 4 to 4.5 to Opus 4.6. Gemini 1 to 1.5 to 2 to 2.5. Each generation resets the evaluation work, because capability shifts, refusal boundaries move, context window behavior changes.

The consequence is that every observation instrument you build has a half-life of roughly eighteen months, measured in frontier model generations. The instrument itself has to be versioned and re-calibrated at each generation turn. That is a cost nobody is budgeting for, and it is the cost that determines whether your 2026 observation layer still works in 2028.

And the change is not monotonically bad. Some generation shifts fix errors the previous generation made. The buyer gets silent improvements alongside silent regressions. The net effect is not decline, which would be measurable. The net effect is uncertainty in both directions. You are not running the system you evaluated, and you do not know in which direction you are off.

Uncertainty-in-both-directions is the condition under which incident recovery time goes long, because the team cannot tell whether the anomaly is a degradation or a new capability they did not plan for. Rollback is easy when things got worse. Rollback is paralysis when they might have gotten better in three places and worse in one.

## What to do about it

The four runtime artifacts from the earlier pieces in this series, the autonomy boundary, the approval moment, the audit surface, and the recovery workflow, are necessary. The six observation instruments, task success rate, unintended action rate, override frequency, confidence calibration, rollback time, and incident recovery time, are also necessary.

Silent degradation adds three operating disciplines on top.

First, treat the observation instruments as first-class product artifacts with their own versioning and their own re-calibration cadence at each frontier model generation, not as dashboards maintained on someone's side.

Second, ask the vendor question the buyer side is not yet asking. When was the training data refreshed, on what corpus, and do you publish behavioral change notes at each release? The silence on this question is not neutral. It is a risk the buyer has accepted without naming.

Third, budget for an external audit. Not a vendor audit, not a compliance audit. An independent external audit on the model of what the Michigan team did to the Epic Sepsis Model. If the vendor's answer to "how do you know your agent is still doing what it was doing eighteen months ago" is "we monitor it," the audit is what tests the monitoring, not the agent.

## The list nobody wants to be on

In 2028, there will be a list of companies whose agent did something in production that no one on the team knew it had been doing for months. The Epic Sepsis Model is already on a version of this list. It took six to eight years to get there, and the only reason it got there at all is that an academic team at Michigan had research funding and curiosity.

Your company does not get Michigan. Your company gets whatever observation layer it built, and whatever external audit it commissioned.

Silent degradation is not a clinical problem. It is not a regulated-industry problem. It is what happens by default to every deployed agentic AI, in every domain, because the mechanism is attention, drift, replacement, and organizational memory, and every one of those is a human constant.

The companies that will not be on the 2028 list are the ones that treated observation as infrastructure, not afterthought, and that re-calibrated their instruments every eighteen months, on the clock of the next frontier model.

Maturity requires stability. The field has none. Plan accordingly.


---

*This piece closes the Agentic Experience Design series. The previous articles framed the human and the AI agent as simultaneous customers, developed the four runtime artifacts, the six observation instruments, and the four-question pre-launch review. This installment follows the system past the ship date and into the eighteen-month window where silent degradation does its work.*

## Sources

1. Wong A, Otles E, Donnelly JP, et al. External Validation of a Widely Implemented Proprietary Sepsis Prediction Model in Hospitalized Patients. JAMA Internal Medicine. 2021;181(8):1065-1070. (n=27,697 patients, 38,455 hospitalizations; observed AUC 0.63; sensitivity 33 percent; PPV 12 percent)
2. Akhawe D, Felt AP. Alice in Warningland: A Large-Scale Field Study of Browser Security Warning Effectiveness. USENIX Security Symposium. 2013. (25+ million warning impressions; 70.2 percent click-through on Chrome SSL warnings)
3. Parasuraman R, Manzey DH. Complacency and Bias in Human Use of Automation: An Attentional Integration. Human Factors. 2010;52(3):381-410.
4. Van Der Sijs H, et al. Drug-drug interaction alert override rates in clinical decision support: systematic review and meta-analysis. Multiple peer-reviewed sources, override range 49-96 percent.
5. Vaughan D. The Challenger Launch Decision: Risky Technology, Culture, and Deviance at NASA. University of Chicago Press, 1996. (origin of "normalization of deviance")
6. NHTSA Office of Defects Investigation, PE24031 and EA26002, Tesla Full Self-Driving visibility failures, March 2026. 3.2 million vehicles; nine crashes; one fatality; one injury.
7. NHTSA Office of Defects Investigation, PE25012, Tesla FSD traffic violations investigation, October 2025.
8. Agentic Experience Design series, Articles 1-4, Yoram Friedman, 2026 (four runtime artifacts; six observation instruments; Four-Question Pre-Launch Review).
9. The Iceberg framework, FHIR and clinical data exchange essay, Yoram Friedman (context stays behind when data moves).


---

*Yoram Friedman, MD is a physician and senior product manager at SAP Business Data Cloud. He holds three Harvard Medical School executive education certificates in healthcare digital transformation and AI.*
