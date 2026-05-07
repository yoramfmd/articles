---
title: The Microscope
slug: iv-the-microscope
published: 2026-01-04
excerpt: In 2018, the FDA cleared an AI to diagnose disease without a physician in the loop. A nurse captures two retinal images, the system delivers a clinical decision, and the company, not the clinic, carries the liability. That was seven years ago. The future we keep debating is already here.
---

*When the machine makes the call*

The first three articles in this series traced AI through specialties where the physician was always in the loop. In radiology, AI learned to read images alongside the radiologist. In cardiology, it moved from interpreting signals to guiding physical interventions. In anesthesia, it evolved from monitoring to prediction to closed-loop control, building what we called a fly-by-wire architecture for the operating room.

This fourth article crosses a different threshold. In pathology and ophthalmology, AI didn't just assist the physician. In one landmark case, it replaced the physician entirely, making autonomous clinical decisions with no human in the loop at all. And in the process, it began to reveal something unexpected: that the diagnostic information hiding in our tissues and our eyes was far richer than anyone had imagined.

**The Machine Is the Doctor**

Here is a claim you will hear at every medical AI conference this year: autonomous AI diagnosis is a dangerous fantasy, a Silicon Valley fever dream that strips the physician from the loop and puts patients at risk.

It sounds reasonable. It sounds cautious. It is also seven years out of date.

In April 2018, the FDA did something it had never done before. It authorized an AI system, called IDx-DR, to diagnose a disease, diabetic retinopathy, entirely on its own. No physician in the loop. No specialist reviewing the output. A clinic nurse takes two photographs of the retina, uploads them, and the system returns a binary clinical decision: refer, or do not refer. The machine is the doctor.

That was not a research prototype. It was a commercial product, deployed in primary care offices, with its own CPT billing code and, in a move that startled the legal community, the manufacturer voluntarily assumed medical liability for the AI's decisions. Not the clinic. Not the nurse. The company.

By 2025, the system, now rebranded as LumineticsCore, was running in dozens of health systems across the country. And it was no longer alone. Eyenuk's EyeArt received its own FDA clearance for autonomous diabetic retinopathy screening, reporting sensitivity around 96 percent in real-world use. This was no longer a single breakthrough product. It was a product category. A 2026 real-world study out of Germany confirmed what the early trials had shown: these systems caught severe retinopathy with high sensitivity while maintaining specificity above 90 percent. The most common "failure" was not a misdiagnosis. It was the machine rejecting blurry images it refused to read, which is exactly the kind of conservatism you want from an autonomous system.

The access argument is what makes this more than a technical achievement. Retinopathy of prematurity, a leading cause of childhood blindness worldwide, faces an even more severe specialist shortage than adult diabetic eye disease. There are only a handful of ROP-qualified ophthalmologists in many countries, and deep learning models trained on wide-field neonatal retinal images can now detect treatment-requiring ROP with sensitivity and specificity in the 90 percent range. About 600 infants in the United States still go blind from ROP each year. The technology to prevent most of those cases exists. The bottleneck, as always, is getting it to the bedside.

The future that the skeptics warn us about is not approaching. It arrived, quietly, in a primary care clinic that couldn't recruit an ophthalmologist.

**Not Enough Eyes to Look**

Pathology and ophthalmology seem like strange bedfellows. One discipline lives in the basement of the hospital, bent over glass slides stained pink and purple. The other sits behind a slit lamp, shining light into a patient's eye. But both fields share the same bottleneck: they depend entirely on pattern recognition in images, and for decades the only pattern recognizer available was a human being who was expensive, scarce, and inconsistent.

For diabetic retinopathy, the barrier was access. The American Diabetes Association recommended annual retinal exams for every diabetic patient. Fewer than half got one, because the ophthalmologist was simply not in the building. In pathology, the crisis was workforce. The number of pathologists in the United States has been declining even as biopsy volumes have risen. A 2019 College of American Pathologists survey found that nearly 70 percent of pathology groups had at least one open position they could not fill. The downstream effect: longer turnaround times, delayed diagnoses, and missed cancers on slides read too quickly by a physician running through 200 cases before lunch.

Both fields hit the same wall. Not enough eyes to look.

The technological response in pathology followed the same arc we have traced across this entire series, from hand-coded rules to supervised learning to foundation models. But pathology hit this arc with a twist: the field could not even begin the journey until it solved a hardware problem that radiology had solved in the 1990s.

Radiology went digital decades ago. The first article in this series described how DICOM standards and PACS workstations became the infrastructure on which everything from early computer-aided detection to modern deep learning was built. Pathology had no equivalent revolution. Glass slides remained physical objects, prepared by hand, read under a microscope, filed in cabinets, and occasionally mailed across the country in a cardboard box when a second opinion was needed. You cannot run an algorithm on a cardboard box.

Whole-slide imaging, the technology that scans a glass slide into a gigapixel digital image, existed in concept from the early 2000s but was painfully slow. A 2006 review clocked scanners at roughly one hour per slide. By the late 2010s, high-throughput devices could digitize a slide in under a minute, but the capital costs, storage demands (each image can exceed a gigabyte), and laboratory integration challenges meant that going digital was an enterprise infrastructure project, not a software upgrade. Pathology departments that wanted to join the AI revolution needed to become small data centers first.

The point matters for builders: radiology's AI revolution was possible because the images were already digital. Pathology's data was locked behind glass. The algorithms could have been brilliant, and it wouldn't have mattered. Without digitization, there was nothing to compute.

Still, a few institutions made the leap. And once the images were digital, the pattern recognition revolution arrived fast.

**From One Cancer to Every Cancer**

The first generation of AI tools for pathology were narrow and task-specific. In 2021, Paige received de novo FDA authorization for Paige Prostate, the first AI-based pathology product ever approved by the agency. Pathologists using the system saw a 70 percent reduction in false negatives and completed their reads faster. Non-specialists using Paige Prostate performed as accurately as prostate subspecialists working without it.

Powerful, but narrow. One model, one tissue type, one cancer. If you wanted rare cancers, you were out of luck, because rare cancers don't generate the large labeled datasets that supervised learning demands. This was the same constraint that limited early AI in every domain this series has covered: the architecture could detect patterns, but only the specific patterns it had been trained to see.

The practical impact even at this early stage was real. Labs that adopted digital pathology with AI-assisted workflows reported measurable gains: AI prescreening slides and triaging suspicious cases to the top of the queue, with pathologists confirming the flagged findings. The human still decided. The machine decided what to show them first. Early-adopter labs reported turnaround-time reductions of up to a third, not because the AI was faster at reading, but because it eliminated the wasted effort of a pathologist carefully examining slides that turned out to be benign.

The foundation model era in pathology changed the ceiling starting in 2023 with "Virchow", a collaboration between Paige and Microsoft Research. Virchow was a vision transformer with 632 million parameters, trained through self-supervised learning on 1.5 million whole-slide images from Memorial Sloan Kettering. The critical difference: Virchow was not trained to detect any specific cancer. It was trained to learn what human tissue looks like, in all its variation, across dozens of tissue types and hundreds of disease states. Only afterward was it adapted, with relatively small amounts of labeled data, to specific diagnostic tasks.

Instead of building a separate model for each cancer type, Virchow could be adapted to detect cancers across 16 different tissue types. The pan-cancer detection system achieved a specimen-level AUC of 0.95 for common cancers and 0.93 for rare ones.

That performance on rare cancers is the real headline. Foundation models can recognize an unusual cancer the way an experienced pathologist can: not because they have memorized that exact pattern, but because they understand what normal tissue looks like, and this isn't it. In 2025, Tempus AI acquired Paige for $81 million, gaining control of nearly seven million digitized slides and the Virchow model. The future of computational pathology was not a collection of narrow tools bolted onto a microscope. It was a platform.

The parallel arc in ophthalmology reached its own foundation-model moment in September 2023, when researchers at Moorfields Eye Hospital and UCL published RETFound in Nature: a self-supervised model trained on 1.6 million retinal images. RETFound could be adapted not just to detect eye diseases, but to predict systemic conditions: heart attacks, stroke, Parkinson's disease.

That last sentence deserves a pause.

A photograph of the back of your eye, run through a foundation model, can estimate your risk of having a heart attack.

This is the moment where the story stops being about better pattern recognition and starts being about something much stranger: the human body as a high-dimensional dataset, and the eye as its most accessible sensor.

**The Body as Dataset**

The retina is an anatomical accident that turns out to be a diagnostic goldmine. It is the only place in the human body where you can directly observe both blood vessels and neural tissue without cutting anything open. Ophthalmologists have known this informally for generations. Hypertensive retinopathy, diabetic changes, papilledema: the clinical instinct that the eye is a window to systemic health is ancient. What is new is the formalization of that instinct into a quantitative discipline. The field now has a name: oculomics.

Coined in 2020 by Pearse Keane and colleagues at Moorfields, oculomics applies AI to retinal images to extract biomarkers of diseases that have nothing to do with the eye itself. Deep learning models applied to standard retinal photographs have shown the ability to predict cardiovascular risk, estimate biological age, detect early-stage chronic kidney disease, and identify signatures of Alzheimer's disease. A 2024 study demonstrated that a model called Eye-AD could detect early-onset Alzheimer's and mild cognitive impairment with AUCs above 0.90, by reading subtle microvascular patterns in the deep retinal layers that no human examiner could reliably assess.

But diagnostics is only one dimension. In ophthalmology, AI has also moved into surgical planning and intraoperative guidance. Systems now use machine learning on corneal topography and patient histories to personalize LASIK ablation profiles and provide real-time micro-adjustments during the procedure. In cataract surgery, AI tools recommend IOL type, power, incision placement, and toric alignment based on clinical data and surgeon preferences. These are not autonomous systems. They are copilots, and they represent a different point on the autonomy spectrum from IDx-DR: the AI optimizes, the surgeon executes. Meanwhile, platforms for AI-enabled home monitoring of macular function, visual fields, and acuity are pushing diagnostics out of the clinic entirely, reaching patients through consumer devices. The eye, it turns out, is not just a sensor the doctor reads. It is becoming a sensor the patient wears.

Meanwhile, in pathology, the equivalent moment is pathomics: AI-identified cellular patterns in tissue biopsies that are invisible to the human eye but correlate with treatment response. Foundation models like Virchow are not just detecting cancer. They are predicting biomarker status, things like microsatellite instability and specific driver mutations, directly from routine H&E-stained slides. That matters because molecular testing is expensive, tissue-destructive, and slow. If you can infer the same information computationally from the slide the pathologist was already reading, you accelerate treatment decisions and preserve tissue for cases where molecular confirmation is genuinely needed.

The convergence of these two threads, the eye as a systemic sensor and the tissue slide as a molecular oracle, points toward a single, disorienting conclusion: the diagnostic information was always there, embedded in the images. We just could not see it.

**The Patient on the Table**

Everything I have described so far operates on a comfortable timescale. A retinal scan is analyzed overnight. A biopsy slide is read within days. The pathologist triages a queue. The foundation model runs in the background. None of it is urgent in the way that a surgical procedure is urgent.

But there is one workflow in pathology where time compression is extreme, and it exposes exactly the kind of gap that AI was built to close. That workflow is the intraoperative frozen section.

Here is how it works. A surgeon is operating on a cancer patient. She removes tissue and needs to know, right now, whether the margins are clear. Did she get it all, or does she need to cut further? A runner carries the specimen from the OR to the pathology lab. A technician rapidly freezes the tissue, slices it, stains it, and mounts it on a slide. A pathologist examines it under a microscope and calls the result back to the surgeon. The entire cycle, from excision to answer, is supposed to take 20 to 30 minutes. The patient is under anesthesia the entire time.

The stakes are binary and immediate. A false negative, calling a positive margin clean, means the patient may need a second surgery. A false positive means the surgeon removes healthy tissue unnecessarily. And the pathologist is making this call on a slide that is, by design, worse than what they normally work with. Frozen sections produce artifacts that formalin-fixed tissue does not: ice crystal damage, poor morphology, inconsistent staining. It is the hardest read in pathology, performed under the most time pressure, on the lowest-quality material.

Mohs micrographic surgery, used primarily for skin cancers, intensifies this further. The Mohs surgeon acts as both surgeon and pathologist, excising tissue layer by layer and examining each one for residual tumor before deciding whether to cut again. The procedure can involve multiple rounds, each requiring slide preparation and microscopic review. It is meticulous, effective, and agonizingly slow. Patients wait, awake, while their tissue is processed and read.

From a product manager's perspective, this is a textbook unmet need. The pain is real, the workflow is constrained, and the bottleneck is the same one that limits all of pathology: a human expert reading an image under pressure. The frozen section did what digital X-ray did for radiology. It solved the access-to-the-image problem. But just as digital X-ray ultimately created more studies than radiologists could read, frozen sections created a demand for rapid interpretation that the pathology workforce cannot always meet. The digitization solved one bottleneck and revealed the next.

AI solutions are emerging, but they are not yet where the foundation models are for standard surgical pathology. A 2025 platform described in NPJ Digital Medicine tackled the frozen-section problem end to end: not just classification, but quality assessment of the slide itself and decision support tailored to the artifacts and time constraints of intraoperative tissue. A separate 2025 study in Nature Communications demonstrated AI-augmented cryosection workflows that reduced unnecessary re-biopsies. And there are early-stage foundation models specifically trained on frozen-section data, aiming for multi-center generalization across the messy, artifact-laden images that intraoperative pathology actually produces.

None of these are FDA-cleared products yet. The gap between research performance and clinical deployment is real, and it is the same gap that held back every other domain in this series. The hardware has to be in the OR or adjacent to it. The scanning has to happen fast enough to fit the surgical window. The intended-use labeling has to match what the surgeon actually needs. The mainstream commercial pathology AI vendors, Paige included, have built their products around formalin-fixed, paraffin-embedded tissue in the standard surgical pathology lab. Frozen sections are a different beast, and the infrastructure is not yet in place.

But the trajectory is clear. If you are a builder looking for the next high-impact application of computational pathology, this is where to look: not at the queue of slides waiting in the lab, but at the patient on the table, the surgeon waiting for an answer, and the pathologist trying to read a bad slide under a ticking clock. The frozen section is pathology's real-time system, its operating room. And just like anesthesia's cockpit, it is the environment where AI assistance will matter most.

**The Regulatory Precedent**

IDx-DR pioneered the FDA pathway that every autonomous AI system in medicine will have to navigate. There was no predicate device for an AI that made its own clinical decisions, so Digital Diagnostics pursued a De Novo classification. The choices they made along the way amount to a template.

First, the trial venue. The pivotal study enrolled 900 patients at primary care sites, not ophthalmology clinics. The entire value proposition was specialty-level diagnostics in settings that lacked specialists. By proving the system in primary care, the company showed the FDA that the AI could do what an ophthalmologist could do in a place where no ophthalmologist existed.

Second, the bias analysis. Trial data were stratified by sex, race, and ethnicity, with no significant differences in performance across subgroups. For builders working on foundation models today, this matters enormously: equitable performance across demographics is not an afterthought. It is a regulatory requirement and, increasingly, a prerequisite for payer adoption.

Third, the business model. A new CPT code, 92229, was created specifically for autonomous AI-based retinal imaging at the point of care. The code did not merely pay for the image. It paid for the diagnostic decision.

Fourth, liability. Digital Diagnostics chose to accept medical liability for the AI's clinical decisions, a move that remains nearly unique. The logic was simple: if the system is autonomous, someone has to be responsible for its output. The company decided that someone should be the company.

De Novo clearance, a dedicated CPT code, voluntary liability assumption. Every autonomous AI system in medicine will face some version of this triad: How do you get authorized? How do you get paid? Who is on the hook when it is wrong?

Paige's FDA authorization for digital pathology followed a similar De Novo path. The field is now watching to see whether the broader oculomics applications will seek clearance as diagnostic devices or position themselves as clinical decision-support tools within the physician-in-the-loop paradigm. IDx-DR sits at one end of the autonomy spectrum: the machine makes the call. Paige Prostate sits at the other: the machine highlights, the pathologist decides. Most products will land somewhere in between, and the regulatory framework they choose will define not just their clearance pathway but their reimbursement, liability, and workflow integration.

**Speculative Correlation, or the Next Framingham?**

The next criticism is already forming, and it will sound like this: "Using eye scans to predict brain disease is speculative correlation, not real medicine."

It is a fair-sounding objection. It also reveals a misunderstanding of how every biomarker in medicine started its life.

Cholesterol was just a number in a blood test before the Framingham Heart Study established its predictive relationship with cardiovascular disease. Hemoglobin A1c was a laboratory curiosity before it became the standard metric for diabetes management. PSA was controversial for decades before the field converged on how to use it, and the debate is still not settled.

Every biomarker begins as a correlation that someone has the persistence to validate. The retinal vasculature, directly observable, cheaply imaged, and structurally connected to both the cardiovascular and central nervous systems, is the next frontier. The data is building. The foundation models are maturing. The regulatory precedent exists.

The real question is not whether retinal biomarkers will enter clinical practice. It is who will own the diagnostic platform when they do. Will it be ophthalmologists expanding their scope, primary care clinics adding a camera to the waiting room, or consumer health companies offering retinal scans at the pharmacy?

If the history of this series has taught us anything, it is this: the technology arrives first, the workflow follows, and the arguments about whose scope of practice it belongs to come last.

The microscope is going digital. The slide is becoming a dataset. And the eye, that ancient diagnostic instrument, is being reimagined not as a window to the soul but as a window to everything else.
