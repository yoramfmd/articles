---
title: "What You Owe the People Who Will Never Be in the Room"
slug: what-you-owe-the-people-who-will-never-be-in-the-room
published_at: 2026-03-24T15:47:00.000Z
custom_excerpt: "The people most affected by your AI product are almost never in the room when you build it. They don't appear in your analytics. They weren't in the meeting when the roadmap was approved. They will never give you feedback. You owe them something anyway"
tags: [pm, people]
feature_image: https://storage.ghost.io/c/e6/05/e605b234-3cc8-4fe4-97bb-2bb55b18b8fb/content/images/2026/03/Gemini_Generated_Image_me99dgme99dgme99.png
source: ghost
---

[*The previous articles*](https://data-decisions-and-clinics.com/there-is-no-certification-for-this/)* were about skills. This one is about obligations.*

---

In 1971, a British physician named Julian Tudor Hart proposed what he called the inverse care law: the availability of quality medical care varies inversely with the need for it. The populations who are sickest get the least care. The populations with the fewest resources have the fewest options.

Fifty years later, a study published this week in *NEJM AI* applied Hart's principle to artificial intelligence in healthcare. The finding: rural areas have higher mortality rates, higher chronic disease burdens, and greater clinical need than urban areas. They also have lower interoperability infrastructure, lower AI adoption, and lower large language model readiness. Where the need for AI is greatest, the capacity to use it is lowest.

This is not a coincidence. It is the same pattern Hart described, now operating one layer up, in the infrastructure that determines who benefits from innovation. And for anyone building AI products that affect health decisions, it is not an academic finding. It is an obligation.

---

## Accountability Is a Design Decision, Not a Policy

When the AI is wrong and something goes wrong as a result, the question of who is responsible does not answer itself. The model cannot be accountable. The team cannot be accountable. A specific person has to be.

This is not a governance question to resolve after launch. It is a design question that belongs at the beginning. Who owns the decision when the system and the human expert disagree? What happens when the AI recommendation is followed and the outcome is bad? What happens when it is overridden and the outcome is bad? How is that override recorded, and by whom, and available to whom, and when?

If you have not answered those questions before you ship, you have not finished designing the product. Accountability is not a policy you add to the documentation. It is an architecture decision, and it has to be made deliberately, before anyone is under pressure to make it carelessly.

The PM who defers this question to legal or compliance has not resolved it. They have transferred it. And the person who eventually has to answer it, under the worst possible circumstances, will not thank them for that.

---

## Equity Means Looking Inside the Error Rate

A model at 94% accuracy looks like a success. The question you have to ask is: who is in the 6%?

A credit model trained on historical data will underperform for first-generation borrowers who built creditworthiness through patterns that were never in the training set. A hiring algorithm trained on past successful hires will systematically discount candidates whose career paths do not match the historical template. The aggregate accuracy looks fine. The harm is invisible in the summary.

The inverse care law paper adds something precise to this argument: a name for the mechanism. It is called distribution shift. Clinical AI systems are primarily trained on data from large metropolitan academic centers. When those systems are deployed in rural settings with different disease patterns, different patient populations, and different resource constraints, their performance degrades. The gap between the population the model learned from and the population it is now being applied to is not a bug that will be caught in QA. It is structural. It is baked into the training data before the first line of code is written.

The numbers are not abstract. Rural areas have mortality rates that were 7% higher than urban areas in 1999; by 2019 that gap had widened to 20%. Psychiatrists are available at roughly 14 per 100,000 people in metropolitan areas; in rural areas the number is 2. Rural suicide rates are nearly double those in urban areas, a gap that has widened substantially in recent decades. Mental illness prevalence is similar across geography. Access to care is not.

These are the populations in the 6%. Not as a metaphor. As a structural prediction about who will bear the cost when a model trained on one population is evaluated against the performance standards of another.

If the answer to "who is in the 6%" is a specific population, consistently, the product is not 94% accurate. It is accurate for some users and failing others entirely. That distinction does not show up in aggregate metrics. It does not trigger an alert. It requires someone with enough domain knowledge and enough conviction to go looking for it before launch, and to refuse to ship when they find it.

The tools to measure disparate performance exist. The question is whether anyone on the product team made it their responsibility to use them. If you did not build that check into the definition of done, no one else will do it.

---

## You Are Designing for the Wrong Person

The user of your product and the person affected by your product are often not the same. A clinician uses the tool. A patient lives with the output. A hiring manager sees the ranked list. A candidate gets the rejection. A loan officer enters the data. An applicant gets the decision.

The inverse care law adds a third layer: the institution adopting the tool and the patient population it serves are also not the same. A health system with robust infrastructure adopts the AI. The patients served by a rural clinic with limited interoperability get a version of care shaped by what that AI says about populations it was never trained on. The decision to deploy was made by people in a room. The consequence is felt by someone who will never be in that room.

This gap has always existed in software. AI widens it. When the system makes a recommendation and a human acts on it, the person acting is insulated from the person experiencing the consequence. That insulation makes it easy to optimize for the user's experience without considering what the affected person needs.

Designing across that gap requires holding two questions at once: does this work for the person using it, and is this fair to the person affected by it. Those questions do not always have the same answer. When they conflict, you have to make a deliberate choice rather than defaulting to whichever one is easier to measure.

One concrete version of this is evaluation standards. The inverse care law paper makes a point that product teams rarely ask: AI tools in healthcare should be measured against the care that currently exists in the setting where they will be deployed, not against an idealized standard that no one in that setting can currently access. A diagnostic AI that performs at 90% of urban specialist level sounds impressive. In a rural community where the alternative is no specialist at all, it may still be the right tool. The evaluation standard shapes what gets built and what gets deemed acceptable. That standard is a product decision.

---

## Knowing What Should Stay Human

Some decisions should not be delegated to an algorithm, regardless of how accurate the model is.

This is not a technical claim. It is a moral one. There are decisions where the act of explanation, the ability to be questioned, and the willingness to say "I made this call and here is why" are part of what makes the decision legitimate. An algorithm can be accurate. It cannot be accountable in the way that some decisions require.

In settings with limited infrastructure, limited physician availability, and populations that have historically had reason to distrust health systems, this question is more fraught, not less. An AI system deployed in a context where the only alternative is no care at all carries a different weight than the same system deployed in a well-resourced academic medical center. The obligation to think carefully about what should stay human does not diminish in underserved settings. It intensifies.

The PM who does not think about this before the product is built will be forced to think about it after something goes wrong. The PM who thinks about it in advance can draw the line in the right place, defend it when there is pressure to move it, and build a product that earns the trust it asks for rather than demanding trust it has not earned.

---

## What These Have in Common

Each of these obligations points at the same thing: there are people affected by your product who will never give you feedback, never appear in your analytics, and never be in the room when you make the decisions that shape their experience.

Hart proposed the inverse care law in 1971 as a description of how medical systems distribute care. He was not prescribing a failure mode. He was describing an observed pattern: resources flow to those who are best positioned to seek and use them, which means they flow away from those with the greatest need. He proposed it as something to resist, not accept.

The new data shows the same pattern is reproducing in AI. This is not inevitable. It is a product decision being made, often by omission, by the people building the tools. The populations bearing the cost of that omission are already carrying the highest burden of illness, the fewest options for care, and the longest history of being excluded from the systems designed to help them.

These are not skills you develop over time. You either hold these standards or you do not, and the difference shows up in the choices you make when no one is watching, when the timeline is compressed, when the commercial pressure is high, and when the person affected by the outcome will never know your name.

That is most of the time.

---

*Reference: Hwang Y, Rice BT, Hernandez-Boussard T. The Inverse Care Law in the Age of AI: Geographic Disparities in Health Care Technology Access. NEJM AI. Published March 25, 2026. DOI: 10.1056/AIp2600103*