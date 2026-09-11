---
title: "The Framework Assumes Someone Is Watching"
slug: the-framework-assumes-someone-is-watching
published_at: 2026-04-13T01:28:00.000Z
custom_excerpt: "Healthcare regulation still assumes a clinician is watching the AI before anything happens. That assumption worked when AI meant a score on a screen. It breaks down when AI runs continuously in a patient's pocket, shaping decisions no one reviews."
tags: [healthai]
feature_image: https://storage.ghost.io/c/e6/05/e605b234-3cc8-4fe4-97bb-2bb55b18b8fb/content/images/2026/04/Gemini_Generated_Image_jb0zbjjb0zbjjb0z.png
source: ghost
---

# The Framework Assumes Someone Is Watching

*Alternative title: The Floor Is Missing*

---

Healthcare regulation still assumes a clinician is watching the AI before anything happens. That assumption worked when AI meant a score on a screen. It breaks down when AI becomes a continuous presence in a patient's life, shaping decisions no human ever reviews.

In my last piece I described how healthcare AI gets built in MVP layers, stacking test balloons into load-bearing structures, with governance always deferred to the next sprint. That was the view from inside the product team.

This is the view from outside: the regulatory framework that was supposed to catch what product teams miss has a structural gap, and it is largest where most patients actually are.

---

## The Assumption Nobody Examined

The FDA's Clinical Decision Support Software Guidance, updated in January 2026, is the most current statement of how the United States regulates clinical AI. It is careful and detailed, and it rests on a single foundational assumption: a qualified clinician will independently review the AI's recommendation before acting on it. Software that meets this standard is "Non-Device CDS," exempt from medical device regulation. Software that bypasses or replaces that clinical review is a regulated device. The legal term for this requirement is Criterion 4.

The logic is sound for its era. When the framework was built, "AI in healthcare" meant a sepsis score on a screen. A number. A risk threshold. An alert that a nurse sees, evaluates, and either acts on or dismisses. The assumption holds when the AI makes one recommendation, the clinician reviews it, and a human decision follows.

It does not hold when the AI is a continuous presence in someone's pocket, shaping behavior through daily nudges that no clinician will ever see. It does not hold when the AI is an orchestrating system in an ICU, coordinating attention across multiple data streams in real time. And it does not hold when the system was built in MVP mode, as I described last time, where governance was never designed because nobody planned to reach this scale.

The FDA's guidance reflects part of this tension. The January 2026 update explicitly states that software intended for time-critical decisions fails Criterion 4, because there is "not sufficient time for independent review." The agency names automation bias. What the guidance does not yet provide is a framework for what happens when the core assumption breaks. The problem is named. The answer is not written.

---

## Two Extremes, One Gap

Look at where regulatory attention actually lands.

At one end: consumer mental health chatbots. Utah's HB452, effective May 2025, is the most explicit regulatory response to date. Disclose that you are AI. Document your safety practices. File a written policy. In exchange, you receive a safe harbor against claims of unlicensed professional practice. The logic is access. Half the United States lives in a mental health workforce shortage area. People are using AI for emotional support whether regulators permit it or not. Utah chose to shape that behavior rather than prohibit it.

At the other end: AI orchestration in intensive care. Clinical researchers are now documenting what happens when AI moves from narrow, single-purpose tools to generalist systems that coordinate multiple data streams, reprioritize clinical attention, and influence decisions across entire care teams. The conclusion is consistent: device-centric regulatory frameworks, built to evaluate discrete products with defined intended uses, cannot evaluate systems where clinically significant behavior emerges from the interaction between components that were each approved individually.

Both ends are visible. Both are receiving scholarly and regulatory attention. Both have documented arguments for why the existing framework falls short.

The middle has none of this.

---

## The Unprotected Middle

The middle ground is where most patients actually live. Chronic disease management apps. Remote cardiac monitoring. Post-discharge follow-up tools. Medication adherence platforms. Symptom triage. Behavioral health support for non-acute conditions.

These tools interact with patients over weeks, months, sometimes years. They are the most persistent AI presence in a patient's life. They operate largely outside device regulation because they avoid making diagnostic claims, positioning themselves under the "general wellness" category that the FDA has historically chosen not to enforce.

The structural problem is that these tools are not static. They update. The models drift. The patient population shifts as the product scales. Feature definitions change when upstream systems update their formats. Performance degrades silently, over months, with no monitoring requirement and no regulatory trigger.

The FDA's own guidance makes clear that consumer-facing software, tools that support patients rather than clinicians, is categorically excluded from the Non-Device CDS exemption. These apps are technically devices. The FDA exercises enforcement discretion and does not regulate them as such, as long as they stay within general wellness framing.

That enforcement discretion is not nothing. It is a reasonable policy choice for genuinely low-risk tools. But enforcement discretion is not governance. It does not require post-market surveillance. It does not mandate drift monitoring. It does not create accountability when the model that was working in year one is quietly failing in year three for a subpopulation that was underrepresented in the original training data.

There is no durable oversight mechanism watching this class of tools. And most of them were not designed by teams who expected one to exist.

---

## What It Looks Like from the Inside

I have spent years building AI products in regulated and semi-regulated healthcare environments. The honest answer to "why didn't you build the governance layer?" is almost never negligence. It is sequencing.

You build the MVP to validate the clinical workflow. Then you build the next layer because the first showed promise. Then you are three layers deep, with real patients on the product, real contractual commitments to health plan customers, and a governance backlog growing faster than the roadmap can address it. You are not ignoring safety. You are running at a pace that makes comprehensive governance feel like a cost the company cannot afford until next quarter.

The regulation was supposed to create the forcing function, defining the floor below which no MVP could ship. In most clinical contexts it does. In the middle ground it does not, because the pathway around device regulation is well-understood, the general wellness carve-out is broad, and enforcement discretion creates a permissive environment that rational product teams rationally use.

The frameworks are moving. Healthcare AI is moving faster.

---

## The Minimum That Is Missing

Healthcare is the most regulated industry on earth because failure here is different in kind, not just in degree. A failed payment system costs money. A medication adherence platform that drifts silently for eighteen months, underperforming for a patient subgroup nobody is monitoring, costs something that cannot be recovered.

In my last article I said that minimum viable without minimum viable safety is just "minimum." That was the engineering argument.

This is the governance argument: the floor beneath the safety minimum is still missing for most of the middle ground of healthcare AI. Not because regulators lack intent. Because the framework was designed for a different era, when "AI in healthcare" meant a number on a screen and a physician was always in the loop reviewing it before anything happened.

That physician is not always in the loop anymore. In some architectures, no human is.

We are building for an era of continuous, ambient, agentic AI. We are regulating the era of discrete clinical decision support. The gap between those two eras is where most of today's patient-facing AI actually lives.

And minimum is still not good enough when patients are at the other end of the pipeline.

---

*This article is part of an ongoing series exploring how AI is integrating into medical practice and the systems built around it.*
