---
title: The Brief Is Now Two Documents
slug: the-brief-is-now-two-documents
published: 2026-06-07
excerpt: The PRD was built for software that does what it's told. An agent exercises judgment, and the moment it crosses from suggestion to decision, the old brief breaks. It splits in two: one document to decide, one to build. The new AI tools can write the second. The first is still yours.
url: https://data-decisions-and-clinics.com/the-brief-is-now-two-documents/
tags: Product Management
source: ghost-api-pull-2026-08-04
---

*The traditional PM brief was built for a deterministic world. Agentic products do not live in that world. Here is what changes, and what you have to write that no platform will generate for you.*

---

A team I know spent a quarter rebuilding a refund agent that already worked.

The agent did exactly what it was asked: it took a refund request and carried it, in one fluent motion, from received to resolved. Then someone asked the question that should have come first. Where does a human step in when the amount is large, or the account looks like fraud? There was no seam. The agent had been built as a single uninterruptible gesture, and inserting a human meant taking it apart and building it again. The boundary had been making the product's most important decision the whole time. The team had just let the architecture make it, instead of making it themselves.

That was not a tooling problem. It was a brief problem. And it is the one this piece is about.

When you build an agentic product, you are building two products at once.

The first is the agent: the thing that acts, reasons, calls tools, and produces output. Call it Channel 1. In 2026 it is becoming table stakes. The model, the orchestration framework, the tool integrations, the whole stack is converging, and the teams that think the agent itself is the moat are finding out otherwise.

The second is the supervisory layer: the behavioral contract, the autonomy boundary, the approval gates, the audit surface, the human system built to watch Channel 1 without losing the power to override it. Call it Channel 2. It does not demo. It does not ship features. It is the thing that makes Channel 1 trustworthy, and almost no team builds it deliberately.

The split matters the moment an agent crosses from suggestion to decision, from drafting something a person approves to taking an action with a consequence. It matters again when the thing crosses from an MVP you can demo to a product you can trust. Those are the same crossing seen twice: the first is about what the agent is allowed to do, the second is about whether you can stand behind what it did. At that line the traditional PM brief breaks. The PRD, the epic, the user story were built for a deterministic world: a system does what it is told, pass/fail is a real answer, a test that runs once means something. Those assumptions do not fail evenly. They hold for the deterministic shell around the agent, and they fail exactly where the agent exercises judgment, which is the half that determines whether you can trust it. Forcing that half into the shape of a deterministic brief is where most agentic products fail before they ship.

The fix is not a better brief. It is two briefs.

---

## The Human Brief

The Human Brief is the successor to the PRD, but its job is not requirements. Its job is the argument.

It states the problem and the alternatives considered. It names what the product will deliberately not become. It holds the cost model: not the model's token price, but the fully loaded per-task cost, the architecture multiplier, the supervision overhead, the break-even against whatever you are replacing. It answers the go/no-go on paper, before anyone builds anything, because once a prototype ships and demos well, the go/no-go leaves the room and never comes back.

Most importantly, it names who answers for what the agent does to people who never touch it.

That is the part teams skip most reliably, because the user story, built for the happy path, has no field for it. An agent that issues a wrong refund, reroutes a shipment to the wrong address, or surfaces a clinical recommendation outside its training distribution has done something to someone. Someone has to own that. The Human Brief is where you decide, in advance, who that is and what they do about it, before the incident makes the decision for you. This is not a compliance function. It is a product decision with a named owner, and the difference shows the night something breaks at 2am.

Channel 2's contribution to the Human Brief is the autonomy boundary: what the agent may do alone, what needs human approval, and where authority returns to a person regardless of what the agent thinks. That boundary is not a technical constraint. It is a business decision, load-bearing from the first line of Channel 1 code. The team that rebuilt its refund agent learned this the expensive way. The boundary was always going to decide the shape of the product. They just deferred it until the architecture had decided for them.

The Human Brief is the artifact the room argues with. A room that cannot argue with it has not made the decisions that determine whether the product is buildable, trustworthy, and worth building at all.

---

## The Executable Brief

The Executable Brief is the successor to the epic, and its job is precision. It structures the experience, the behavior, and the governance in explicit enough form that a generation tool takes the path you intended rather than the shortest one through whatever ambiguity you left in.

The mature pattern, visible in the spec-driven development tooling of the last two years, GitHub's Spec Kit the clearest instance, is to derive the Executable Brief from the Human Brief rather than write it from scratch. Machine-assisted, human-owned. The Human Brief is the source of intent. The Executable Brief is what the build consumes.

Channel 2 shows up here too, in a different form. The Human Brief names the boundary as a decision. The Executable Brief makes it buildable: the approval moment, the audit surface, the recovery workflow, each one a requirement with acceptance criteria of its own.

The Executable Brief is read twice. First by the coding agent that generates the prototype, then by the engineers who build the production system. The same requirement renders differently for each reader. "The agent must not access personal data outside the authorized scope" becomes, in a prototype, an instruction the agent follows as far as it cooperates. In production it becomes an architectural control: a data-access layer that strips the fields before the agent can see them, so the boundary holds whether the agent cooperates or not. One brief, two implementations, hardening from a prompt into a structure as the product moves from bet to build.

One gap in the current tooling is worth naming. Spec Kit has an artifact it calls a constitution: principles the spec must honor. But that constitution holds engineering principles, test-first, simplicity, library boundaries, how the team builds, not how the agent behaves. The tools assume you have already worked out the behavioral contract and the business case, and they help you structure and execute from there. The Human Brief is the thing they assume you have. It is the artifact the tooling does not help you write.

---

## The Unit of Work Changes Underneath Both Briefs

The clearest way to see the gap between the old approach and the new one is the same example, written both ways.

A support agent processes refund requests. The traditional story writes itself: as a customer, when I request a refund for a defective item, the agent issues the refund. Acceptance criterion: given a valid order inside the return window, the agent issues the refund and sends confirmation. Clean story. It passes any backlog review.

It is also the wrong primitive, because it describes the case that was never hard. The defective item inside the window was always going to be refunded. The story has nothing to say about the request just outside the window where the customer is right on the merits, or the one where the customer is about to churn and the refund is worth more than the margin, or the one where the amount is ten times the others and the pattern smells like fraud. Those are the cases the agent will be judged on. The user story has no field for any of them.

The Executable Brief carries those cases as an outcome-centric spec. Four parts the user story structurally cannot hold.

The **outcome**: what the agent is trying to achieve. Resolve refund requests the way a reasonable manager would endorse on review, favoring customer trust on small amounts and human judgment on large or anomalous ones.

The **bounds**, from Channel 2: the agent may issue refunds up to a threshold on its own; above that amount, outside the window, or when a fraud signal fires, it routes to a human.

The **eval set**: a curated dataset of real cases, each paired with the outcome a senior support lead actually endorsed, including the generous exception, the justified denial, the ambiguous escalation, so the agent is graded against real judgment instead of a synthetic happy path.

And **what acceptable failure looks like**: a wrong escalation, routing a borderline case to a human who did not strictly need to see it, is tolerable and expected. A wrong auto-approval on a fraud-pattern case is a never-ship failure. One occurrence fails the eval. The user story has nowhere to put that distinction. The outcome-centric spec is built around it, and the escalation rule is the seam back to Channel 2: every case the agent declines to decide is a case the supervisory layer has to be designed to catch.

Set the two side by side. The story has one field, the happy path, verified by a test that passes. The spec has four, graded against real judged cases, including the ones that say what the agent is allowed to get wrong.

The whole split fits in three lines. A PRD says: issue refunds within policy. A Human Brief says: we will sometimes break policy to keep a customer, up to a set amount, and a named person owns that call. An Executable Brief says: auto-approve under the threshold, escalate above it, never auto-approve on a fraud signal. The PRD is the only one of the three a deterministic backlog already knows how to hold.

---

## Two Doors Into the Same Room

There is a newer pattern that looks like it might dissolve all of this. Instead of writing the spec, you state a business intent in plain language and the platform drafts the specification as an artifact you review and approve, phase by phase. SAP's Joule Studio, shown at SAPPHIRE 2026, is the clearest instance I have seen: you give the intent, it drafts the spec, you own each transition. This is a real advance. It opens spec-driven development to people who were never going to write a spec.

The temptation is to read it as evolution: specification-driven development for developers, intent-driven development as the more advanced successor. That is the wrong read. They are not two rungs on a ladder. They are two doors into the same room, cut for two different people.

Lay the whole path out as a ladder of altitudes. An **idea** ("let customers self-serve refunds") becomes a **decision** (build it or not, where the boundary sits, who owns a wrong outcome, what it costs) becomes a **spec** (experience, behavior, governance, precise enough to build from) becomes a **build** becomes a **running product**. Everything above the spec is judgment. Everything below it is execution. Specification-driven development covers spec to build: the human writes the spec, the machine consumes it, the persona is a developer. Intent-driven development covers idea to spec: the human states the intent, the machine drafts the spec, the persona is a business user. Different doors, different people, opening into the same room, and in practice only its Channel 1 half.

Here is the line that matters. These tools turn an idea into a product by turning a spec into a build. What they cannot do is turn an idea into a decision, and the decision is the rung that determines whether the product should exist at all.

That decision rung is the Human Brief, and it sits exactly where intent-driven development appears to cover, between idea and spec. It does not cover it. A business intent is the opportunity line, the first sentence of the Human Brief, not the Human Brief itself. The intent says what you want to be true. The Human Brief says what it costs, what it must never become, where authority returns to a person, and who answers when it is wrong. The engine takes the intent as given and drafts down from it. It never produces the argument that should have come before the intent, because that argument requires knowing what wrong costs your organization, and no tool knows that. Only you do.

So the failure mode does not improve as the tooling improves. It hides. With specification-driven development the Executable Brief races ahead and the Human Brief is a visible stub. With intent-driven development the generated spec races ahead and the behavioral contract is a stub under a polished surface, which is worse, because no one reviewing a finished-looking spec feels the thing that is missing. They approve on reflex. The industry built two front doors for two personas and called it progress. The room that decides whether the product is safe to ship still has no door, because no tool can generate what goes in it.

---

## What Changes Monday

Three things shift in practice.

Any PRD for an agentic feature that is one document is half a spec. Split it. The Human Brief goes to the room to be argued with. The Executable Brief goes to the build. If the Channel 2 artifacts, autonomy boundary, approval moment, audit surface, recovery workflow, appear only in the Executable Brief as buildable requirements, without the reasoning in the Human Brief, then nobody owns the decisions those requirements encode. They become implementation details carrying the weight of product decisions, with no one accountable for them.

Stop calling the behavioral spec a "governance artifact." That word sends it to a committee that meets quarterly. The outcome-centric spec, the one with the eval set and the definition of acceptable failure, belongs on the backlog with the same owner as the feature it governs, on the same release schedule. An agent without a behavioral spec is not a product. It is a demo that shipped.

And when you evaluate any spec-driven or intent-driven workflow, do not ask what the generation engine produces. Ask what it assumes you already have. The thing it assumes, and does not help you write, is where your work is.

---

The brief did not get simpler. It got split into two documents with different audiences and different jobs.

The one that goes to the room is the harder one. It holds the decisions most teams defer. It names who answers for what the agent does, before the incident makes that decision for everyone.

That document is yours to write. No platform will generate it.

---

*The Channel 1 / Channel 2 framing and the Human Brief / Executable Brief model are from* Agentic AI for Busy Product Managers *and* Why Agentic AI Products Fail, *both available on Amazon.*
