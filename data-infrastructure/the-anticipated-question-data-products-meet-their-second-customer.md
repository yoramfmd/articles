---
title: "The Anticipated Question: Data Products Meet Their Second Customer"
slug: the-anticipated-question-data-products-meet-their-second-customer
published_at: 2026-08-25
custom_excerpt: "Data products were built on a quiet assumption: the designer could anticipate the questions. Agents break that assumption without breaking the discipline. What survives is not the shape we prepared but the honesty of the contract underneath it. Five questions for every data product owner."
tags: [data]
feature_image: https://storage.ghost.io/c/e6/05/e605b234-3cc8-4fe4-97bb-2bb55b18b8fb/content/images/2026/08/ChatGPT-Image-Aug-25--2026--12_23_14-PM.png
source: ghost
---

# The Anticipated Question: Data Products Meet Their Second Customer

# 

Every data product ever shipped encodes a guess about the questions it will be asked. Agents bring their own.

That is not a criticism of data products. I have spent the last years arguing the opposite: that governed, semantically clear, owned data assets are the only foundation on which enterprise AI moves from pilots to production. The discipline is right. But inside every well-designed data product sits an assumption so old and so quiet that we stopped noticing it, and the agentic era is about to make it visible.

I want to name that assumption, and then raise the questions it leaves behind.

## The assumption we stopped noticing

When a team designs a data product today, someone decides the grain. Someone decides which columns matter, which aggregations to precompute, how often to refresh, what history to keep. Each of those decisions is a bet on the questions the product will be asked. Daily grain because nobody asks hourly questions. Twelve columns because those are the ones the quarterly review needs. Aggregated by region because that is how the business thinks.

This is the anticipated question, and for the analytical era it was exactly the right design principle. Human attention is scarce. You cannot hand an analyst a billion rows; you hand them a shape. And because hundreds of people ask roughly the same questions, one carefully curated shape amortizes beautifully. The economics of the analytical data product are the economics of the median question, asked many times, by many people, through a dashboard.

The dashboard was never really the interface. It was the last step of a pipeline of anticipated questions, each one narrowing the data toward the answers someone predicted would matter.

## The consumer that brings its own questions

An agent does not work from your list of questions. It receives a goal, and it decomposes that goal into whatever questions the moment requires: hundreds of them, heterogeneous, most of them never asked by any human because no human had the patience. Where the analytical era had many people asking the same question, the agentic era has one agent asking a thousand different ones.

This inverts the economics. The value of a pre-decided shape falls, because the shape answers the questions someone anticipated and the agent has arrived with different ones. Meanwhile the value of everything underneath the shape rises: the definitions, the relationships, the lineage, the business context that lets any question be answered correctly rather than a chosen few be answered conveniently.

This is why the context-carrying direction matters so much. A data product that travels with its meaning, its calculation logic, its entity relationships, and its governance is already designed for a consumer that asks unanticipated questions. That was the argument for building the semantic layer into the product rather than around it, and the agentic era does not weaken that argument. It makes it the whole argument.

But it also adds requirements that the analytical era never had a reason to state.

## What the agent cannot feel

Here is the difference that keeps me up at night, and it comes from clinical practice rather than data architecture.

A human analyst who hits the edge of a data product knows it. The column is not there, the drill-down stops, and the analyst feels the absence and walks down the hall to ask someone. Friction, but visible friction.

An agent does not feel absence. It reasons over what it can retrieve, and it reasons faithfully. If the data product carries everything except the one field that mattered, the agent does not produce a hesitant answer. It produces a confident answer built on a true and partial record, and nothing in the answer reveals the gap. The record is complete as far as the agent knows, and the picture is wrong.

Medicine solved a version of this problem centuries ago, and the solution is instructive because it is documentation, not technology. A clinical note does not only record findings; it records pertinent negatives. No fever. No chest pain. Not examined. The chart distinguishes explicitly between "we looked and it was absent" and "we never looked," because the next clinician reading the chart cannot feel the difference, only read it.

Data products, as we build them today, do not document their pertinent negatives. They present what they contain, and what they exclude is simply not there: the field outside the scope, the history beyond the retention window, the source system nobody connected. A human consumer eventually learns these boundaries as folklore. An agent never does, unless the product says so.

## Five questions for the next design review

I do not think the answer is a new architecture. I think it is a longer contract, and it starts with questions that data product owners can ask today, in the design reviews they already run.

First: what does this product exclude, and does it say so? Not in a wiki page three systems away; in the product itself, machine-readable, where a consumer that cannot feel absence can at least read it. Coverage becomes part of the interface, not an operational detail.

Second: how fresh is each field, and does the product know? Datasets carry refresh schedules; fields carry lives of their own. The opportunity flag your sales team updates at close rather than at open is accurate by its own rules and misleading by anyone else's. A human learns this over coffee. An agent needs it declared, per field, because the ceiling on its reasoning is not the model. It is the data's honesty about its own age.

Third: which values are measured, which are derived, and which are asserted? Mature semantic models already mark the second tier; decades of analytics modeling distinguish a base measure from a calculated one, and that vocabulary is real and machine-readable today. The missing tier is the third: nothing distinguishes the human-keyed estimate, the forecast, the value somebody asserted, from the value a system measured. A finance controller instinctively treats an actual, a calculation, and an estimate as three different kinds of truth even when they sit in identical columns. An agent will treat the asserted one as measured unless the metadata says otherwise, and confident arguments built on asserted numbers are the enterprise version of a differential diagnosis built on hearsay.

Fourth: which fields are trusted, and which merely present? Free-text fields, notes, memos, descriptions written by thousands of hands: for a human these are color, for an agent they are input, and input can carry instructions. A data product consumed by agents needs to mark the boundary between fields that state facts and fields that merely contain text.

Fifth: who is asking, on behalf of whom, for what task? This is the question the platform vendors have moved on fastest: agent identities now live alongside human identities, with gateways that constrain which tools and interfaces an agent may touch. What remains open is the sharper half. An agent is a delegated authority with a task description, and the same agent may deserve different answers on different tasks. The access model of the analytical era answered "who are you." Agent identity answers "which agent are you." The question still ahead of us is "what are you doing right now, and who answers for it."

None of these questions requires abandoning anything. Every one of them is an extension of what made data products work in the first place: ownership, contracts, meaning carried with the data. The teams that built that discipline are the only teams positioned to extend it.

## What we were selling all along

Which brings me to the question under the questions.

If the shape layer of data products loses value, what were data product teams actually producing? I think the honest answer is that the shape was never the product. The product was trust: the guarantee that when a number arrived, it meant what it said, came from where it claimed, and could be defended in the meeting. The shape was just the packaging that human attention required.

Agents remove the packaging requirement and keep the trust requirement, then raise it, because the consumer can no longer compensate for what we left unsaid. The design review question of the analytical era was "which questions will this answer?" The design review question of the agentic era is harder and better: what will an agent believe about the world after reading this product, and is every part of that belief one we are prepared to stand behind?

Every data product encodes a guess about the questions it will be asked. We can no longer guess the questions. We can still, and must, stand behind the answers.

*I work at SAP; the opinions here are my own.*

*This article is part of an ongoing series on AI product design, healthcare data, and the human side of technology adoption.*
