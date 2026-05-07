# What Physicians Know That Cannot Be Written Down

*Series: Healthcare AI Analysis and Research Synthesis | Published: April 2026*

---

The attending was pointing to a region of ground-glass opacity on a CT slice. The resident beside me had been working the case for forty minutes. She had followed every protocol, checked every window, compared every prior study. She had not seen it.

The attending had seen it in three seconds.

When we asked him how, he could not tell us. He tried. He used words like "pattern," "something about the distribution," "it looked wrong." None of those words would have helped the resident find it. They did not describe what he saw; they described the space around what he saw, because the thing itself was not a verbal object.

This was not a failure of communication. It was the structure of the knowledge.

---

## The knowledge that never entered the notes

When clinical AI underperforms, the usual diagnosis is bad training data. The notes were too short. The notes were too long. The notes were copy-pasted. The notes reflected billing categories rather than clinical reasoning. All of that is true, and the quality of clinical documentation is a real and consequential problem. It is also not the deepest problem.

The deeper problem is that the most consequential clinical knowledge was never going to show up in the notes regardless of how carefully they were written. It was never going to show up in the textbooks. It was never going to show up in any written record of any encounter. What the attending saw in three seconds is not in the literature. It is not in the teaching file. It is not something he could have dictated to a scribe in the moment, because the mechanism that produced the recognition does not route through language.

I spent two years of my life in a radiology residency learning to read imaging, and two more in anesthesiology and intensive care learning to read patients. In both, the early months felt exactly like the textbooks said they would. You memorized the list of things to check. You went through the list. You arrived at an answer, or you did not. The slow, analytical version of clinical reasoning is the one medicine knows how to teach, because it is the one medicine knows how to describe.

The interesting thing was what happened in the second year.

The list started to disappear. Not because I stopped doing the work. Because the work stopped feeling like a list. I would look at a chest film and my attention would land somewhere before I had thought about where to look. My hands would adjust an infusion before I had assembled the conscious reason. The reasoning did not become faster. It became different. It began to use a substrate that the first year of training did not have access to.

This is the part that does not get written down. Not because physicians are careless about documenting it. Because the substrate is not text.

---

## Why the body holds what the mind cannot dictate

The cognitive science has names for what is happening, and the names point in the same direction.

The basal ganglia, the part of the brain that learns motor skills, is also what learns expert perception. Functional imaging of experienced clinicians reading imaging or responding to a monitor shows activity patterns that look more like a tennis serve or a surgical knot than like a deliberate differential diagnosis. This is not metaphor. The same circuit that encodes the golfer's swing encodes the radiologist's recognition. It is a procedural system, and like all procedural systems, it does not have a reporter function. You cannot ask your basal ganglia what it knows.

Antonio Damasio's somatic marker hypothesis describes a second substrate. The brain tags decisions with their physiological consequences, and those tags bias future decisions before the conscious reasoning engages. The physician who lost a patient to a missed pulmonary embolus is not more vigilant because he remembers to be. The possibility arrives in his body weighted differently than it arrived before the loss. The hands get ready. The attention shifts. The threshold for ordering the test drops. This is not emotion interfering with cognition. It is consequence-weighted cognition, implemented in biology.

James McGaugh showed that high-stakes memory is encoded differently from routine memory. Stress hormones at the moment of an adverse event deepen the memory trace, making it more durable and more influential on every future case that resembles it. This is how one harrowing night on call restructures a physician's risk model for a decade. The written record of that night looks like any other shift. The internal record does not.

A prospective primary care study found that when a pediatrician's gut feeling signaled that something was wrong despite otherwise reassuring findings, the likelihood of serious infection was twenty-five times higher. A meta-analysis of cancer consultations found a fourfold increase in cancer diagnosis when a GP recorded a gut feeling, and the predictive value rose with the physician's years of experience.

The gut feeling is not superstition. It is a compressed signal of consequences accumulated over a career. It is earned, case by case, often at cost, and the writing never catches it because the writing was never the medium.

---

## What happens to AI built from text

None of this is in the training corpus of any large language model, because the training corpus is text.

The corpus can contain a description of what an expert radiologist reported. It cannot contain the mechanism that produced the report. It can describe a pulmonary embolus. It cannot deliver the somatic weight a physician carries after missing one. It can simulate reasoning by predicting plausible-sounding token sequences. It cannot be shaped, the way a clinician is shaped, by twenty years of outcomes arriving in the body with timing and intensity calibrated to the magnitude of the consequence.

This is why the Bedi study in JAMA Network Open last August mattered more than its surface result suggested. When researchers removed the familiar diagnosis labels from standard reasoning benchmarks and replaced them with descriptions of the same physiology, Claude 3.5 Sonnet's performance fell by thirty-four percent. GPT-4o fell by twenty-six. A physician would not be affected. If you understand why a patient is hypoxic, tachycardic, and has pleuritic chest pain, you do not need the phrase "pulmonary embolism" to appear somewhere on the page to reason toward the correct management. The LLMs do. Their reasoning is a sophisticated pattern match over linguistic structures, not a reasoning from physiological first principles.

That is not a data quality problem. It is a medium problem. The model is doing exactly what a system trained on text should do. The limitation is structural, not remediable by more tokens or a better note template.

The labs that built these systems have quietly documented a related pattern. Before the approval-shaping stage of training, language models are reasonably well calibrated; their expressed confidence tracks their actual accuracy. After it, they become more confident and less calibrated. Anthropic published this finding. OpenAI published it in the GPT-4 technical report. The physician's experience, over a career, sharpens the link between confidence and accuracy. The dominant training process in modern AI measurably weakens it. The two systems are accumulating opposite kinds of habits.

---

## Designing for complementarity, not substitution

This analysis does not imply that AI has no place in clinical medicine. It has several. Structured pattern matching on well-labeled data, literature synthesis, protocol adherence, summarization of long charts, triage for common presentations with complete context. These are real contributions, and they become more valuable, not less, once the boundaries of the medium are understood.

The substitution narrative, the one in which AI replaces the diagnostic physician, is a category error. The knowledge is not missing from the AI for a temporary reason that more training will fix. It is not in the medium the AI was built from. No amount of additional text will cause text to become what text is not.

The complementarity design is the one that actually generates value. The AI surfaces what the text can surface: patterns across millions of records, rare findings the individual clinician has not seen, protocol drift, coverage gaps in the documentation, prior studies the human forgot to pull. The physician carries what the body carries: the procedural recognition, the somatic weighting, the consequence-shaped threshold, the gut feeling that earned its rate of return the hard way. The product is the handoff between them, and the handoff has to be designed, because neither medium will bridge the gap on its own.

The pre-verbal response that moved the attending's eyes to the ground-glass opacity in three seconds is not a capability gap on the AI's side. It is a capability the AI was not built to have. The design question is not how to replicate it. The design question is how to build a system in which the AI does the work text is good for, the physician does the work the body is good for, and the interaction between them is legible enough to trust.

The note was never the knowledge.

The sentence can only take you so far.

---

*Yoram Friedman, MD is a physician and senior product leader working at the intersection of healthcare AI, data infrastructure, and human-centered design. He writes on healthcare AI, agentic systems, and what it actually takes for AI to move from pilots to production in regulated environments.*

*This article is part of an ongoing series on healthcare AI, clinical workflow, and the systems that connect them.*

---

**Sources**

1. Bedi N et al. "NOTA: None of the Above: Removing Diagnosis Labels from Clinical Reasoning Benchmarks." JAMA Network Open, August 2025.
2. Damasio A. *Descartes' Error: Emotion, Reason, and the Human Brain.* Putnam, 1994. (Somatic marker hypothesis)
3. McGaugh JL. "Memory consolidation and the amygdala: a systems perspective." Trends in Neurosciences, 2002.
4. Van den Bruel A et al. "Clinician gut feeling about serious infections in children." BMJ, 2012. (25-fold likelihood ratio for serious infection when gut feeling present)
5. Friedemann Smith C et al. "GP gut feelings in cancer diagnosis: a meta-analysis." BJGP, 2020. (Pooled OR 4.24 for cancer; predictive value rises with experience)
6. Tonelli MR, Shapiro D. "Experiential Knowledge in Clinical Medicine." Chest, 2020.
7. Cera ML et al. "Neural correlates of clinical reasoning expertise: an ALE meta-analysis." Frontiers in Neuroscience, 2025.
8. Durning SJ et al. "Perspective: redefining context in the clinical encounter." Academic Medicine, 2010. (Expert fMRI studies)
9. Kadavath S et al. "Language Models (Mostly) Know What They Know." Anthropic, arXiv:2207.05221, 2022. (RLHF reduces calibration)
10. OpenAI. "GPT-4 Technical Report." arXiv:2303.08774, 2023. (Figure 8: post-training process reduces calibration)
