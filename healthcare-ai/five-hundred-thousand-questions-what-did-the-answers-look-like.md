---
title: Five Hundred Thousand Questions. What Did the Answers Look Like?
slug: five-hundred-thousand-questions-what-did-the-answers-look-like
published: 2026-04-17
excerpt: Microsoft just analyzed 500,000 Copilot health conversations. The paper is honest: they observed questions but not outcomes. The physician in me cannot stop thinking about it. In medicine we audit what happened to the patient, not just what we considered. Why should AI be different?
url: https://data-decisions-and-clinics.com/five-hundred-thousand-questions-what-did-the-answers-look-like/
tags: Healthcare AI
source: ghost-api-pull-2026-08-04
---

Microsoft AI just published a careful analysis of more than five hundred thousand health-related conversations with Copilot in a single month. The paper is clean, honest, and does something useful. It also states plainly, on page four of the methods, that they observe questions but not outcomes.

That admission is what I cannot stop thinking about.

The findings themselves are interesting. About one in five conversations involve personal symptom assessment or condition management. One in seven are caregivers asking about someone else, a child, a parent, a partner, who never touches the interface. Mobile is where the worried parent lives. Desktop is where the paperwork gets done. Emotional well-being queries rise more than fifty percent from morning to midnight, peaking exactly when clinicians are unreachable. The picture is concrete and statistically robust. The researchers deserve credit for a difficult measurement done well.

The product manager in me is excited to see this kind of data. It can help fine-tune the model, improve the user experience, and reveal interaction patterns that design reviews usually miss. A worried parent at midnight is not a persona anyone would have drafted in a design workshop. This paper makes them visible, at scale, with statistical confidence, and with enough granularity to inform platform-specific design. That is a real contribution.

The physician in me is less comfortable. These users are not running through test scenarios. They are asking about their own symptoms, or about a child, or about an aging parent, at times when no clinician is reachable. The AI answered them. We know what was asked. We do not know what was said in return, whether it was correct, whether it helped, or whether it led them somewhere safe.

In medicine, we do not stop at the question. A chart that recorded only what a physician considered, with no record of what they did or what happened to the patient, would be an indictment of the institution that produced it. We audit outcomes. We track readmissions, complications, missed diagnoses, mortality. We distinguish between what was asked and what came of it, because in clinical work those are fundamentally different. The first is cognition. The second is consequence. A medical record without outcomes is not a record. It is a conversation transcript.

The Copilot paper has the cognition. It does not have the consequence, and nothing in the current architecture of consumer health AI produces it.

That is not a failure of the paper. It is the state of the field. When a user at midnight asks Copilot about their child's fever, the AI answers, the conversation ends, and the institution that ran the exchange has no visibility into what happened next. Did the parent wait? Did they drive to an emergency department? Did they give acetaminophen and watch? Was the advice appropriate? Was the fever viral or bacterial? Did the child recover in the morning or get worse?

Five hundred thousand instances of that blind spot in a single month, just on one platform. That is the gap the paper documents honestly, by admitting what it could not see.

Other high-stakes fields have worked out, painfully and over decades, what it takes to measure the answers and not just the questions. Pharmaceutical medicine is the clearest example. Mandatory post-market surveillance infrastructure, funded by industry through user fees, triggered by statute, connecting clinicians, patients, manufacturers, and regulators in a shared system that captures what happens after the prescription gets written. Troglitazone was withdrawn because of a pattern of liver toxicity that showed up in adverse event reports. The JAK inhibitor boxed warnings came from a signal that accumulated across thousands of post-market cases. The mechanism is not fast and not perfect, but it exists.

Consumer AI health has none of this. Not the mandatory reporting, not the funding stream, not the infrastructure to aggregate signals across platforms, not the statutory trigger that forces a label change when a pattern of harm accumulates. What it has is voluntary guidance, a Coalition for Health AI registry still in development, and platforms studying themselves.

The Microsoft team should not need to solve this alone, and I do not think the paper is trying to. It would be unfair and also unlikely to work. Pharmacovigilance infrastructure in drugs was not built by a single manufacturer. It was built by regulators, professional societies, insurers, and patient advocacy groups over decades, with substantial pushback along the way. What it took was a combination of mandate, funding, and a shared understanding that the supply side of a health intervention needs to be measured as carefully as the demand side.

The Microsoft paper is, in fact, a useful first step in that direction. It establishes the demand side at scale. Five hundred thousand questions is not a small signal. The taxonomy they developed is exportable. The privacy-preserving pipeline is reproducible. The pattern by time of day and device is the kind of observation that helps us design better supply-side measurement.

What would the supply side look like at the same scale? It is not one thing. It would probably include randomized evaluation of Copilot outputs against clinician panels on a rotating sample, which is technically doable today. It would include longitudinal follow-up of users who asked high-stakes questions, which requires governance that does not yet exist. It would include an adverse event reporting mechanism that patients and clinicians can use when an AI recommendation contributes to harm, which again requires institutional infrastructure nobody has built. It would include honest disclosure of how often the model declined to answer, how often it escalated, and what happened when it did.

None of that exists at scale today. All of it is within reach if the field decides it matters.

There is also the caregiver layer, which I keep coming back to. One in seven queries in the Microsoft data is a caregiver asking about someone who never touches the product. That is roughly seventy thousand conversations a month where a third party is making a health decision for a patient who has no relationship with the interface, no consent chain, and no way to know what was asked or answered on their behalf. In any other clinical context this would be a documented encounter with a chart note. Here it is a conversation transcript and a blind spot combined.

Here is the question I am left with, and I suspect I am not alone. If the demand side of health AI is worth five hundred thousand data points in a Nature Health paper, what do the answers need to be worth before we measure them with the same rigor?

Where technology meets people, the question is never only what they asked. It is what they got, and what came of it.

*This article is part of an ongoing series on AI product design, healthcare data, and the human side of technology adoption.*
