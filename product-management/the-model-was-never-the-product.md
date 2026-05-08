# The Model Was Never the Product

*Published title: Intelligence Without Context Is Just Confidence*

---

In October 2025, Walmart and OpenAI announced a partnership. Both CEOs were enthusiastic. The announcement used phrases like "AI-first shopping experiences" and "the future of e-commerce." Customers would plan meals, restock essentials, and discover products simply by chatting with ChatGPT. Walmart would take care of the rest.

Five months later, Walmart quietly pulled the plug.

Not because the model stopped working in general. Because, in this setup, it had no idea what it was actually working with.

---

I spent two years at Walmart Global Tech leading the cloud platform product management team. I know what the real infrastructure looks like from the inside.

An endless catalog of SKUs. Millions of customers. Real-time inventory across 4,700 store locations. Pricing logic that varies by geography, membership tier, and promotional window. Delivery constraints tied to specific fulfillment centers. Order history and customer context that took years to build.

These are not separate data points. They are a living system, constantly updated, tightly integrated, and deeply interconnected. A "Sales Order" affects "Inventory Availability." A delivery window depends on which fulfillment center serves which zip code at what time. None of that logic lives on the website.

OpenAI's Instant Checkout obtained its data by scraping Walmart's website.

Scraping gives you a shadow. A snapshot of what was listed hours ago, without real-time inventory, without pricing rules, without delivery constraints, without the business logic that makes the system actually work. The model was reconstructing Walmart's business from the outside. And it was doing it confidently. Which is the most dangerous kind of wrong.

The result was predictable to anyone who understood the architecture: broken carts, inaccurate delivery windows, and conversion rates that fell well below Walmart's own digital channels. The AI answered every question. It just answered them wrong. The answers looked right. That is the part that matters.

---

What surprises people on the outside is how fast a company this size moves when the data is clear.

There are no endless roadmap discussions at Walmart. No committee reviews. No multi-quarter debates about whether to pivot. There are sharp KPIs, short dev cycles, and a very simple operating principle: if the numbers say it is not working, you fix it or you walk away. The speed is not recklessness. It is discipline. A clear metric, a defined window, a decision.

We all remember how quickly Walmart responded to the COVID-19 lockdowns, rolling out curbside pickup across its stores in days. Amazon's comparable rollout at Whole Foods took much longer. That gap was not a technology gap. It was a semantic model gap. Walmart had already mapped its 4,700 locations as a live data network, with real-time inventory, fulfillment logic, and delivery constraints all connected and queryable. When lockdowns hit, they updated the operational rules. The semantic model did the rest. Amazon had to build that foundation first.

Five months is already a long test by Walmart standards. The decision to walk away was not slow deliberation. It was execution.

But Walmart did not just abandon the idea. They inverted the relationship.

Instead of letting an external model scrape their site and simulate a shopping experience, they built Sparky: their own assistant, anchored in their own data, business rules, and operational context. As of March 2026, Sparky lives inside ChatGPT and Gemini. Not the other way around.

Walmart owns the customer. Walmart owns the transaction. Walmart owns the relationship. The LLM runs on top of the foundation they built. Early results show conversion rates through Sparky reaching 70% of direct Walmart.com performance. That number will improve as the integration matures. The OpenAI era never got close.

The architecture is the answer: the model is the interface, the business system is the truth.

---

This is why SAP's strategy makes sense to me. From my vantage point working on SAP Business Data Cloud, the architectural bet is the same one Walmart ended up making, and the logic behind it is the same.

SAP Business Data Cloud is built on a specific architectural bet: that the semantic layer, the definitions, relationships, and business rules that reflect how an organization actually operates, has to be the foundation that agents are built on, not a layer they approximate from the outside. The agents that work are the ones that query the actual system of record. The ones that fail are the ones that reconstruct it from what they learned on the internet.

What makes SAP's managed data products structurally different from a conventional data warehouse or a data lake is how they preserve business context. Operational logic persists within the data product itself: a purchase order carries not just the transaction amount but the approval hierarchies, spending authorities, supplier relationships, and contract terms that govern it. Entity relationships maintain their integrity across functional boundaries: a customer connects to orders, invoices, support tickets, and service contracts through relationships the system has tracked from the first transaction, so AI systems never have to reconstruct a customer hierarchy from scratch. Comprehensive metadata travels with the data: when an AI model encounters "payment terms," it can access the business definition, valid values, and calculation methods without requiring separate documentation or tribal knowledge.

This is why harmonization across SAP's application portfolio matters in a way that a data warehouse cannot replicate. When SAP defines "customer," that entity carries the same meaning whether it appears in order management, accounts receivable, service management, or marketing automation. Revenue means the same thing in sales analytics and financial reporting. Inventory value means the same thing to supply chain planners and finance controllers. The definitions do not require reconciliation because they originate from a unified business data model. An AI working on top of that foundation can identify anomalies, payments without invoices, shipments without orders, not through pattern matching but because it understands which sequences should occur and which represent exceptions. That is reasoning. The scraping approach produces confidence. This produces understanding.

Joule, SAP's AI assistant, is grounded in this foundation. It does not scrape. It does not approximate. It queries the truth. When it tells you a delivery is available, that answer comes from the system that knows whether the delivery is available. When it surfaces a business rule, that rule comes from the system that holds it.

The Walmart story is not about OpenAI losing a contract. It is about what every organization will eventually learn, some faster than others, some at greater cost than others: that the model is not the product. The model is the interface. The data foundation, the semantic layer, the living system of record, that is the product.

Healthcare figured this out under pressure because the cost of a confident wrong answer is immediate, documented, and visible. Retail figured it out because the cost showed up in conversion rates. Every other industry running AI on consequential decisions will get there too.

The companies that will be ahead are not the ones with access to the best models. Every organization has access to the best models. They are the ones that built the foundation the models can actually reason from.

Walmart figured it out in five months. That is fast, even for Walmart.
