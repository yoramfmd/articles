---
title: The House of Cards: Why MVP Thinking Is Breaking Healthtech
slug: the-house-of-cards-why-mvp-thinking-is-breaking-healthtech
published: 2026-02-28
excerpt: MVP was meant to test ideas, not become architecture. Now, we've started stacking prototypes into production systems nobody designed as systems. When one layer fails, the whole structure drifts silently. In medicine, that's not technical debt. It's patient risk.
---

The MVP used to be a test balloon. You sent it up, watched where the wind took it, and then built the real thing. Somewhere in the last decade, we stopped building the real thing. Now we just send up more balloons and call it architecture.

It's not hard to see how we got here. Markets move faster. Planning cycles compress. The team that spends eighteen months engineering a robust platform loses to the team that ships a demo in six weeks and iterates. So we iterate. MVP one validates a workflow. MVP two consumes the output of MVP one. MVP three orchestrates the first two. Each one makes sense in isolation. Each one passes its quarterly review. And before anyone draws an architecture diagram, there's a compound system in production that was never designed as a system. A house of cards, each card labeled "MVP," each one load-bearing.

In most industries, this is expensive and embarrassing. In healthcare, it's dangerous. Because in healthcare AI, MVP has quietly shifted from a learning tool to an architectural philosophy, and that shift is producing systems where nobody can answer a basic question: what happens when one layer fails?

## The MVP Was Never Meant for This

The Minimum Viable Product, as Eric Ries defined it, is elegant in its original context. Build the smallest thing that validates your assumptions. Measure. Decide: persevere, pivot, or stop. The key word in that sequence is "decide." The MVP was a decision-making tool, not a delivery strategy. It assumed that after the experiment, you would either kill the idea or do the real engineering.

That assumption no longer holds. In today's enterprise, "stop" is never on the table. The business case is already sold. The headcount is allocated. The customer advisory board has seen the deck. The MVP quietly stops being a Minimum Viable Product and becomes a Most Visible Placeholder on the roadmap. The decision gate gets skipped, "persevere" is the only acceptable outcome, and the test balloon becomes a load-bearing structure.

In my years as an integration consultant, I watched this same pattern destroy ERP rollouts and cloud migrations. But there, a poorly integrated system meant delayed invoices or duplicate records. Painful, recoverable. In healthcare AI, the consequences are qualitatively different: clinical systems that degrade silently, bias that compounds invisibly, and safety gaps that nobody monitors because nobody designed the monitoring.

## The Stacking Problem

Consider how a typical healthcare AI "solution" actually gets built. (Sometimes we call these MVPs a "proof of concept," which sounds even more temporary but somehow ends up just as permanent.)

Phase one: a predictive model. A deterioration risk score, trained on retrospective EHR data from a single institution. It validates well. The MVP ships. Clinicians see alerts. The COO issues a press release. Everyone moves on to phase two.

Phase two: a second model uses those risk scores as input, maybe to recommend interventions or prioritize nursing workflows. This model was trained assuming the upstream score is stable and calibrated. Nobody wrote that assumption down, but everything depends on it.

Phase three: an orchestration layer routes both models' outputs into dashboards, notification systems, and documentation workflows. Its own logic, its own failure modes, its own silent assumptions about the reliability of everything beneath it.

Three test balloons, each one tethered to the last, none of them rated for the weight they're carrying.

Now ask: what happens when the upstream model drifts? When the patient population shifts after a service line expansion? When the EHR vendor updates an export format and a feature silently changes meaning?

The house falls. Not dramatically, but quietly, over months, because nobody built cross-layer monitoring and nobody is accountable for the system as a system.

This isn't hypothetical. The Epic Sepsis Model, deployed across hundreds of hospitals, was shown in an external validation study to have poor discrimination and calibration in real-world settings, far below the performance its developers reported. That was a single layer. Imagine the failure modes when three layers of that quality depend on each other.

## The Price of the Cards

If the clinical risk doesn't get your attention, the economics should. Research estimates that the average global enterprise wastes over $370 million annually on technical debt and legacy system maintenance. Roughly 78% of IT decision-makers agree that what they spend maintaining legacy debt could be better used on projects that actually drive value.

And that's the steady-state cost. The acute cost is worse. In 2012, Knight Capital deployed a software update that accidentally reactivated dormant code. In 45 minutes, erroneous trades cost the firm $460 million. The root cause wasn't a bad algorithm. It was architectural negligence: layers of code stacked over years, nobody accountable for the compound system, no monitoring to catch the cascade.

Now transplant that into a clinical workflow where the downstream consequence isn't a trading loss but a missed deterioration signal, a delayed intervention, or a biased risk score silently widening a disparity. Same negligence. Higher stakes.

## "Viable" Has to Mean Something

In consumer software, "viable" means a user will try it. In healthcare AI, the word needs to carry real weight. A healthcare MVP is not a toy prototype you iterate on until it works. It's a production-grade slice: shippable, supportable, and review-ready for real clinical environments. The distinction matters because a prototype teaches you about feasibility, while a production-grade slice teaches you about clinical reality.

This isn't philosophical. Regulators already agree. The EU AI Act imposes lifecycle risk management and post-market monitoring on high-risk medical AI. The FDA's PCCP framework pre-authorizes iterative updates, but only with predefined validation protocols and impact assessments. The US QMSR, effective February 2026, incorporates ISO 13485's system-level quality controls. The message from every jurisdiction is the same: if you want to iterate on clinical AI, you must design the governance before you ship the first version, not after the third.

None of these frameworks are compatible with "ship now, add quality later." And yet the MVP pressure persists. Why? Because health tech companies need traction for investors. Enterprise vendors need AI demos for health system buyers. Health systems need innovation stories for their boards. Everyone needs something to show by quarter's end. The MVP becomes a Minimum Viable Promise, just enough to close the deal, just enough to renew the contract, just enough to keep the board convinced that AI is happening. The house of cards keeps going up because nobody gets promoted for saying "we need to stop and design the architecture."

## What "Learn Fast" Actually Looks Like in Healthcare

I'm not going to argue that MVPs are wrong for healthcare. The uncertainty they address is real. We genuinely don't know how a deterioration model will behave until it meets actual clinical workflows. Sitting in a lab for five years running retrospective studies is its own form of negligence.

But "learn fast" doesn't mean "ship fast." It means designing the learning to be safe.

The most promising pattern is what the literature calls silent trials. The model runs on live data in the real environment, but its outputs are hidden from clinicians and don't influence care. You get the real-world signal: pipeline failures, drift, population mismatch, calibration decay. You get it prospectively. And you get it without exposing a single patient to an unvalidated algorithm.

After silent mode: a controlled pilot. Restricted sites, human-in-the-loop, explicit safety thresholds, and a real decision gate. Not "should we build the next layer?" but "does the evidence support expanding exposure?"

This is still fast. It's just not reckless. And it produces something an MVP stack never does: an evidence trail that a regulator, a clinical governance committee, or a malpractice attorney can actually evaluate.

## The Interoperability Lesson We Refuse to Learn

I went to medical school in the late 1990s. The promise was that electronic health records would unify clinical data and transform care. What we got was decades of fragmented systems, incompatible data models, and a cottage industry of integration middleware.

We built FHIR, OMOP, and SNOMED CT to fix that mess. Years of painstaking standards work, driven by the hard-won realization that you cannot bolt interoperability onto systems that were never designed for it.

Now look at what we're doing with AI. Each model trained on its own data slice. Each pipeline built to its own spec. Each MVP scoped to its own use case, with no shared semantic layer, no common data contracts, no architectural vision for how the pieces compose.

We are rebuilding the interoperability crisis from scratch. One MVP at a time.

## Redefining "Minimum"

The alternative to the house of cards is not waterfall. It's not eighteen-month release cycles and 400-page requirements documents. It is engineered iteration: small scope, full lifecycle governance, designed decommissioning. A slice of architecture, not a slice of functionality.

That means redefining what "minimum" protects.

**Minimum viable safety.** Before any clinical exposure, even in silent mode, define the risk management, failure modes, escalation paths, and monitoring. This isn't bureaucracy. It's the clinical equivalent of checking the anesthesia machine before induction. I've done that check a few hundred times. It never once felt like overhead.

**Minimum viable architecture.** Before the second model goes on top of the first, define the data contracts between them. Define what happens when the upstream component degrades. Embed the governance into the pipeline, automated compliance checks, model registries, drift monitors, not as a separate review committee that meets quarterly. If you can't answer how your layers fail together, you don't have a platform. You have two demos duct-taped together.

**Minimum viable evidence.** At each stage, offline to silent to pilot to scale, define what evidence justifies proceeding and what triggers a stop. Make "stop" a real option. Not a theoretical one that nobody has the courage to use.

**Minimum viable honesty.** Call things what they are. If the build exists to demo capability to a buyer, call it a demo and treat it as disposable. If it exists to test a clinical hypothesis, call it an experiment and design it as one. If it exists to run in production, call it engineering and invest accordingly. The dysfunction starts when MVP language lets us avoid admitting which of these we're actually doing.

## The Window Is Still Open

I started my career watching computational drug design run on Silicon Graphics workstations in a Jerusalem research lab. Healthcare AI has always been a long game dressed up in short-term hype.

We are at a genuine tipping point. The models are capable. The data infrastructure is maturing. The regulatory frameworks are converging on lifecycle governance that actually matches how AI behaves in the real world. But tipping points go both directions.

If we keep stacking MVPs and POCs into architectures nobody designed, optimizing for demo velocity over system integrity, we will produce the high-profile failures that set this field back by a decade. We've already seen the previews: the Epic sepsis model that didn't generalize, the surgical navigation system that triggered recalls, the cost-proxy algorithm that encoded racial bias into risk prediction. Knight Capital lost $460 million in 45 minutes from stacked code nobody owned. In healthcare, the currency isn't dollars. It's trust. And trust, once lost in a clinical setting, doesn't come back in 45 minutes. It doesn't come back in 45 months.

The house of cards is not inevitable. But it is the default. Changing it requires saying what most of us already know: in healthcare, "minimum viable" without "minimum viable safety" is just "minimum."

And minimum is not good enough when patients are at the other end of the pipeline.
