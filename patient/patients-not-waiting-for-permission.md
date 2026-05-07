# Patients Are Not Waiting for Permission

A patient arrives at a consultation with a differential diagnosis her AI has already generated. She has interpreted her symptoms, identified conditions worth ruling out, and formed a plan before she sat down.

The Lancet published a piece this month on "the rise of the AI-empowered patient." I read it as both a physician and a product manager, and I must say, I was surprised it was not published much earlier.

---

## We Have Been Doing This Our Whole Careers

Before any clinician expresses concern about patients using AI to self-diagnose, we should acknowledge something we rarely say out loud.

Every medical student and every physician has done exactly this. You notice an unusual symptom, an unexpected finding, a clinical situation you have not encountered before, and before you can reach a colleague or see a specialist, you run your own differential. You open a textbook. You search PubMed. You check UpToDate. You map your findings against what you know and what you can quickly learn, while waiting days or weeks for an expert who can help you make sense of it.

When I had to see another physician, I came prepared. I had done the reading, run the possibilities, and organized my thinking the same way I would before presenting a complex case.

---

## The Knowledge Monopoly Is Over

The Lancet paper makes a point that is overdue: AI has broken the physician knowledge monopoly. For centuries, medical knowledge was held almost exclusively by clinicians. The internet challenged that. LLMs have dismantled it.

Patients now have access to detailed, conversational medical guidance at any hour, in any language, at no cost. And a KFF survey from March 2026 confirms the scale: 32% of US adults are already using AI for health information or advice. The uninsured use it at nearly twice the rate of the insured. Among AI health users ages 18 to 29, 38% cite no provider or lack of access to an appointment as a major reason. One-third of AI health users with household incomes under $40,000 cite cost.

For many of these patients, AI is not supplementing care. It is replacing it.

---

## A Generation That Does Not Wait for Mediators

It is also worth understanding who we are talking about when we describe the AI-empowered patient.

We are describing a generation that manages its own investment portfolio without a financial advisor, trains with an AI coach without a personal trainer, and handles its own legal research before deciding whether it needs a lawyer. Self-sufficiency through technology is not a workaround for this generation. It is the default mode. The health system is one of the last institutions that still treats the absence of a professional intermediary as a problem to be corrected rather than a behavior to be understood.

And the tools available to these patients have moved far beyond reading articles online. A patient today can monitor her heart rate variability, blood oxygen, sleep architecture, and continuous glucose levels from a device on her wrist. She can order blood panels, urine analysis, throat cultures, and viral antigen tests at home. She can access genetic testing spanning pharmacogenomics, brain methylation pathways, and full genome sequencing. She can schedule a privately offered whole-body MRI or CT scan without a physician referral.

She is not arriving at the consultation with a question. She is arriving with data, and increasingly with an AI-interpreted analysis of that data.

---

## What the Office Visit Is For Now

When that patient finally sits down across from a physician, something has already happened that medicine has not yet fully reckoned with.

She has spent hours, possibly days, in conversation with an entity that was patient, available at any hour, never rushed, and consistently confident. The AI did not make her wait three weeks for an appointment. It did not charge her a copay. By the time she reaches the examination room, she has a working hypothesis, a set of questions, and in many cases a plan she is hoping the physician will ratify.

The physician now has two choices, and only one of them sustains the relationship.

The first is to function as a trusted continuum: someone who takes what the patient has learned seriously, adds clinical judgment, catches what the AI missed or overstated, and helps her navigate to the next step. This positions the physician as the person who makes the AI's work meaningful, who brings accountability and consequence to a process that otherwise has none.

The second is to become a friction point: the gatekeeper who questions the patient's sources, retreats to authority, and treats AI-generated thinking as something to be corrected rather than engaged. That physician will lose that patient, not dramatically but quietly. She will come back only when she has no choice.

The medical community also needs to be honest about what the remaining reasons to visit the clinic actually are. If continuous monitoring, at-home diagnostics, genetic testing, and AI interpretation can handle the information layer, the gaps that still bring patients in are specific: procedures and imaging that cannot yet be done privately, laboratory tests that require clinical ordering, referrals that gatekeep specialist access, prescriptions that still require a licensed physician. These structural dependencies are real, but they are not permanent.

The monetary dimension is the hardest thing to say plainly. Many younger patients are on high-deductible plans or carry no insurance at all. They have already received what feels like a thorough consultation for free. When they choose to pay for a clinical encounter, they need to feel it delivered something AI could not: a judgment call that required examination, a referral that opened a door, a finding that changed the picture. If the visit consists largely of re-explaining what the AI already told them, that patient has paid to have her research repeated back to her. She will not make that mistake twice.

That is the biggest gap in the current system. Not that patients are using AI. But that medicine has not yet defined what the clinical encounter offers that AI cannot, and has not designed the visit around delivering it.

---

## What Product Builders Need to Hear

This is where the PM in me needs to say something the Lancet paper cannot.

The AI these patients are trusting was not built for them. Healthcare AI has been developed predominantly on data from insured, English-speaking, connected patients with regular access to care. The populations turning to it most heavily now are largely absent from the training sets that shaped its outputs.

There is a deeper version of this problem in the direct-to-consumer diagnostic layer. A patient arrives with continuous glucose data, a month of sleep architecture, and an AI-interpreted whole-body MRI. Each of those data streams was analyzed by a model trained on something. The question is: trained on whom, validated on which population, and calibrated for what baseline? These are not questions the consumer-facing product surfaces, and most patients will not know to ask them.

I have spent years building data systems designed to make AI trustworthy: ensuring context travels with data, that governance is embedded in architecture rather than bolted on, and that systems reasoning over clinical data reflect the populations they are meant to serve. The challenge in consumer healthcare AI is the same problem at far greater scale, with much less institutional accountability.

When a patient asks an AI whether her symptom is serious, the quality of that answer depends on whose experience shaped it. Most of the time, neither the patient nor the clinician she eventually sees will know the answer.

---

## The Obligation That Follows

The medical community is having an important conversation about AI. About governance, trust, equity, and risk. It is happening on every major stage, in journals, at conferences, in policy rooms. The debate is serious and the people having it are serious.

The problem is that most of the audience has already left. They are watching a different show, and by all available evidence, they are enjoying every moment of it.

Empowerment is not just access. A patient who receives a confident but poorly calibrated AI response and acts on it without follow-up is not empowered. She is exposed.

The AI-empowered patient is already here, arriving not just with ChatGPT summaries but with wearable data, home lab results, and privately acquired imaging. Clinicians need to meet her where she is. Health systems need to stop treating this as deviation and start treating it as legitimate care behavior that deserves infrastructure, literacy support, and accountability.

The people building these systems need to ask a harder question than "does it work." For whom does it work, on what evidence, and what happens to the person it gets wrong.

That is not a technology question. It is a design obligation.

---

*Sources: Riggare S, Sundemo D, Lewis M, Blease C. Patients are not waiting for permission: the rise of the AI-empowered patient. Lancet Prim Care. 2026. KFF Tracking Poll on Health Information and Trust: Use of AI for Health Information and Advice, March 2026.*
