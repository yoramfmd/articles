---
title: The Architect
slug: v-the-architect
published: 2026-01-05
excerpt: Thirty years ago, in a small room at the Hebrew University School of Pharmacy in Jerusalem, a group of graduate students was simulating protein structures on Silicon Graphics workstations, the same machines Hollywood used for visual effects.
---

*From molecular search to molecular generation*

In the mid-1990s, I was a medical student at the Hebrew University Faculty of Medicine in Jerusalem, and I had a side career that no one had asked me to pursue. I was the unofficial IT instructor. Faculty members and fellow students needed someone to walk them through DOS commands, word processing, spreadsheets, data management in dBase IV. The machines were a motley fleet: VAX/VMS terminals, bulky IBM PCs, and a few Apple LC IIs that someone had fought hard to procure. Each department chair seemed to be in an arms race for the latest model.

But no lab in the building could match what was happening in a small room at the School of Pharmacy.

There, a group of graduate students worked with Professor Amiram Goldblum on something I could barely comprehend at the time: three-dimensional simulations of protein structures, specifically aspartic proteinases like HIV-1 protease, and the development of algorithms for predicting how protein side chains would arrange themselves in space. The computers were Silicon Graphics Indigo workstations, the same machines Hollywood was using for visual effects. In a medical school where most of us were still learning to format a floppy disk, Goldblum's students were rotating molecular structures on screen and watching atoms settle into configurations that would determine whether a drug candidate could fit into its target.

What Goldblum's lab was building, an algorithm called Iterative Stochastic Elimination, addressed a problem that was, in the precise mathematical sense, intractable. Protein folding and molecular interaction involve combinatorial spaces so vast that no computer could evaluate every option. ISE took a different approach: sample randomly, score the results, eliminate the worst-performing values, and repeat. Each iteration shrank the search space until what remained could be computed exhaustively. It was not brute force. It was intelligent elimination. The algorithm won the American Chemical Society's Computers in Chemistry prize in 2000, earned Goldblum the Kaye Innovation Award in 2017, and contributed to the founding of two companies, Pepticom and RebioticsRX.

I am telling you this story because what Goldblum was doing in that small room in Jerusalem is precisely what every generative biology platform in this article descends from: the computational prediction of molecular structure as a prerequisite for rational drug design. The tools have changed beyond recognition. The problem has not. And the fact that a lab in a pharmacy school in the 1990s was working on the same fundamental challenge that won two Nobel Prizes in 2024 tells you how long this revolution has been building.

Here is a claim you will hear from skeptics this year: AI-designed drugs are vaporware. Lots of press releases, no approved therapies, no proof that computational molecular design translates into medicines that work in human bodies.

It sounds prudent. It is also increasingly hard to sustain.

In June 2025, Nature Medicine published Phase 2a results for rentosertib, a drug whose target and lead molecule were both discovered and optimized using an AI platform built by Insilico Medicine. The system flagged a protein kinase called TNIK, which no one had previously pursued for lung disease, as a novel therapeutic target for idiopathic pulmonary fibrosis. Then it generated a molecule to inhibit that target and optimized it for drug-like properties. The journey from project initiation to preclinical candidate took roughly eighteen months, against an industry average of four to five years. In a small Phase 2a cohort, patients receiving the highest dose showed a trend toward improved lung function while the placebo group declined. For a disease where existing therapies mainly slow the deterioration, this was a notable early signal, though it still requires confirmation in larger trials.

The vaporware narrative was cracking. What happened next in the field of antibody design opened it further.

**The Lock and the Key**

To understand what AI changed in drug discovery, you need to understand the problem it inherited.

A drug works by binding to a specific protein in the body. Think of it as a lock-and-key problem: the protein is the lock, the drug is the key, and the binding depends on three-dimensional shape. Does the molecule fit into the pocket on the protein's surface? Does it grip tightly enough to block or activate the protein's function?

For most of pharmaceutical history, we could not see the lock. Determining a protein's three-dimensional structure required growing crystals and bombarding them with X-rays, a process that could take months or years and did not work for many proteins. Without the shape, drug design was essentially trial and error. Pharmaceutical companies synthesized or acquired hundreds of thousands of compounds, tested each one robotically against the target, and looked for the rare molecule that happened to fit. Hit rates were typically below one percent. The process was industrialized guessing.

Antibodies, the class of drugs at the center of this article, presented a specific version of this challenge. An antibody is a Y-shaped protein produced by the immune system that binds to a specific target, called an antigen, with high precision. Monoclonal antibodies, meaning identical copies of a single antibody produced at scale, became the fastest-growing class of drugs in medicine. Well over a hundred have been approved globally, treating cancers, autoimmune diseases, infections, and more, in a market now valued in the hundreds of billions of dollars annually.

But making a new antibody was agonizingly slow. The traditional process involved immunizing animals, harvesting the antibodies their immune systems produced, then painstakingly engineering those molecules so the human body would tolerate them. The first monoclonal antibody approved for human use, in 1986, was derived entirely from mouse cells. It worked, preventing kidney transplant rejection, but patients' immune systems attacked the foreign protein, causing severe side effects including a dangerous inflammatory cascade called cytokine release syndrome. Much of the early engineering effort in the decades that followed focused on reducing this immunogenicity, one manual redesign at a time.

The fundamental limitation was that drug designers could search through existing molecules, but they could not generate new ones from first principles. They were explorers, not architects.

That changed in 2020.

**The Shape of Everything**

DeepMind, the artificial intelligence laboratory owned by Google's parent company Alphabet, had spent years working on a problem that biologists considered one of the hardest in science: predicting how a protein folds. Every protein is a chain of amino acids that folds into a specific three-dimensional shape, and that shape determines what the protein does. Predicting the shape from the amino acid sequence alone had resisted decades of effort. In November 2020, DeepMind's system, called AlphaFold 2, solved it. Given only a sequence, the model could predict the protein's structure with accuracy rivaling experimental methods.

The impact was immediate. The Protein Data Bank, the global repository of experimentally determined structures, had accumulated roughly 100,000 entries over fifty years. AlphaFold predicted structures for over 200 million proteins and made them freely available. Decades of bottleneck, dissolved in a computation. For drug designers, this meant the lock was no longer a mystery. If you could predict the shape of any protein computationally, you could begin to design molecules that fit it computationally.

AlphaFold 3, released in May 2024, extended the model's reach to interactions between proteins and other molecules, using a type of AI architecture called a diffusion model. Diffusion models learn by adding random noise to real data and training the system to reverse the process, reconstructing coherent structures from chaos. The same approach powers image generators like DALL-E, except here the output is molecular geometry rather than pictures.

The 2024 Nobel Prize in Chemistry recognized the significance. One half went to Demis Hassabis and John Jumper of DeepMind for protein structure prediction. The other half went to David Baker of the University of Washington for computational protein design. Hassabis and Jumper solved the forward problem: given a sequence, predict the structure. Baker solved the inverse: given a desired function, design a protein that performs it. One team gave drug designers the map. The other gave them the drafting tools.

By early 2026, Isomorphic Labs, DeepMind's drug-discovery spinoff, had announced a new internal platform it calls the Drug Design Engine, claiming substantial improvements over AlphaFold 3 on novel targets, with rapid binding-site identification suitable for routine use in active discovery programs. The company is deploying it daily, backed by partnerships with Eli Lilly, Novartis, and Johnson & Johnson valued at billions of dollars in potential milestones.

The trajectory from Goldblum's Silicon Graphics workstation to this moment is thirty years. The problem is the same: predict how a molecule fits into a protein. The scale is unrecognizable.

**From Searching to Generating**

Knowing the shape of the lock was necessary but not sufficient. The next step was learning to generate the key.

Traditional drug discovery searches existing chemical or biological space. Generative drug design creates molecules that have never existed, optimized computationally for a specific target, before anyone synthesizes them in a lab.

In late 2025, Baker's lab published work in Nature demonstrating that fully AI-designed antibodies could bind disease-relevant targets, including influenza and bacterial toxins, with near-atomic accuracy. A majority of tested designs matched their predicted binding pose under electron microscopy. The method works the way image diffusion models do, but for proteins. The system learned what protein structures look like from the entire Protein Data Bank, then learned to generate new structures from random noise, optimized for specific binding targets. Baker's group extended this to the hardest part of the antibody, the flexible loops that determine what it grabs, and showed that generative design could produce functional antibodies no natural immune system had ever created.

The Baker lab subsequently released an even more powerful version of its design software as open-source, free for all researchers. The spin-off company Xaira Therapeutics, co-founded by Baker with approximately a billion dollars in committed capital, is translating these designs toward the clinic.

**The Clinical Proof**

The skeptic's strongest argument was always the translation gap. Proteins behave differently in computation than in a human body. Binding affinity in a lab assay does not guarantee efficacy in a patient. So the real question was never whether AI could design a molecule. It was whether an AI-designed molecule could treat a disease.

By early 2026, the answer is arriving from multiple directions.

Absci has advanced AI-designed antibodies into early clinical trials, including programs in hair loss and inflammatory bowel disease, with molecules taken from computational design directly into human testing without an animal-derived starting point. These represent some of the first fully de novo AI-designed antibodies to enter the clinic.

Generate:Biomedicines has delivered the most advanced clinical milestone. Their lead candidate, GB-0895, is an AI-engineered antibody targeting a protein called TSLP that drives airway inflammation in severe asthma. The platform designed it for ultra-high binding affinity, an extended half-life enabling dosing approximately twice a year, and favorable manufacturability, properties that would be extremely difficult to achieve through conventional methods. Phase 1 data showed sustained suppression of inflammatory markers with a favorable safety profile. Generate has since initiated large Phase 3 trials and is pursuing a public offering. Concept to Phase 3 in roughly four years. Traditional antibody programs typically require four to five years just to reach clinical candidacy.

That is not incremental improvement. It is structural compression of the drug development pipeline.

No AI-designed drug has been approved yet. That needs to be said plainly. Clinical trials exist for a reason. Biology is not computation. Roughly ninety percent of drugs entering clinical trials never reach the market. AI compresses discovery; it does not compress approval. The FDA does not care how you found the molecule. It cares whether it works and whether it is safe.

The honest framing: AI has compressed the front end of the pipeline, the years spent searching for targets and designing candidates, from half a decade to months. Whether that translates into higher trial success rates is a hypothesis under active testing. The early data is encouraging. It is not conclusive. That uncertainty is not a weakness of the technology. It is the nature of drug development, and it is precisely the uncertainty the regulatory system was built to manage.

**The Forward Provocation**

The next criticism will sound familiar: "AI-designed drugs have no long-term safety record. The computational models cannot capture the full complexity of human biology."

Both concerns contain a grain of truth, and both have precedent that should temper the alarm. The safety concern applied to every new drug modality when it first entered the clinic: to monoclonal antibodies after the severe reactions to that first mouse-derived drug in the 1980s, to mRNA vaccines before the COVID-19 pandemic proved the platform could be developed and deployed at unprecedented speed. AI-designed drugs enter the same regulatory gauntlet as every other therapeutic. They do not get a shortcut.

The concern about biological complexity is valid and irrelevant in equal measure. Of course models are incomplete. All models are incomplete. The pharmacokinetic models anesthesiologists use for target-controlled infusion are incomplete. The risk scores cardiologists use for catheter interventions are incomplete. The Framingham equations are incomplete. The question is not whether the model is perfect. It is whether the model, with its imperfections, produces better outcomes than the alternative. In drug discovery, the alternative costs billions per approved drug, takes over a decade, and fails the vast majority of the time.

**The Convergence**

This is the last article in this series, and it is time to say what five articles have been building toward.

Each article traced the same arc within a different clinical domain. In radiology, from pixel-matching algorithms to a foundation model triaging fourteen acute conditions across the whole body. In cardiology, from diagnostic headers printed on ECG paper to autonomous catheters guided by reinforcement learning. In anesthesia, from the integrated cockpit display to closed-loop systems titrating anesthetic depth in real time. In pathology and ophthalmology, from digitized slides to foundation models that predict systemic disease from an image of the eye. In drug discovery, from Goldblum's ISE algorithm running on a Silicon Graphics workstation to diffusion models generating novel antibodies from noise, with those antibodies now in advanced human trials.

The architectural progression is identical in every case: hand-coded rules gave way to supervised models on narrow datasets, which gave way to foundation models that learn general representations and generalize across tasks. The domain changes. The physics differs. The regulatory pathways differ. But the underlying pattern is one pattern, and it has been developing for fifty years.

The people who say AI in healthcare is failing are looking at the last five years. They see pilot projects that stalled, overpromised products that underdelivered. They are not wrong about the failures. They are wrong about what the failures mean.

The people building the next generation are looking at the last fifty years. They see a continuous engineering program that has reached its tipping point, the moment when the models became general enough, the data infrastructure mature enough, and the clinical evidence compelling enough to shift from narrow tools to general-purpose reasoning substrates. A single model family can now parse medical images, interpret physiological waveforms, simulate drug-target interactions, and generate novel molecules. These are not five separate revolutions. They are one.

The stethoscope was invented in 1816 because a physician named René Laennec was too uncomfortable to press his ear against a young woman's chest. He rolled a sheet of paper into a tube, placed one end on her thorax and the other to his ear, and heard the heartbeat more clearly than he ever had before.

Two hundred years later, the silicon stethoscope was built because the data grew too vast for any human sense. Too many pixels on the scan. Too many waveforms on the monitor. Too many molecules in the chemical library. Too many slides in the queue. The impulse is the same: build a better instrument, and medicine follows.
