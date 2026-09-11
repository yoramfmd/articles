---
title: "Utah Climbed the Autonomy Ladder. Nobody Designed the Rungs."
slug: utah-climbed-the-autonomy-ladder-nobody-designed-the-rungs
published_at: 2026-04-30
custom_excerpt: "Utah just became the first US state to let an AI autonomously renew prescriptions. The legal debate is real. The design question nobody is asking is more important: who designed the rungs on the autonomy ladder before the climb began? "
tags: [healthai, pm]
feature_image: https://storage.ghost.io/c/e6/05/e605b234-3cc8-4fe4-97bb-2bb55b18b8fb/content/images/2026/04/ChatGPT-Image-Apr-30--2026--10_37_08-AM.png
source: ghost
---

# Utah Climbed the Autonomy Ladder. Nobody Designed the Rungs.

I have never been to Utah, but it is certainly on my list. The Mighty Five national parks. Zion, Bryce, Arches, Canyonlands, Capitol Reef. A landscape unlike anywhere else in the world.

But recently Utah became the first US state to formally approve an autonomous AI agent for prescription renewals, running a real clinical experiment in the real world.

Not a sandbox. Not a proof of concept. Not a demo for a conference. An autonomous AI system, built by a startup called Doctronic, that renews prescriptions for 192 chronic disease medications, including blood thinners, thyroid replacements, and antidepressants, without a physician reviewing each decision.

The design: a physician reviews the first 250 AI renewal decisions. After that, the system operates autonomously.

Most of the coverage has focused on the legal questions. The New England Journal of Medicine published a perspective piece this week asking whether Doctronic's system qualifies as an FDA-regulated medical device and whether an algorithm can legally be a "practitioner." There is also a federal prescribing law question: current statute requires a licensed practitioner to authorize refills, and whether an AI can qualify as one is genuinely unsettled. Utah's regulatory sandbox gave Doctronic a state-level waiver, but federal law is not waived by a state sandbox. The FDA's own framework for clinical decision support requires that a qualified clinician independently review AI output before acting. Utah's design, 250 supervised renewals and then autonomy, is one of the first state-sanctioned production systems to bypass continual clinician review by design rather than by drift.

Those are real questions. They are not the most important ones.


---

**The rungs were not designed.**

The 250-review threshold is a count. It is not a safety criterion. It does not measure whether the AI correctly identifies the patients for whom autonomous renewal is inappropriate. It does not measure escalation quality. It does not measure what happens when a patient's clinical status has changed since the last visit. It measures how many times a physician said yes.

The autonomy ladder framework I have been writing about holds a simple idea: agentic systems should move from suggesting to acting only after demonstrating competence at each step, with a defined path back down. Movement up the ladder is supposed to be earned, not scheduled. Earned means demonstrated competence in the specific failure modes that matter for this decision type. Scheduled means a number was picked, the count was reached, and the human was removed.

Utah scheduled it.

We have one well-studied precedent for autonomous AI in clinical decision-making: closed-loop insulin delivery systems, sometimes called the artificial pancreas. They work. But they work because real-time physiological feedback is built into the architecture. The sensor reads blood glucose continuously. When the model acts on bad data or makes an error, the body signals it within minutes, and the system corrects. The feedback loop is the recovery workflow. Doctronic has no equivalent. A patient whose thyroid function has changed since their last visit generates no real-time signal the system can read. The error propagates silently, across renewal cycles, until a clinician or a lab result catches it. That gap is not only a clinical concern. It is a product design gap. The absence of a feedback-grounded recovery workflow is an artifact that was never built.


---

**Then came the prompt injection.**

AI security researchers discovered that the Doctronic system, the same one autonomously renewing blood pressure and thyroid medications for real patients, could be manipulated through the conversation interface. The reported results: the system was tricked into spreading vaccine conspiracy theories, recommending methamphetamine as treatment, and tripling a prescribed pain medication dosage.

The researchers said the flaws persisted after they notified Doctronic.

This is not a theoretical risk. This is a production system, deployed to real patients, without documented input trust classification. Every content source that reaches an agentic system, including what the patient types into the chat, needs a trust tier. Untrusted content cannot trigger high-consequence actions without explicit human confirmation. Input trust classification is a product design obligation, not a security engineering afterthought. The team that shipped this system made a decision by not making one.


---

**The medical board found out after launch.**

The eleven physicians on the Utah Medical Licensing Board said they were not consulted or notified about the program until after it was already live. Their letter asked for an immediate suspension. The state dismissed it.

As a clinician who used to prescribe medication and be accountable for the results, I understand exactly where the medical board is coming from. Prescribing is not a transaction. It is a clinical judgment that carries personal liability and professional accountability. Removing the physician from that loop, after 250 renewals, because the count was reached, is not a governance model any practicing clinician would recognize.

As a product manager designing agentic solutions now, I am genuinely happy to follow this experiment and learn from it. The underlying problem Utah is trying to solve is real: patients struggle to get timely prescription renewals because clinicians are scarce and overwhelmed, and poor adherence to chronic disease medications carries a measurable mortality cost. Utah is doing something the rest of the industry is only talking about. The feedback will be real, the stakes are real, and the documentation, as you will see below, is more transparent than anything the enterprise software world produces. 

I just hope no one gets hurt while we find out.


---

**Why healthcare is the northstar for agentic AI.**

While most enterprise AI teams are running single-agent proofs of concept in controlled environments, Utah shipped a full production autonomous actor into the real world, operating on real patients with real clinical consequences.

There is something the tech industry should notice about how this story surfaced. The NEJM published a peer-reviewed perspective within months of launch. Security researchers published their findings with specific, reproducible test cases. The medical board's letter is a public document. The state's response is a public document. Healthcare has a transparency infrastructure for failure that the enterprise software industry does not come close to matching. We treat post-mortems as optional. Healthcare treats them as professional obligation.

That is not because healthcare is more virtuous. It is because the cost of hiding failures is higher, and the accountability mechanisms are older and harder to route around. When an agentic system touches a patient, someone has to sign their name to it. That discipline is exactly what enterprise AI product teams are going to need, and most of them are not building it.


---

**What this means for PMs building agentic systems.**

The autonomy ladder is real, and it will be climbed in your product. The question is whether the rungs were designed before the climb began.

Before any agentic feature moves from supervised to autonomous, four design artifacts need to exist: a documented autonomy boundary, an approval moment that contains actual decision information, an audit surface built from observable actions rather than the model's own explanation of what it did, and a recovery workflow that is a named operational process rather than an error message.

Utah gave us some of the clearest evidence yet of what happens when a clinical agentic system is promoted up the autonomy ladder on a schedule rather than a safety criterion.

There is a fifth artifact most teams never get to: the demotion trigger. What causes the system to move back down the ladder? What pattern of errors, what volume of edge cases, what drift in clinical context forces a return to supervised mode? Without a defined demotion trigger, autonomy is a one-way door. The system climbs and never descends, regardless of what happens in production. The Doctronic mitigation agreement is a public document. I have read it. A demotion mechanism is not described.

The Mighty Five will still be there when I finally get to Utah. The lesson from Doctronic should not have to wait that long.


---

*This article is part of an ongoing series on AI product design, healthcare data, and the human side of technology adoption.*


---

## Sources

1. Gerke S, Parikh RB, Cohen IG. Utah's Prescription-Renewal Pilot Program — Autonomous AI Managing Patient Care. *N Engl J Med.* 2026;394(16):1561–1563. https://www.nejm.org/doi/10.1056/NEJMp2601148
2. Utah medical board calls for immediate suspension of state's AI doctor experiment. *STAT News*, April 24, 2026. https://www.statnews.com/2026/04/24/doctronic-ai-doctor-pilot-utah-face-backlash-medical-board/
3. Utah dismisses medical board call to halt its pioneering AI prescription program. *KUER*, April 28, 2026. https://www.kuer.org/health/2026-04-28/utah-dismisses-medical-board-call-to-halt-its-pioneering-ai-prescription-program/
4. Medical Licensing Board calls for suspension of Utah pilot program using AI to refill prescriptions. *Utah News Dispatch*, April 28, 2026. https://utahnewsdispatch.com/2026/04/28/medical-licensing-board-calls-to-suspend-program-using-ai-to-refill-prescriptions/
5. NEWS RELEASE: Utah and Doctronic Announce Groundbreaking Partnership for AI Prescription Medication Renewals. Utah Department of Commerce, January 6, 2026. https://commerce.utah.gov/2026/01/06/news-release-utah-and-doctronic-announce-groundbreaking-partnership-for-ai-prescription-medication-renewals/
6. Utah's Experiment With AI-Driven Prescription Renewals. Stanford HAI, March 19, 2026. https://hai.stanford.edu/research/utahs-experiment-with-ai-driven-prescription-renewals
