# Not All AI Errors Look Like Errors

*A new paper from MIT, Harvard Medical School, and Google Research maps how AI hallucinates. The taxonomy belongs to every industry, not just medicine.*

---

In a recent article I argued that healthcare AI is the best proving ground for artificial intelligence in the world. The field everyone called a laggard has been running the most rigorous AI experiment for decades, publishing its results, including the failures, so the rest of the field can learn from them.

A new paper from MIT Media Lab, Harvard Medical School, and Google Research is exactly that kind of result. It maps how AI hallucinates in clinical settings: not random noise, but five structured patterns of fabrication. The taxonomy the authors built for medicine applies to every high-stakes AI deployment.

One caveat: the paper is a preprint and has not yet completed peer review. The taxonomy is largely a synthesis of existing research literature, and the failure modes it describes will be familiar to anyone who has worked with AI outputs in production.

I use AI every day, for writing, for research, for synthesis, for first drafts I then revise. Hallucinations are what I fear most. Not their frequency. Their invisibility. A wrong answer that looks wrong is easy to catch. The problem is that AI hallucinations rarely look wrong. They arrive in the same format as a correct answer, with the same confidence, the same fluency, the same structural integrity. Recently it has gone further: a model that knows your voice well enough to write in it will also hallucinate in it. The fabrication arrives in first person. It wears your byline. That is a harder problem. I have also learned the hard way that asking another LLM to validate the first one does not solve this. A model asked to check its peer applies the same training distribution, the same confident tone, and frequently agrees. The validation theater is convincing. The error survives it.

The paper gives this problem a structure. It identifies eleven hallucination subtypes organized into five practical clusters, each with a distinct failure mode and a distinct detection challenge. The labels below are my groupings of the paper's taxonomy, not the paper's exact category names. What the paper says, and what I am arguing here, are two different things: the paper establishes that medical hallucinations are structured and classifiable; I am arguing that those same structures appear in every industry running AI on consequential decisions.

---

## Factual Errors

The model states something false, contradicts data it was given, or ignores information that was explicitly provided. The most dangerous subtype is what the paper calls input-conflicting hallucination: the model overrides the information in front of it with something from its training data instead.

In the paper's clinical examples, a model generates a drug dosage that contradicts the patient-specific parameters provided in the input. The correct weight-adjusted dose is calculable from the data in front of it. The model applies a standard adult dose from its training distribution and presents it with the same confidence as a correct calculation.

In financial services, this would look like: a contract review AI given a supplier agreement with an explicit liability cap of $500,000 summarizes it as uncapped. The correct figure was in the document. The model applied a different figure from its training distribution and presented it as if it had read the document correctly.

The output does not look wrong. That is the problem.

---

## Outdated References

The model draws on information that was accurate at the time of training but has since been revised. Guidelines change. Standards are updated. Regulations are amended. A model trained on static data does not know what it does not know.

In clinical settings, the paper documents cases where models recommend treatment protocols that have since been superseded by updated guidelines, sometimes because new safety data emerged after the training cutoff. The recommendation is delivered with the same authority as current-standard care.

In manufacturing, this could look like: a predictive maintenance AI recommending a lubrication interval based on the manufacturer's 2019 specification. The specification was revised in 2022 after a pattern of field failures. The model was trained before the update. It has no mechanism to know the interval changed. The recommendation arrives with the same confidence as a correct one.

---

## Spurious Correlations

The model merges information from unrelated contexts into a single output that sounds coherent but is internally incoherent. Both underlying data points may be real. The combination is a fabrication.

In clinical AI, the paper describes models blending treatment data from two distinct patient populations whose surface features appear similar but whose underlying conditions differ. The recommendation sounds clinically grounded. The evidence base it draws on does not apply to the patient in front of the clinician.

In retail, this could look like: a seasonal promotion tool asked to recommend discount depths for a back-to-school campaign blending demand elasticity data from a summer outdoor sale with margin signals from a luxury gifting category. Neither dataset applies to the campaign in question. The output is structured correctly, uses the right vocabulary, and produces a number that cannot be traced to any valid logic.

This is the cluster most likely to pass initial review.

---

## Fabricated Sources

The model invents references, certifications, studies, or standards that do not exist. It does not flag uncertainty. It presents the fabrication in the same format as a legitimate citation.

In clinical research, the paper documents AI-generated literature summaries that cite plausible-sounding journal articles, complete with correct formatting and coherent abstracts, that cannot be found in any database. The citations are invented. The confidence is indistinguishable from legitimate sourcing.

In legal practice, this failure has already produced documented consequences. Courts have sanctioned lawyers for submitting fabricated AI-generated citations without independent verification. The citations were formatted correctly. The language was authoritative. The cases did not exist. The legal profession has had to issue specific guidance because the hallucinations were structurally indistinguishable from legitimate sourcing.

---

## Incomplete Chains of Reasoning

The model reaches a conclusion without completing the logical steps that should have produced it. It skips the differential. It ignores relevant factors. The endpoint is stated confidently. The path that should have led there is missing.

In healthcare, where the paper's experimental work is grounded: a clinical decision support tool recommends a first-line antibiotic for a respiratory infection. It does not surface the documented allergy to that antibiotic in the patient record. The recommendation is correct for the diagnosis in the abstract. It is wrong for the patient in front of the clinician. The model completed the task without completing the reasoning.

In financial advisory, this could look like: an AI-powered portfolio tool recommending equity reallocations for a client. The recommendations are reasonable against the stated risk profile and time horizon. The model does not surface a liquidity flag the client entered six months earlier, noting an anticipated capital need within the year. The portfolio logic is sound in the abstract. It is wrong for this client. The model completed the recommendation without completing the reasoning.

---

## What the Taxonomy Is Really Saying

The paper's central observation is not the five clusters. It is the distinction between hallucinations that are visible and hallucinations that are not.

Factual errors can be caught by someone who knows the facts. Fabricated citations can be verified against primary sources. But spurious correlations and incomplete reasoning chains pass initial scrutiny. They use the correct vocabulary. They arrive formatted the way a correct answer would arrive. In medicine they feel like medicine. In finance they feel like finance. In manufacturing they feel like engineering. The paper's phrase for this is "superficially plausible but ultimately incorrect." That description holds in any domain.

The validation problem follows from the taxonomy, even if this paper does not test it directly. The logic is this: a second AI reviewing the first one's output may help catch factual errors that can be checked against something in the input. But for spurious correlations and incomplete reasoning chains, a second model applying the same training distribution is likely to apply the same confident tone and the same tendency to suppress uncertainty. Model-to-model checking may still miss errors unless it is grounded in external evidence. The paper supports this indirectly: its recommended mitigations are all source-anchored, including RAG, knowledge graphs, and constrained decoding, not additional model layers.

The right approach is source-anchored verification. Each factual claim should trace back to a primary source that is not the model. Citations should be independently verified before use. Time-sensitive recommendations should be checked against current standards. For multi-step reasoning, the prompt should explicitly ask the model to show its work step by step, and then each step should be verified independently. One useful pattern: before acting on an AI output, ask the model directly: "Which claims in this output can you verify from what I provided, which come from your training data alone, and which should I independently verify before using?" This does not eliminate hallucinations. It surfaces the uncertainty the model would otherwise suppress.

Healthcare is being forced to develop per-cluster detection and mitigation strategies because failure is immediate, documented, and consequential. The same five failure modes exist in every other industry deploying AI in consequential workflows. Most organizations are still measuring aggregate error rates. Knowing which cluster an error belongs to changes what you do about it.

The taxonomy is not a healthcare document. It is a methodology healthcare developed first because it had no choice. The rest of the field will need it too.

---

*Kim et al. (2025), "Medical Hallucination in Foundation Models and Their Impact on Healthcare." MIT Media Lab, Harvard Medical School, Google Research, Johns Hopkins University, Carnegie Mellon University, Columbia University, Seoul National University Hospital. Preprint: medRxiv, https://doi.org/10.1101/2025.02.28.25323115*
