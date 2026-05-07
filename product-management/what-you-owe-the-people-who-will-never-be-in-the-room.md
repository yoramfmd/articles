# What You Owe the People Who Will Never Be in the Room

*Article 2 was about skills. This one is about obligations.*

---

The first two articles in this series were about skills: what companies should hire for, and what PMs need to build in themselves. Skills are what you develop over time. Obligations are different. They are what you carry regardless of whether anyone is checking.

The PMs who do this work well are not just more competent. They are more serious about what their products do to real people. In the age of AI, that distinction matters more than it ever has. The gap between what a product can do and what it should do is wider than with any previous generation of tools, and the consequences of getting it wrong travel faster and farther.

You will not find these obligations in a job description. They are not in any PM framework. But if you are building AI products that affect consequential decisions about real people, you carry them anyway.

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

If the answer is a specific population, consistently, the product is not 94% accurate. It is accurate for some users and failing others entirely. That distinction does not show up in aggregate metrics. It does not trigger an alert. It requires someone with enough domain knowledge and enough conviction to go looking for it before launch, and to refuse to ship when they find it.

This is not a technical problem. The tools to measure disparate performance exist. The question is whether anyone on the product team made it their responsibility to use them. If you did not build that check into the definition of done, no one else will do it.

The populations inside the error rate are almost always the ones least represented in your discovery process. They are not in your user interviews. They are not in your beta cohort. They are not in the meeting when the roadmap gets approved. You have to go looking for them deliberately. If you do not, you will ship a product that works well for the people who already had access to things that work well.

---

## You Are Designing for the Wrong Person

The user of your product and the person affected by your product are often not the same. A clinician uses the tool. A patient lives with the output. A hiring manager sees the ranked list. A candidate gets the rejection. A loan officer enters the data. An applicant gets the decision.

This gap has always existed in software. AI widens it. When the system makes a recommendation and a human acts on it, the person acting is insulated from the person experiencing the consequence. That insulation makes it easy to optimize for the user's experience without considering what the affected person needs.

Designing across that gap requires holding two questions at once: does this work for the person using it, and is this fair to the person affected by it. Those questions do not always have the same answer. When they conflict, you have to make a deliberate choice rather than defaulting to whichever one is easier to measure.

One concrete version of this is cognitive fatigue. Designing for someone at the end of a high-volume day is not the same as designing for an attentive user in a usability lab. If your product requires careful attention to use correctly, and your users are systematically exhausted, you have designed for a person who does not exist in your actual deployment context. The product will behave as designed. The outcomes will not be what you intended.

---

## Knowing What Should Stay Human

Some decisions should not be delegated to an algorithm, regardless of how accurate the model is.

This is not a technical claim. It is a moral one. There are decisions where the act of explanation, the ability to be questioned, and the willingness to say "I made this call and here is why" are part of what makes the decision legitimate. An algorithm can be accurate. It cannot be accountable in the way that some decisions require.

The PM who does not think about this before the product is built will be forced to think about it after something goes wrong. The PM who thinks about it in advance can draw the line in the right place, defend it when there is pressure to move it, and build a product that earns the trust it asks for rather than demanding trust it has not earned.

Where the line sits is not always obvious, and it shifts depending on the stakes, the context, and the populations involved. But the obligation to find it before you ship is not negotiable. If you are not sure where the line is, that uncertainty is itself a signal that you have more work to do.

---

## What These Have in Common

Each of these obligations points at the same thing: there are people affected by your product who will never give you feedback, never appear in your analytics, and never be in the room when you make the decisions that shape their experience.

These are not skills you develop over time. You either hold these standards or you do not, and the difference shows up in the choices you make when no one is watching, when the timeline is compressed, when the commercial pressure is high, and when the person affected by the outcome will never know your name.

That is most of the time.

The PMs who carry these obligations are not more cautious or slower. They build better products. And in an industry moving as fast as AI, that is exactly what serious looks like.

---

*This is the third article in a series on what it takes to lead AI product work. Each piece stands on its own.*
