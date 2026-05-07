# Silent Degradation: What a Deployed Clinical AI Looks Like at Month Eighteen

*Series: Agentic Experience Design, Article 5*

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

Call it silent degradation. That is what this piece is about.

## The scissors close from both sides

The reason silent degradation is worse than loud failure is that it is the product of at least four vectors closing on each other.

Human trust in the system rises with time in deployment, even when the system is getting worse. Users watch it appear to work, and appearance compounds into assumed reliability. At the same time, human vigilance falls. Warning fatigue at the interface layer, automation complacency at the workflow layer, automation bias at the decision layer. All three firing at once.

On the system side, the drift is not one thing. The model vendor silently updates the underlying model. The training cutoff moves. The context window changes. The tokenizer changes. The retrieval corpus shifts. The upstream tool API evolves. The system prompt accretes small improvements, each tested alone and never tested together. The guardrail policy tightens and the workflow that used to complete now pauses. Each substrate has its own drift rate. The agent composes all of them, and the composition amplifies rather than dampens.

Behind both of those, two vectors nobody talks about. The detection system itself degrades as the team rotates, the dashboard deprecates, the PM who knew which metrics mattered leaves, and the organizational memory of why the observation existed at all erodes. And the human workaround silently compensates. Users learn the AI's quirks, prompt around failures, ignore low-confidence outputs, double-check certain task types. Their metric, did I finish the task, keeps ticking green. The system's metric, did the AI do its job, was never being measured in the first place.

The scissors close. The middle is where the customer lives.

## Why agentic systems are not vertical systems

A fair reader pushes back here. Classical software drifts too. Schemas evolve, dependencies break, feature flags accumulate until nobody remembers which combinations are tested. That is true. The difference is not that vertical systems are stable. The difference is that vertical systems have thirty years of tooling, regression harnesses, golden datasets, and canary deploys, and when they break they usually throw an error.

Agentic systems fail differently. They do not throw errors. They produce fluent wrong answers. And they have a combinatorial execution surface that no vertical system has. A traditional tool has N code paths; you test them. An agent navigates a decision tree where each node is a probabilistic call to a model the vendor may silently change, calling tools whose APIs may silently change, against a retrieval corpus someone may silently update, on a context window whose compression heuristics may silently change. The product of eight drift rates, not the sum, is what determines whether the agent is doing its job.

Every stable vertical system has one substrate that can drift. Agentic systems have eight, each unobserved by default, and the failure mode is fluent-and-wrong, not loud-and-broken.

## The CME question

A physician is required to prove continuing medical education. It is auditable. State licensing boards log the credits. Specialty boards require recertification. When was your last renewal, in what, is a question a physician can answer.

Ask the same question of a deployed AI. When was the training data last refreshed. On what corpus. Curated by whom. Retractions pulled, yes or no. Clinical guideline updates propagated, yes or no. In most enterprise deployments, the vendor knows, maybe. The buyer, never.

CME is performative in places. Physicians click through modules. The analogy still holds, because CME is not making a claim about knowledge currency. It is making a claim about accountability structure. The physician's currency is imperfect but auditable. The AI's currency is neither.

The concrete clinical examples are brutal. The 2020 Surgisphere Lancet paper on hydroxychloroquine was retracted within weeks. Any model trained on late-2020 web corpora reasoned from it, and the retraction never propagated. The FDA changes boxed warnings continuously. A model with a 2023 cutoff does not know about a 2024 label change that is now standard of care. AJCC 9th edition replaced 8th edition in 2023. A model trained before the transition will stage a tumor using retired criteria, fluently.

Retrieval augmentation mitigates this imperfectly. Layering a current corpus over a stale base model moves the problem without solving it. Now the question becomes who curates the retrieval corpus, how often, and whether retractions get pulled. The Epic Sepsis Model ran in production for six years while retracted clinical studies sat in its training substrate and nobody asked the question.

## The observation you are doing right now

Every LLM interface you use today ships with a disclaimer under the input box. "AI can make mistakes. Please double check responses."

The foundational study in this space, Akhawe and Felt at USENIX 2013, measured 70 percent click-through on Chrome SSL warnings across 25 million impressions. That was for a warning that interrupted the workflow. The LLM disclaimer does not interrupt. It sits under the chat box. No published study has measured compliance. That is a research gap the industry has carefully not filled.

The disclaimer is where silent degradation meets the user. Three failure modes fire at the same time. Warning fatigue says ignore the warning. Automation complacency says the output probably is right. Automation bias says even if I had doubts, I will defer. Nobody catches the degradation because nobody was looking.

## What Tesla shows us

Tesla Autopilot is the consumer-facing mirror of the Epic Sepsis Model. The difference is that the observation layer exists. NHTSA built it. Tesla did not.

As of April 2026, NHTSA's investigation into Full Self-Driving visibility failures has been escalated to an Engineering Analysis covering 3.2 million vehicles. Nine crashes, one fatality, one injury, with documentation that the system fails to detect sensor degradation under common roadway conditions. Tesla's self-reported safety figures use a miles-between-incidents denominator skewed toward highway driving, while NHTSA counts incidents across all conditions.

The point is not that Tesla is uniquely bad. The point is that a regulator had to build the observation layer, and the regulator's data is what made degradation visible. In enterprise SaaS and clinical decision support, there is no NHTSA. There is academic curiosity, occasionally, years late.

## The eighteen-month problem

The counter-argument is that the industry is maturing. Vendors are building guardrails. The field will figure this out.

Part of this is right. Input-output moderation is maturing. Content filters, refusal training, jailbreak defense. Real, visible progress. Runtime observation of deployed agentic systems is not. Evaluation harnesses like HELM and BIG-bench are pre-deployment benchmarks, not production monitors. LangSmith and Braintrust solve trace inspection, not drift detection.

The history cuts the other way. Browser security has been maturing for twenty years and Akhawe and Felt still measured 70 percent click-through in 2013. Clinical decision support has been maturing for thirty years and override rates sit at 49 to 96 percent in 2024. Domain maturity addresses specific incidents. It does not solve the class of problem.

Underneath the maturity argument is a problem that kills it. The field is not maturing; it is replacing itself. Three generations of frontier LLMs have shipped in the last eighteen months. Each generation resets the evaluation work, because capability shifts, refusal boundaries move, context window behavior changes.

The consequence is that every observation instrument you build has a half-life of roughly eighteen months, measured in frontier model generations. The instrument itself has to be versioned and re-calibrated at each generation turn. That is a cost nobody is budgeting for, and it is the cost that determines whether your 2026 observation layer still works in 2028.

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

*This piece closes the Agentic Experience Design series.*

*Yoram Friedman, MD is a physician and senior product manager at SAP Business Data Cloud. He holds three Harvard Medical School executive education certificates in healthcare digital transformation and AI.*
