---
title: "The Guide Is Not the Business"
slug: the-guide-is-not-the-business
published_at: 2026-04-27T15:42:44.000Z
custom_excerpt: "Amazon owns the patient at the moment of health decision intent. OpenEvidence owns the physician at the moment of prescribing intent. Both are monetized by the same pharmaceutical industry. The prescription is the handshake between them."
tags: [healthai]
feature_image: https://storage.ghost.io/c/e6/05/e605b234-3cc8-4fe4-97bb-2bb55b18b8fb/content/images/2026/04/ChatGPT-Image-Apr-27--2026--11_40_42-AM.png
source: ghost
---

# The Guide Is Not the Business

In 1900, Michelin published a free guide to French restaurants, hotels, and gas stations. It was beautifully researched, editorially independent, and distributed at no cost to drivers across France.

It lost money every year.

It still does. The guide reportedly costs Michelin roughly $24 million annually to produce and distribute, by one widely cited estimate. By any conventional accounting, it is a failure.

Except that Michelin sells tires. And people who trust the guide drive to restaurants worth a detour. Detours wear tires. The guide is not the business. The guide is the behavior modifier that makes the business possible.

I have been thinking about Michelin since I walked through the Amazon Health funnel two weeks ago, and again after watching OpenEvidence raise capital at a valuation that makes no sense if you think its business is medical search.

It makes complete sense if you understand what Michelin figured out in 1900.


## Two funnels, one prescription

A few weeks ago I needed an antibiotic cream. In most of Europe, you walk into a pharmacy and buy it. In the United States, it requires a prescription. I found the drug while searching on Amazon, which now has detailed pharmaceutical product pages with clinical information and a button to request a prescription. I clicked the button.

What followed was a precise, well-designed funnel. Amazon OneCare, which looks exactly like any other Amazon page. A $29 visit fee, waived through a Prime offer I did not fully understand. An AI questionnaire that took under five minutes. Two hours later, a human provider had reviewed my submission and the prescription was at my local pharmacy. Amazon had completed its first clinical transaction with me.

Now consider what happened on the other side of that prescription.

Somewhere in that chain, a physician-facing AI platform had likely influenced the evidence that informed the prescribing decision. Not at my specific visit. But at the layer where clinical knowledge gets synthesized, ranked, and surfaced to the 350,000 physicians who use OpenEvidence more than one million times a day, a platform monetized at CPMs between $70 and $1,000, paid by pharmaceutical companies, for access to verified physicians at the exact moment of clinical decision-making.

Amazon owns the patient at the moment of health decision intent. OpenEvidence owns the physician at the moment of prescribing intent. Both are monetized by the same pharmaceutical industry. The prescription is the handshake point between them.

That handshake is where a new conflict of interest lives. When physician knowledge and patient access are both funded by pharmaceutical advertising and commerce, accuracy becomes a constraint on growth rather than the product itself. This is not a healthcare strategy. It is a two-sided market built around the most valuable transaction in the $5.3 trillion US healthcare economy.


## The pattern has a name

The structure both platforms are running has been documented in business literature for over a century, though it goes by several names depending on which mechanism you emphasize.

The canonical term is razor-and-blades: sell the handle at cost or below to create dependency, then extract margin from the consumable the customer must buy to use what they already own. Gillette's competitors perfected this after his patents expired in 1921, turning a 20% sales decline into 127% growth in a single year. HP sells printers at minimal margin and charges ink cartridge markups estimated at 1,000 to 4,000 percent. Nespresso sells machines at commodity pricing and extracts margin from proprietary aluminum pods. The handle is a customer acquisition device. The blade is the business.

The digital variant is the attention platform: offer the most useful free product available to a defined audience, then sell access to that audience to a third party who values their attention. Google gives you search; advertisers pay $60 to $80 per user annually for the intent signal your searches generate. Facebook gives you social connection; advertisers pay for the behavioral profile your connections reveal. The user is not the customer. The user is the inventory.

OpenEvidence and Amazon Health are running the attention platform model, with one modification that makes it more defensible than either Google or Facebook: the audience cannot be replicated.

Google sells consumer intent signals. Any sufficiently large platform can assemble consumer intent signals. OpenEvidence sells verified physician attention — credentialed by NPI number — at the moment of clinical decision-making. That audience requires credentialing infrastructure, clinical trust, and a product good enough that physicians choose to use it in the workflow moments that matter. The CPM premium, $70 to $1,000 versus $5 to $15 on consumer social media, reflects the irreplaceability of the context, not just the size of the audience.

Amazon's patient-side funnel is harder to replicate because it sits inside the largest consumer commerce platform in the world, with Prime membership, connected health records via FHIR, an integrated pharmacy, and the behavioral data of hundreds of millions of existing customers. Building that stack from scratch is not a startup problem. It is a decade-long infrastructure problem.

The knowledge, the clinical evidence on OpenEvidence, the health information on Amazon, is not the moat. It is the cost of acquiring the relationship that is the moat. Michelin's restaurant ratings are not the moat either. Any publication could rate restaurants. The moat is 120 years of anonymous inspectors, global editorial authority, and a behavior change that turns trust into tire demand.

The content is the cost. The relationship is the business.


## What this means for the quality of the knowledge

For a hundred years, medical knowledge had a different relationship with commercial interest than it does today.

This is not a naive claim. Pharmaceutical companies have always advertised in medical journals. CME has always attracted pharma sponsorship. Medical publishing has never been a nonprofit enterprise. The wall between clinical knowledge and commercial interest was never perfect.

But the optimization target was different. A journal optimized for subscription revenue needs to publish accurate things, because its credibility is its product. A peer-reviewed journal that publishes findings later shown to be commercially shaped loses subscribers, authors, and reputation. The commercial incentive and the accuracy incentive pointed in roughly the same direction.

An attention platform optimized for engagement has a structurally different incentive. Engagement and accuracy are not the same thing. They are not even reliably correlated. Content that generates physician time-on-platform, return visits, and click-through to adjacent material can do all of those things while systematically emphasizing certain treatment modalities over others, not through fraud, but through the gradual accumulation of editorial choices that favor the audience pharmaceutical companies most want to reach.

The mechanism is not conspiracy. It is architecture.

To see how this plays out, consider a hypothetical: a cardiologist searching for management of symptomatic aortic stenosis. Evidence-based guidelines favor intervention: TAVR and surgical valve replacement carry documented mortality benefits over medical management in most patient categories. But a platform whose revenue depends on pharmaceutical advertising has a structural pressure, even with completely clean editorial intentions, to surface content that generates prescribing-adjacent attention. Medical management trials appear. Drug therapy options are presented first. The evidence for procedural intervention is accurate but requires one more click to reach. The physician still sees evidence-based content. The selection and ranking of that evidence has been shaped by an incentive structure the physician cannot see.

This is not hypothetical. It is the documented history of pharmaceutical influence on medical knowledge intermediaries, now running on a new substrate.

To be clear: no independent audit has yet shown that OpenEvidence itself has biased recommendations toward advertised drugs. The risk described here is structural and prospective, grounded in how similar revenue models have behaved in every other part of the system.

The cases are not ancient history. Wyeth used a medical writing firm to produce dozens of ghostwritten papers promoting hormone therapy while downplaying breast cancer risks, documented through thousands of unsealed court documents. Merck's promotion of Vioxx involved ghostwritten articles that omitted participant deaths from published clinical trial reports. GSK misrepresented pediatric trial results for Paxil. Each case moved through peer review with named academic authors in major journals. The peer review process did not catch it. The journals did not catch it. What caught it, in every case, was litigation discovery.

The COURAGE trial, which demonstrated in 2007 that stents offered no survival advantage over optimal medical therapy for stable coronary artery disease, is the most cited example of how this plays out at the institutional level. Despite the evidence, practice change was slow. Subsequent investigations found that key cardiology professional societies derived a large share of their revenue from device and drug manufacturers, and that industry advisory boards acknowledged they had done "a better job promoting PCI than policing it." This was not a conspiracy. It was a structural incentive producing a predictable outcome.

## The legal precedent: Practice Fusion

The most direct legal precedent for what this looks like inside a clinical AI platform is Practice Fusion. In 2020, the Department of Justice revealed that Practice Fusion, a free-to-clinician, ad-supported EHR platform, had accepted payments from pharmaceutical companies to embed prescribing prompts inside its clinical decision support system. The prompts appeared as unbiased clinical guidance. They were purchased. The US Attorney described it as having pharma's "thumb on the scale at precisely the moment a doctor was making incredibly intimate, personal, and important decisions about a patient's medical care." Practice Fusion paid $145 million to resolve the criminal charges.

Google Search's degradation followed a specific trajectory. First, sponsored results were clearly labeled. Then the boundary blurred. Then search engine optimization grew as an industry specifically to game the organic results, not just buy the paid ones. A search for a medical symptom today returns content optimized for search ranking and advertising revenue. The platform whose founders described it as correcting that problem now runs on the same revenue model that caused it.

The Michelin condition is the thing worth holding onto here. The blade has to work, or you lose the platform. Michelin's guide maintained credibility for 120 years because honest ratings were the mechanism that drove the behavior (driving to restaurants) that wore the tires. Accuracy was not a value in tension with the business model. It was the business model.

The question for OpenEvidence and similar platforms is whether that condition holds. If physicians detect commercial shaping of clinical content, they leave. The audience evaporates. The pharma CPM collapses. In that sense, clinical accuracy is structurally incentivized. The platform only works if physicians trust it.

But physicians are not the only ones who need to trust it. And the patient side of this equation is in a different position entirely.


## What pharma SEO looks like when it moves to AI

In the current search environment, pharmaceutical companies are already exploiting what the industry calls the "search loophole." FDA regulations prohibit promoting drugs for off-label use, but pay-per-click ads can contain so little text that they avoid making any direct therapeutic claim. A company making a diabetes drug can bid on the keyword "weight loss" without triggering fair-balance disclosure requirements. The intent is monetized. The claim is never technically stated.

This is already transitioning into AI-driven environments. Instead of keywords, advertisers will bid on conversational context. A physician querying second-line options for treatment-resistant hypertension could see a response in which one drug class is fractionally more prominent, not because the evidence is better, but because the manufacturer paid for that context.

The structural asymmetry runs deeper. Pharmacological management is amenable to advertising. Procedures are not. A device company cannot bid on a clinical query the way a pharmaceutical company can. Over time, the evidence that gets surfaced first is the evidence adjacent to revenue.

This does not require a conspiracy. It does not require anyone at OpenEvidence to make a single corrupt editorial decision. It requires only that the algorithm learns what generates engagement, and that engagement on a pharma-funded platform is structurally correlated with pharmacological content. The bias would be invisible from the inside and difficult to detect from the outside without independent algorithmic audits that no regulatory body currently requires.

## The asymmetry that matters

When a physician uses OpenEvidence, they bring years of clinical training, specialty knowledge, and the ability to evaluate whether a summary of evidence matches what they know from their own practice. They can detect when something is missing, when a study being cited is funded by the drug manufacturer, when the framing of treatment options does not match the guideline they read last month. The Michelin condition holds for physicians, imperfectly but meaningfully, because they can verify the food.

When a patient uses Amazon Health, they cannot.

## The equity problem

The 1 in 3 Americans now using AI for health information includes, according to KFF data from early 2026, a disproportionate share of people using it because they cannot afford or access traditional care. Among AI health users aged 18 to 29, 38% cited not having a provider or not being able to get an appointment as a major reason. Among users with household incomes under $40,000, one-third cited cost. Uninsured adults are twice as likely as insured adults to use AI for mental health advice.

These are not patients with a regular physician who can verify the recommendations they receive from a consumer health platform. For many of them, the AI is not a step in the care process. It is the entire process.

## Who replaces the wall?

The wall between medical knowledge and patients is coming down. I believe that is mostly a good thing. The physician knowledge monopoly was never purely about quality; it was about gatekeeping, and it served physicians as much as it served patients.

But the wall also enforced something that is not being replaced: a separation between clinical knowledge and commercial interest. Imperfect, but structural. A physician at the point of prescribing was not being paid by a pharmaceutical company. The information infrastructure behind them was funded by institutions whose interests were roughly aligned with accuracy.

What we are building now has no such accident in its favor.

The question nobody is asking loudly enough: who is building the governance to replace what the wall provided?

The Michelin guide works because a tire company's commercial interest happened to align with honest restaurant ratings. That alignment was an accident of the specific business model, not a design choice. Clinical AI running on pharmaceutical advertising revenue does not have that accident in its favor.

When Michelin's inspectors write reviews, they are answering to a tire company whose interest is in accurate information. When an algorithm ranks clinical evidence on a platform funded by pharmaceutical CPMs, it is answering to a revenue model whose interest is in physician engagement with pharmaceutical-adjacent content.

Those are not the same thing.

And unlike the restaurant, the patient cannot send the food back.

---

*The Signal Series — Healthcare Data Infrastructure*

---

*Note to self before publishing: the article makes structural and prospective arguments grounded in well-documented historical precedent. No peer-reviewed study has yet demonstrated that OpenEvidence specifically has biased clinical recommendations toward advertised drugs. That finding is absent because independent audits have not been conducted, not because the platform has been cleared. The article should be read as a structural warning, not an accusation of documented harm.*
