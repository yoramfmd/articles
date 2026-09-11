---
title: The AI Model War Will Not Be Won by the Best Model
slug: the-ai-model-war-will-not-be-won-by-the-best-model
published: 2026-05-03
excerpt: LLMs are getting faster, cheaper, and better every week. The comparison charts prove it. They also prove nothing about who wins. I've watched six technology wars end. The best product lost every time. The winner owned the right layer of the stack.
url: https://data-decisions-and-clinics.com/the-ai-model-war-will-not-be-won-by-the-best-model/
tags: Product Management, Data & AI
source: ghost-api-pull-2026-08-04
---

*I run four AI models in parallel. Not because I love complexity. Because I have been here before.*

Right now, on any given morning, I might use one model for long-form writing, a different one for fact-checking, another for summarizing research, and a fourth for image generation. I keep a browser tab open with a model router that sends queries to whichever engine seems most capable for the task type. I have a spreadsheet, slightly embarrassing in its specificity, that tracks which model I reach for when.

And every day, my LinkedIn feed serves me a new image: a comparison chart ranking the latest models on some benchmark. Speed, reasoning, coding, multimodal. A new chart arrives before I have finished processing the last one.

I stopped paying attention to the charts weeks ago.

Not because the question is unimportant. Because I have been here before, and I know what the charts are telling me and what they are not. I was a product manager during the browser war, the search engine war, and the social media war. I am, with a slight measure of professional embarrassment, old enough to have lived through the spreadsheet war, the presentation software war, and the database wars. I once taught students how to use Harvard Graphics, made some genuinely good presentations with it, and moved to the next tool when the time came. That is the job. I have watched technology markets do this exact thing: generate enormous noise at the product level while something structural is quietly deciding the outcome underneath.

The noise is not the signal. The comparison charts tell you what week it is. They do not tell you what decade it is.

---

## What every technology war looks like from the inside

Let me be specific about what I mean when I say I have been here before.

The spreadsheet war was not won by the best spreadsheet. Lotus 1-2-3 was technically excellent. So was Quattro Pro. VisiCalc invented the category. IBM DB2 remained a serious enterprise contender through the 1990s, but Oracle pulled ahead decisively; today DB2 survives almost entirely inside financial institutions where the migration cost to anything else exceeds any conceivable switching benefit. The winner in each category was the product positioned at the right layer of the stack, not the product that won the feature comparison. Microsoft Excel won because Microsoft controlled the operating system that spreadsheets ran on, because it bundled Office into enterprise licensing deals that made individual product choices irrelevant at the procurement level, and because it got to the right distribution channel before the others understood what distribution channel they were actually competing in.

The browser war. Netscape pioneered the commercial web browser. It was better than what came after it for years. Microsoft shipped Internet Explorer for free, bundled it with Windows, and made every PC in the world a default Netscape replacement. Distribution bundling won the war. Regulation came after the outcome was already decided. The browser did not matter; the operating system did.

The search engine war. AltaVista, Excite, Lycos, Infoseek, Yahoo. All of them had meaningful market share at one point. None of them had PageRank. Google's insight was architectural, not incremental: the link graph of the web was itself a signal about relevance that none of the other engines were using. When the architectural advantage is big enough, the company with it wins even if its product looks worse on every feature comparison chart, because the feature comparison charts are measuring the wrong thing.

The social media war is still instructive because it has not fully resolved. Friendster arrived first. MySpace was dominant. Facebook won the Western market, WeChat won the Chinese market, and TikTok arrived fifteen years later and won the attention market that neither of them understood they were in. What defined each transition was not product quality or feature count. It was network effects, data access, and the specific type of value the platform could compound over time.

What do all of these have in common? The winning product was almost never the best product at the moment of transition. The winner was the product or company positioned at the right layer of the stack, with access to the right compounding asset, at the moment the market structure crystallized.

---

## The academic name for what I am watching

Researchers who study industrial evolution call the chaotic period before a market structure crystallizes the era of ferment. The term comes from Utterback and Abernathy, two MIT economists who in the 1970s mapped the lifecycle of manufacturing industries from inception to maturity.

The model is precise: industries begin with fluid phases, in which many competing product architectures exist simultaneously and no one has established which design will become the standard. During this phase, competition is intense, product variation is high, and firm entry rates are enormous. Then a dominant design emerges, not necessarily the best design, but the one that becomes the reference architecture against which all subsequent products are built. After that, competition shifts from "what should the product be" to "who can deliver it cheapest and most reliably." Entry rates collapse, incumbents with production advantages win, and the market that looked like a hundred simultaneous experiments begins to look like a handful of durable competitors.

Steven Klepper's work extended this by documenting the shakeout that follows dominant design emergence with remarkable consistency across industries: automobiles, tires, televisions, hard disk drives. Entry peaks. Then collapses. The survivors are not the original innovators. They are the firms that were best positioned to industrialize the production of the dominant design at scale.

Karim Lakhani at Harvard Business School published a careful reading of the AI model wars through this lens in early 2026. He has described what we are currently in as a kind of "structured ferment," which is more precise than era of ferment alone. Structured means that while the architectural question remains open, competitive asymmetries are already forming underneath the surface noise. The cloud providers have balance sheets that dwarf any foundation model startup. The enterprises that most need AI have existing vendor relationships with SAP, Salesforce, Microsoft, and Oracle that predate the foundation model era by decades. The distribution channels are not neutral. The platform layer is not new.

From inside structured ferment, the market looks like genuine uncertainty. Viewed from outside or from after, it usually turns out that the selection pressures were operating the whole time, just below the threshold where they were visible to the daily benchmark chart.

---

## Why the economics deserve particular attention

There is a data point that I find more useful than any benchmark chart: the cost per million tokens for frontier AI inference has fallen roughly a thousand times in three years. In 2022, using a high-capability model in production was economically prohibitive for most applications. In 2025, it is roughly the cost of sending an email, per call. And total enterprise AI spending grew by over 300 percent in the same period.

This is a pattern that has a name: demand grows faster than efficiency gains can reduce price. In industrial economics, this dynamic produces LLMflation, a term that captures the counterintuitive situation in which prices fall sharply while total spending rises sharply. The unit gets cheaper. The units deployed multiply. The net effect is expanding market, not contracting.

The implication for the technology war framing is significant: this is not yet a zero-sum fight for a fixed market. The cost reduction is simultaneously creating applications that did not exist at prior price points, which means the market boundary is moving. In the browser war, there were a fixed number of people who needed a browser. In AI, the market is being defined by what becomes economical to build at each successive price point.

This changes the timeline. The shakeout may come later than the comparison charts suggest, because the market expansion is absorbing entrants that in a static market would already be losing. But it does not change the structural logic. When expansion slows, the selection pressures that have been forming underneath will become visible all at once.

---

## The complication this cycle adds

I want to be careful here. The dominant design framing from Utterback, Klepper, and Lakhani describes one trajectory: markets move toward a single dominant architecture and then consolidate around the firms that can produce it efficiently. That is one path. There is another: some markets fan out into permanent variety rather than converging. Some markets converge. Others fragment. From inside the ferment, they look identical.

I do not know which trajectory AI is on. What I do know is that several forces are competing to determine it, and they are not the forces that the daily model comparison charts are tracking.

The first is the abstraction layer. When I use a model router that selects between GPT-4, Claude, Gemini, and Llama depending on task type, I am demonstrating that the underlying model is already becoming interchangeable for some classes of task. The router itself, the orchestration layer, the interface through which I never touch the model directly, is the product I am actually using. Perplexity is a product. SAP's Joule is a product. The specific model running underneath is an infrastructure choice that the product makes on my behalf. If the orchestration layer becomes the stable value layer, then the model war resolves by becoming irrelevant at the consumer level, while becoming a cost-of-goods competition at the infrastructure level. The browser moment, not the Google moment. What ended the browser war was not a better browser; it was the application layer shifting to the web, which made the browser a commodity.

The second force is data access monopoly. In healthcare, which multiple credible analysts project will be the largest AI market by 2035, the race is not just for model capability. It is for access to the training data and inference-time context that makes a general model into a clinical-grade system. Medical literature, clinical trial data, real-world evidence, pharmaceutical formulation data: these are not uniformly accessible. A company or consortium that secures exclusive or preferred access to comprehensive medical literature creates a structural advantage that no model quality improvement can overcome, because the competing model cannot be trained on what it cannot see. This is less like the browser war and more like the search war: the link graph was a structural insight that was both technical and about access. Medical data access is the link graph of healthcare AI. It is not yet exclusive. It could become so.

The third force is government. I want to be measured here, because I have read analysis arguing that U.S. government procurement decisions in 2025 and 2026 have already begun to bifurcate the AI market into a commercial track and a national security track, with different regulatory requirements, different personnel clearance constraints, and different infrastructure architectures. This analysis may be correct. Government has shaped technology markets before, the semiconductor industry being the clearest example. It may shape this one. But government intervention is one route, not the only route, and market-shaping forces are not always the ones that look most dramatic in the short term.

---

## What this means for the PM who is not Anthropic or Google

I am not building a foundation model. My job is to build products on top of whatever the infrastructure layer becomes. Which means the question I actually care about is: what is stable, and what is transient?

The comparison charts are tracking the transient. They are precise measurements of performance differences that will largely close as the market matures. Every PM I respected in the search war was tracking which features of the leading engines were durable differentiators and which were lead times that would erode. PageRank was a durable differentiator. Index size was a lead time that would erode. Knowing the difference was not obvious in 2000. It became obvious by 2005.

The stable layer in this cycle is not the model. It is the data, the orchestration, and the workflow integration. Which model sits underneath is a detail the product decides invisibly, the way an application decides which database engine to query or whether to write the backend in Java or C#. The user never sees it and, increasingly, does not need to care. The context the model receives, the business rules it operates within, the approval workflows it sits inside, the audit surfaces it writes to, the organizational trust it must earn: these are product decisions that compound over time in ways that model quality improvements do not displace.

Running four models in parallel is not a strategy. It is an acknowledgment that I do not yet know which one will be the stable production choice for each task type, and I refuse to prematurely converge. Every PM who picked Lotus 1-2-3 as their spreadsheet standard in 1990 had to migrate. Every PM who standardized on a browser in 1997 had to migrate again. The cost of premature convergence is high. The cost of maintaining optionality is the slight embarrassment of explaining to colleagues why your AI stack looks like a museum of every model released in the last eighteen months.

I will take the embarrassment.

---

## The thing the comparison charts are not measuring

Here is what I have learned from living through multiple technology wars: the thing that ends the ferment is almost never the product innovation that the comparison charts are tracking. It is a structural event that the charts were never designed to see.

The spreadsheet war ended with a licensing bundle, not a formula engine improvement. The browser war ended with an operating system monopoly enforcement action, not a rendering engine breakthrough. The search war ended with an architectural insight about the structure of the web itself, which was both a technical advance and a data access claim nobody else had made.

The AI model war will end with something structural. It might be data access. It might be platform integration. It might be a regulatory architecture that makes some models deployable in regulated industries and others not. It might be the abstraction layer becoming the product and the model becoming interchangeable infrastructure. It might be something I have not named because I cannot see it yet from inside the ferment.

What it will not be is the model that scores highest on the benchmark chart published this week.

The comparison charts are a weather report. Every product manager I know reads the weather. The ones I respect are also reading the geology: the slow-moving structural forces that will determine what is possible in this landscape over the next decade, and that cannot be measured in milliseconds or tokens per second.

I run four models in parallel because I respect the geology. I ignore the daily comparison charts because I do not want to confuse weather with terrain.

The wars always end. The question is not which product wins the week. It is what layer of the stack becomes the stable ground.

---

*This article is part of an ongoing series on AI product design, healthcare data, and the human side of technology adoption.*
