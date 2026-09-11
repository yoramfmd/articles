---
title: Intelligence Without Context Is Just Confidence
slug: intelligence-without-context-is-just-confidence
published: 2026-03-25
excerpt: OpenAI had one of the best models in the world. Walmart still fired it. Not because the model was weak. Because it had no idea what it was working with.
url: https://data-decisions-and-clinics.com/intelligence-without-context-is-just-confidence/
tags: Data & AI
source: ghost-api-pull-2026-08-04
---

In October 2025, Walmart and OpenAI announced a partnership. Both CEOs were enthusiastic. The announcement used phrases like "AI-first shopping experiences" and "the future of e-commerce." Customers would plan meals, restock essentials, and discover products simply by chatting with ChatGPT. Walmart would take care of the rest.

Five months later, Walmart quietly pulled the plug.

Not because the model stopped working in general. Because, in this setup, it had no idea what it was actually working with.

---

## What the infrastructure actually looks like

I spent two years at Walmart Global Tech leading the cloud platform product management team. I know what the real infrastructure looks like from the inside.

An endless catalog of SKUs. Millions of customers. Real-time inventory across 4,700 store locations. Pricing logic that varies by geography, membership tier, and promotional window. Delivery constraints tied to specific fulfillment centers. Order history and customer context that took years to build.

These are not separate data points. They are a living system, constantly updated, tightly integrated, and deeply interconnected. A "Sales Order" affects "Inventory Availability." A delivery window depends on which fulfillment center serves which zip code at what time. None of that logic lives on the website.

OpenAI's Instant Checkout obtained its data by scraping Walmart's website.

Scraping gives you a shadow. A snapshot of what was listed hours ago, without real-time inventory, without pricing rules, without delivery constraints, without the business logic that makes the system actually work. The model was reconstructing Walmart's business from the outside. And it was doing it confidently. Which is the most dangerous kind of wrong.

The result, according to reporting and internal metrics that have surfaced publicly, was predictable to anyone who understood the architecture: broken carts, inaccurate delivery windows, and conversion rates that fell well below Walmart's own digital channels. The AI answered every question. It just answered them wrong. The answers looked right. That is the part that matters.

---

## The execution culture most people don't see

What surprises people on the outside is how fast a company this size moves when the data is clear.

There are no endless roadmap discussions at Walmart. No committee reviews. No multi-quarter debates about whether to pivot. There are sharp KPIs, short dev cycles, and a very simple operating principle: if the numbers say it is not working, you fix it or you walk away. The speed is not recklessness. It is discipline. A clear metric, a defined window, a decision.

We all remember how quickly Walmart responded to the COVID-19 lockdowns, rolling out curbside pickup across its stores in days. Amazon's comparable rollout at Whole Foods took much longer. That gap was not a technology gap. It was a data foundation gap.

Five months is already a long test by Walmart standards. The decision to walk away was not slow deliberation. It was execution.

But Walmart did not just abandon the idea. They inverted the relationship.

Instead of letting an external model scrape their site and simulate a shopping experience, they built Sparky: their own assistant, anchored in their own data, business rules, and operational context. As of March 2026, Sparky lives inside ChatGPT and Gemini. Not the other way around.

Walmart owns the customer. Walmart owns the transaction. Walmart owns the relationship. The LLM runs on top of the foundation they built. Early results show conversion rates through Sparky reaching 70% of direct Walmart.com performance. That number will improve as the integration matures. The OpenAI era never got close.

The architecture is the answer: the model is the interface, the business system is the truth.

---

## The failure mode is not retail

In a recent article I argued that healthcare is the northstar for AI. The field everyone called a laggard has been running the most rigorous AI experiment for decades, publishing its failures so the rest of the world can learn from them.

Walmart is one of those lessons. It has nothing to do with healthcare.

The same pattern shows up in healthcare when models are wired to incomplete or external data rather than the actual clinical systems. It shows up in retail when a model scrapes a website instead of querying a live inventory. The domain changes. The failure mode does not.

The failure mode is architectural, and it appears everywhere a powerful model is deployed on top of incomplete, context-free, or scraped data. The model answers confidently. The answer looks correct. The format is right, the vocabulary fits, the structure is intact. And the answer is wrong. I have written about this pattern in the context of clinical AI hallucinations: the most dangerous errors are not the ones that look like errors. They are the ones that pass review because they are superficially plausible.

In medicine, a model recommending a dosage it pulled from its training distribution rather than from the patient record in front of it does not look obviously wrong. It looks like a correct answer. In retail, a model confirming a delivery window it cannot actually verify looks like a correct answer too. The failure mode is identical. The domain is different. The lesson is the same.

This is what I call validation theater: the output passes because it is fluent, structured, and confident. The error survives because nothing in the review process was anchored to an actual source of truth. Asking a second model to validate the first one does not solve this. It adds a second layer of confidence on top of the same flawed inputs. Walmart did not solve the problem by switching models. They solved it by changing what the model was connected to.

---

## What this means for every organization building on AI

This is also why SAP's strategy makes sense to me. From my vantage point working on SAP Business Data Cloud, the architectural bet is the same one Walmart ended up making, and the logic behind it is the same.

SAP Business Data Cloud is built on a specific architectural bet: that the semantic layer, the definitions, relationships, and business rules that reflect how an organization actually operates, has to be the foundation that agents are built on, not a layer they approximate from the outside. The agents that work are the ones that query the actual system of record. The ones that fail are the ones that reconstruct it from what they learned on the internet.

Joule, SAP's AI assistant, is grounded in the knowledge graph of the business systems it operates within. It does not scrape. It does not approximate. It queries the truth. When it tells you a delivery is available, that answer comes from the system that knows whether the delivery is available. When it surfaces a business rule, that rule comes from the system that holds it.

The Walmart story is not about OpenAI losing a contract. It is about what every organization will eventually learn, some faster than others, some at greater cost than others: that the model is not the product. The model is the interface. The data foundation, the semantic layer, the living system of record, that is the product.

Healthcare figured this out under pressure because the cost of a confident wrong answer is immediate, documented, and visible. Retail figured it out because the cost showed up in conversion rates. Every other industry running AI on consequential decisions will get there too.

The companies that will be ahead are not the ones with access to the best models. Every organization has access to the best models. They are the ones that built the foundation the models can actually reason from.

Walmart figured it out in five months. That is fast, even for Walmart.

---
