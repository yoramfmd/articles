# Customer Data Platforms in Healthcare: Necessary Infrastructure, Dangerous Autonomy

Healthcare is adopting Customer Data Platforms at scale. Vendors promise unified patient views, personalized engagement, and real-time orchestration across fragmented systems. Health systems are buying in, eager to close care gaps and improve experience.

This should make us cautiously optimistic, not because CDPs are bad technology, but because healthcare hasn't yet decided what they're allowed to decide.

### What Is a Customer Data Platform?

A Customer Data Platform unifies customer data across channels to enable modeling, targeting, and analysis. Core capabilities include:

**Customer data object management**: Creating unified profiles from person-level data through deterministic or probabilistic identity resolution, governing related objects like audiences, campaigns, and scores.

**Data collection**: Ingesting first-party data from multiple sources and formats, online and offline, in real time, including anonymous and known identifiers, behaviors, and attributes.

**Activation**: Sending segments to engagement platforms and increasingly functioning as centralized decision-making tools supporting real-time personalization and next-best-action recommendations.

**Analytic reporting**: Performance and propensity analysis at attribute, profile, or segment levels.

In retail and marketing, CDPs succeed because the optimization target is clear: increase engagement, conversion, retention, and satisfaction. Healthcare cannot be optimized like a consumer domain, because engagement is not the same as benefit, and need is not the same as responsiveness.

### The Green Zone: Where CDPs Function as Infrastructure

Healthcare IT is a graveyard of fragmented systems. The legitimate role of a CDP is to provide connective tissue, operating as unification infrastructure rather than an autonomous decision engine.

**Identity Resolution**: A patient logs into Epic, schedules via a third-party app, receives SMS through Twilio, uses a telehealth platform, and calls a Salesforce call center. The EHR knows clinical history but lacks the full engagement picture. The CDP stitches these fragments using deterministic and probabilistic matching to create persistent profiles.

**Consent Orchestration**: Privacy preferences and opt-out signals must propagate in real-time. When a patient revokes tracking permissions, that signal must instantly reach email, SMS, call centers, and ad networks. CDPs excel at this governance layer, preventing PHI from flowing to unapproved third parties.

**Behavioral Signal Capture**: EHRs track clinical encounters; CDPs track operational exhaust: abandoned forms, repeated symptom searches, unopened messages, missed appointments. Not diagnostic, but operationally decisive.

**Cross-Channel Analytics**: The CDP reveals where patients face access barriers, which communication strategies work, and where workflows break down, enabling better processes and outreach design.

In these roles, the CDP unifies, manages, and reports. It does not decide.

### CDPs in Practice: What Good Deployment Looks Like

**Payer: Cambia Health Solutions** Cambia had fragmented data across claims, website behavior, and call centers. They implemented Tealium in a HIPAA-compliant environment to create a unified "Member 360" view. The CDP operated as infrastructure to improve experience and efficiency through data unification, not clinical decision-making.

**Provider Operations** Health systems integrate EHR appointment data and clinical flags into CDPs. When a patient due for screening (clinical fact from EHR) visits the website (behavioral signal from CDP), the CDP triggers a personalized scheduling message. Clinical logic comes from the EHR; activation comes from the CDP.

**Pharma Patient Support** Manufacturers use CDPs to track adherence signals. When verified patients repeatedly visit side-effect content but don't refill prescriptions, the CDP flags them for nurse intervention. The CDP identifies the signal; clinical staff own the intervention.

**The Common Thread**: In successful implementations, the CDP ingests clinical data, listens for behavioral signals, and triggers operational actions. The CDP senses and activates. Humans and clinical systems decide.

### Where CDPs Become Dangerous: The Red Zone

The risk emerges when activation becomes autonomous prioritization. CDPs maximize engagement and conversion, so "next best action" can quietly become "next easiest patient." In healthcare, responsiveness is a biased proxy for need.

**Next-Best-Action Without Clinical Context**: A CDP sees a patient hasn't scheduled follow-up. It often cannot see that the patient is unhoused, their insurance lapsed, or they're in hospice. Context data may be missing, delayed, or not shareable. The system has behavioral signals, not meaning.

**Optimization for Wrong Outcomes**: CDPs maximize engagement metrics: open rates, clicks, conversion. In healthcare, high engagement doesn't equal good care. Campaigns optimized for appointment completion might systematically deprioritize Medicaid patients whose phones are off during work, or rural patients with unreliable connectivity. The algorithm works inequitably.

**Propensity as De Facto Prioritization**: When propensity predictions drive resource allocation (navigator time, expedited scheduling, follow-up calls), low propensity becomes deprioritization. In retail, ignoring low-propensity customers is efficiency. In healthcare, ignoring low-engagement patients who might be low-literacy or low-income is inequity. Low engagement often correlates with access barriers, not lack of need. The failure mode is consistent directional optimization toward the easiest to reach.

**Shadow Clinical Logic**: When CDPs recommend which patients receive care reminders, which specialists to suggest, or how to prioritize outreach without clinical review, they become de facto triage systems built by engineers optimizing for engagement, not clinicians accountable for outcomes. This bypasses established clinical decision support protocols built into EHRs.

CDPs were designed to model customers, not patients. They excel at propensity and orchestration, which can quietly turn into prioritization unless constrained. In healthcare, where equity and clinical need determine whether optimization helps or harms, this distinction is the difference between closing care gaps and widening them.

### The Missing Layer: Governance

Most health systems deploy CDPs without defining what they're allowed to decide autonomously. Technology does not enforce boundaries. Governance does.

**Three questions must have clear answers:**

**1. Who defines "next-best-action," and is a clinician involved?** If a CDP recommends care-related outreach or prioritization, clinical leaders must define what "best" means and for which populations.

**2. Can the system make equitable decisions when critical context is missing?** Insurance instability, housing status, language proficiency, caregiver availability, transportation access - none of this reliably appears in clickstream data. If the CDP decides based primarily on digital behavior, it's systematically blind to factors determining whether patients can act on recommendations.

**3. Is there a checkpoint between recommendation and patient-facing action?** Real-time activation is powerful and irreversible at scale. For high-stakes interventions, there needs to be a checkpoint.

If you cannot answer all three, you have a marketing automation platform making clinical decisions.

### CDPs as Edge Layer, Not System of Record

The future role of CDPs in healthcare is as an edge layer: sensing behavior, personalizing experience, and activating workflows, but only when tightly coupled with clinical context and explicit guardrails.

**Green zone (autonomous)**: Identity resolution, consent management, behavioral data collection, reporting.

**Yellow zone (human-in-loop)**: Audience segmentation, communication timing and channel optimization, workflow triggers.

**Red zone (requires clinical governance and equity auditing)**: Any CDP-driven next-best-action that changes clinical access, prioritization, or care pathways. Any use of behavioral propensity to decide resource allocation, unless equity constraints are explicit and audited.

These boundaries must be designed into governance frameworks, enforced through integration architecture, and monitored through ongoing audits of algorithmic impact and equity outcomes.

Without governance, CDPs become engagement engines at scale, optimizing for metrics that may conflict with care. With governance, they become infrastructure that unifies fragmented systems, respects patient context, and enables human judgment rather than replacing it.

We cannot allow our desire for an "Amazon-like" patient experience to inadvertently create an algorithmically biased triage system. The difference is not the platform. It is how intentionally we decide what it is allowed to optimize for, and who gets to make that decision.
