---
title: "The Last Generation That Can Supervise AI"
slug: the-last-generation-that-can-supervise-ai
published_at: 2026-05-01T23:59:31.000Z
custom_excerpt: "We are running an experiment on human oversight without a control group, without outcome tracking, and without a policy framework designed for the result. The current generation of experts may be the last one capable of catching what AI gets wrong."
tags: [healthai]
feature_image: https://storage.ghost.io/c/e6/05/e605b234-3cc8-4fe4-97bb-2bb55b18b8fb/content/images/2026/05/ChatGPT-Image-May-1--2026--08_01_55-PM.png
source: ghost
---

# The Last Generation That Can Supervise AI

> *"Did you feel she was a person?"*
> *"Yeah. I did."*
> *"That's all I needed to know."*
> — Alex Garland, Ex Machina (2014)

---

There is a physician practicing today who learned to read a colonoscopy without any help. She developed the skill over hundreds of procedures, learned to move the scope with the slow, deliberate patience that polyp detection requires, trained her eye to linger rather than scan. She is good at this. And for the past year, she has been doing colonoscopies with an AI assistant that highlights suspicious lesions in real time with a green bounding box.

She is not aware of what is happening to her.

A multicenter observational study published in The Lancet Gastroenterology and Hepatology in August 2025 tracked 19 experienced endoscopists across four Polish centers during the first three months after AI-assisted colonoscopy was introduced. The investigators looked specifically at what happened when those physicians performed procedures without AI. The adenoma detection rate fell from 28.4% to 22.4%. An absolute drop of six percentage points. A 21% relative decline in the ability to find precancerous growths, independently, among physicians who had spent years developing exactly that skill.

Three months. That is how long it took.

The study was observational, not a randomized trial. Nineteen endoscopists is a modest cohort. It has not yet been replicated. The authors acknowledged sensitivity to confounding. All of those caveats are real and worth keeping. And yet: this is the first real-world clinical study to measure what happens to a physician's independent skill after sustained AI use, and the result was not ambiguous. The skill declined, measurably, in the direction you would predict, at a speed that should concentrate the mind.

The deeper finding is not in the numbers. It is in the mechanism. Eye-tracking research published before the Lancet study showed that endoscopists under AI assistance reduce their eye travel distance during procedures. They stop scanning. The AI is scanning for them. The brain, efficient machine that it is, offloads the task it no longer needs to perform. When the AI is removed, the active visual search that experienced endoscopists had built over years is not sitting in reserve, waiting to be called on. It has atrophied. The physician who used to scan methodically now waits, without quite realizing it, for a box that is not coming.

---

This is deskilling. The loss of a capability that existed.

But there is a second phenomenon, structurally more dangerous and almost impossible to detect from the outside. A 2025 New England Journal of Medicine review crystallized a taxonomy: deskilling, mis-skilling, and never-skilling. The third category is the one that should keep policymakers awake. Never-skilling is not losing a skill. It is never developing it in the first place, because AI was present during the entire formative window.

Medicine builds expertise through encounter volume, acuity range, failure, and feedback timing. A radiology resident learns to read a chest X-ray by reading thousands of them, being corrected in real time by someone who has read tens of thousands. A pathology trainee develops pattern recognition by sitting with slides until the morphology is not something they remember but something they see. This is not pedagogical tradition. It is how neural pattern recognition is built in human experts. The mechanism requires friction: independent judgment, including wrong independent judgment, corrected under pressure.

When AI is present from the beginning of that window, the mechanism is interrupted. The trainee produces correct outputs. The outputs are graded as correct. The attending confirms. Nobody in the feedback loop has visibility into whether the correct output came from developing clinical judgment or from AI-assisted pattern matching that the trainee cannot replicate independently. The skill appears to form. The competency is never actually acquired.

The NEJM review is a framework, not a dataset. It names the risk; it does not yet measure it. Direct evidence for never-skilling is thin: small software development experiments showing novices who use AI during learning score 17 points lower on comprehension tests afterward, conceptual arguments about formative windows, early signals from medical education researchers. The field is looking for a study that tracks a full cohort of residents through training with and without AI and measures independent performance at the end. That study has not been done. It may take a decade to complete. By then, the first never-skilled cohort will be practicing.

---

The question underneath all of this is the one nobody is asking directly: what happens to the safety model?

Healthcare AI governance, like most AI governance, is built on the assumption of a human in the loop. The FDA's Clinical Decision Support guidance rests on Criterion 4: a qualified clinician independently reviews AI recommendations before acting. Medical AI products are approved on the premise that a physician will catch the errors. The entire framework for deploying clinical AI in regulated environments requires that the physician is actually capable of independent review.

That assumption is not being tested. It is being assumed.

In 1983, the British psychologist Lisanne Bainbridge described what she called the ironies of automation. Her central observation: the more reliable the automated system, the more thoroughly atrophied the monitoring skill. When automation fails, it fails under the conditions humans are least prepared for: unexpectedly, under time pressure, in situations where the judgment required to identify and correct the failure has not been exercised in months or years. The automation that makes the system safer under normal conditions is the same automation that makes the system fragile under abnormal ones. She was describing industrial control systems in 1983. She was describing healthcare AI in 2026.

The supervision paradox has been theorized for over four decades. Nobody has directly measured it in a clinical AI context. No published study has taken a cohort of physicians with documented AI-induced skill decline and tested their ability to catch AI errors, compared to a control group that continued practicing independently. This is the most important evidentiary gap in the field. The human-in-the-loop safety model rests on the assumption that the loop contains a human who can actually catch an error. That assumption has never been empirically tested under conditions of sustained AI use. The argument that the model is structurally unstable is therefore inferential, but it is not speculative: each link in the chain has independent empirical support.

The evidence that does exist points in one direction. When AI provides incorrect BI-RADS suggestions to experienced mammographers, their accuracy drops substantially compared with reading unaided; in controlled experiments, readers with wrong AI suggestions are meaningfully more likely to abandon correct initial judgments in favor of the AI's answer than readers working without any suggestion at all. Not because they are unskilled. Because the confident wrong answer activates a cognitive override that decades of training does not reliably prevent. This is automation bias: an acute effect, not the same as longitudinal deskilling, but a demonstration of what happens when the AI and the physician disagree and the physician defers. Now layer deskilling on top. The physician who has spent three years with AI-assisted imaging has less independent baseline to anchor against. The bounding box has more authority, not because the model has earned it, but because the alternative, independent human judgment, is thinner than it used to be.

In computational pathology, the picture is similar. Controlled experiments show that when AI suggestions are wrong, a non-trivial fraction of initially correct human judgments are overturned; in one careful study, roughly 7% of correct evaluations were reversed by erroneous AI advice, an effect that intensified in severity under time pressure. Seven percent sounds manageable until you consider the scale: millions of pathology reads per year, an error rate that compounds, and a workforce whose independent baseline is narrowing.

---

The software data is consistent, and it arrives with better experimental controls.

The METR 2025 randomized controlled trial followed 16 experienced developers across 246 tasks. AI use increased task completion time by 19%. The developers believed they would be faster. They were not. The study was small, but it was an RCT, and the direction of the effect was the opposite of what every AI productivity narrative assumes. A parallel dataset from GitClear, analyzing 211 million changed lines of code across major repositories between 2020 and 2024, showed refactoring activity falling from 25% of code changes to under 10%. Copy-paste code rose from 8.3% to 12.3%. The hallmark of sustainable engineering, the ongoing restructuring and simplification of systems, was being quietly displaced by the generation of new output that required less judgment and more cleanup.

Neither of these findings is catastrophic in isolation. Together they describe a direction of travel, and that direction is the same one the colonoscopy data suggests. The work that builds and maintains expertise is being offloaded to AI. The outputs look correct. The underlying skill that would allow a practitioner to catch an incorrect output, or to produce correct output when AI is unavailable or wrong, is atrophying.

The novice data is starker. Anthropic's coding skills study showed that novices who used AI during learning scored 50% on subsequent comprehension tests. Those who engaged directly scored 67%. The debugging gap was worse: novice AI users scored near zero on debugging questions. Not because the tasks were harder. Because they had never done the cognitive work of understanding what they were building.

---

Aviation is the only profession that has looked directly at this problem and built an institutional response to it.

In September 2025, the European Aviation Safety Agency issued a Safety Information Bulletin explicitly warning that "continuous use of automated systems does not contribute to maintaining pilot manual flying skills" and could degrade the ability to handle manual flight during unusual situations. Long-haul captains on heavily automated aircraft have been estimated in some analyses to accrue under one hour of true manual flying per year. The EASA bulletin was not predicting a future problem. It was naming a present one.

The institutional response is mandatory recurrent manual proficiency. Pilots are required, on a regular schedule, to demonstrate that they can fly the aircraft without automation. Not as a theoretical exercise. In the simulator, under actual conditions, including upset recovery, sensor failures, and off-normal situations designed to test whether the skill is present or merely assumed to be present. The checks are binding. The record is maintained. The requirement is not negotiable.

No other knowledge profession has built the equivalent. Not medicine, not software engineering, not any of the fields where AI is now handling an increasing share of the cognitive work that practitioners are paid to perform. Aviation did not develop its recurrent proficiency model because the problem was theoretical. It developed it because aircraft fell out of the sky when automation failed unexpectedly and the pilots, who believed they could take over, discovered that the assumption had not been tested in a long time.

---

The argument here is not that AI should not be used in clinical or technical settings. The Brodeur et al. study published in Science earlier this year demonstrated that o1 outperformed attending physicians on management reasoning, approaching 90% accuracy against roughly 40% for physicians with access to GPT-4 and roughly 34% for physicians using conventional resources. That evidence is real. AI can reason at a level that exceeds current human performance on the benchmarks we have. The argument for human oversight is not that humans are better. It is that the system is safer when a competent human can catch the cases where AI is wrong.

That argument requires the competent human to actually be competent.

The better the AI becomes, the more plausible it seems to rely on it, and the less practice the human gets doing the underlying work. That is the structural reason the safety model can fail faster than capability forecasts alone would predict.

The current generation of physicians, engineers, and other knowledge workers who were trained before AI entered their formative window are, in an important sense, the last cohort who will be able to supervise AI from a position of independent capability. They have the baseline. They can notice when the output does not look right. They have enough mental model of the underlying process to recognize a wrong answer that is presented confidently. That is not a credential. It is a skill built through years of practice that the next generation will not have the same opportunity to develop.

This is not a prediction about machines replacing humans. It is a prediction about a safety model that was designed for one world and is being deployed in a different one. The FDA's Criterion 4 was designed for a clinician who had spent years developing independent clinical judgment. It is being applied, increasingly, to clinicians who are developing clinical judgment alongside AI, through AI, sometimes instead of the friction that builds it.

The colonoscopy data showed what three months can do to experienced practitioners. The formative window for a physician spans five to seven years of residency. Nobody is measuring what happens to someone who completes that window with AI as a constant presence. Nobody has defined what independent clinical competence looks like for a physician trained in that environment, or whether the current regulatory model for human oversight holds when the human in the loop is never-skilled.

That is the experiment we are currently running, without a control group, without outcome tracking, and without a policy framework designed for the result.

Aviation had the accidents first. Then it built the requirements.

Medicine is still waiting to find out which comes first.

---

> *"One day the AIs are going to look back on us the same way we look back on fossil skeletons on the plains of Africa. An upright ape living in dust with crude language and tools, all set for extinction."*
> — Alex Garland, Ex Machina (2014)

---

*This article is part of an ongoing series on healthcare AI, clinical workflow, and the systems that connect them.*

---

**Sources**

Budzyń K et al. "Endoscopist deskilling risk after exposure to artificial intelligence in colonoscopy: a multicentre, observational study." *Lancet Gastroenterology and Hepatology.* 2025 Oct;10(10):896–903. doi: 10.1016/S2468-1253(25)00133-5

Abdulnour R-EE, Gin B, Boscardin CK. "Educational Strategies for Clinical Supervision of Artificial Intelligence Use." *New England Journal of Medicine.* 2025 Aug 21;393(8):786–797. doi: 10.1056/NEJMra2503232

Dratsch T et al. "Automation Bias in Mammography: The Impact of Artificial Intelligence BI-RADS Suggestions on Reader Performance." *Radiology.* 2023 May;307(4):e222176. doi: 10.1148/radiol.222176

Bainbridge L. "Ironies of Automation." *Automatica.* 1983;19(6):775–779.

METR. "Measuring the Impact of Early-2025 AI on Experienced Open-Source Developer Productivity." 2025 RCT, n=16 developers, 246 tasks.

GitClear. Developer Productivity Analysis, 211 million changed lines of code, 2020–2024.

European Aviation Safety Agency. Safety Information Bulletin 2025-09, Manual Flying Skills Degradation.

Rosbach E et al. "Automation Bias in AI-Assisted Medical Decision-Making under Time Pressure in Computational Pathology." In: *Bildverarbeitung für die Medizin 2025.* doi: 10.1007/978-3-658-47422-5_27

Brodeur A et al. "Artificial Intelligence versus Physicians on Clinical Reasoning and Patient Management." *Science.* 2026. doi: 10.1126/science.adv2679
