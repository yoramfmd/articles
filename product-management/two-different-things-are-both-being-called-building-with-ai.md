---
title: Two Different Things Are Both Being Called "Building with AI"
slug: two-different-things-are-both-being-called-building-with-ai
published: 2026-06-18
excerpt: Two things are both called "building with AI." One makes small teams faster at familiar products. The other ships products that act on their own, and that one needs a bigger, more senior supervisory layer, not a leaner pod. The ICU knew this before software did.
url: https://data-decisions-and-clinics.com/two-different-things-are-both-being-called-building-with-ai/
tags: Product Management
source: ghost-api-pull-2026-08-04
---

---

There is a conversation happening on every software team right now, and most of the people in it are talking past each other without realizing it. They are using the same words, AI and agents and the new way of building, and they mean two completely different things.

Here is the distinction in one line. One kind of AI work makes small teams faster at shipping familiar products. The other creates products that act on their own, and that kind needs a bigger, more senior supervisory layer, not a leaner one.

The confusion is costing teams real money, because the two things require two different team models, and most organizations are applying the wrong one.

Let me draw the line as clearly as I can.

## The first thing: AI-empowered teams building conventional products

A team ships a new feature for a retail app. Another ships the next release of an enterprise data platform. A third builds an analytics dashboard. The product is conventional. It is predictable, consistent, and familiar, because as an industry we have been building products like this for fifty years.

What changed is the team, not the product. AI made every craft faster. It crunches the scrum process down from a sprint to an afternoon. It blurs the seams between the product manager, the engineer, and the designer, because the model now does a large share of the translation, the code, and the comps. It empowers each member in a different way, and it rewards the person who already has deep judgment while quietly removing the apprenticeship that produced that judgment.

This is real, and it is most of what the industry means when it says AI is changing how we work. The "AI pod," the lean, capability-organized team that Meta, Microsoft, Shopify, and the major consultancies are now restructuring around, is the answer to exactly this. Fewer people, more senior, judgment over execution, review as the new bottleneck. Meta named the roles, AI Builder, AI Pod Lead, AI Org Lead, and cut thousands of roles to get there.

I want to be clear that this is a good move, and in many cases the correct one. If your product is a conventional one, the pod is a faster, leaner way to build it. The caution is not about the pod. It is about what happens when the same team starts building products that act on their own, which brings me to the second thing.

## The second thing: teams building agentic products

If the first story is "AI makes the team faster," the second is "the product itself becomes an actor."

A team builds a refund agent. A triage agent. A claims agent that decides and acts on its own.

This team also uses AI to write its code, so it lives the first story too. But the product it is shipping is a different kind of thing, and that difference changes the work in ways the productivity story never touches.

A conventional product does what it was told, every time. An agentic product decides. And the moment a product decides, four things become true that were never true before.

- It has behavior that has to be understood, not just specified. You do not test every path, because the agent is capable in ways you cannot fully enumerate and unreliable in ways you cannot fully predict.
- It has a lifecycle that moves. It climbs an autonomy ladder, from suggesting, to drafting, to acting with approval, to acting on its own. Each rung is a different product with a different risk profile, and you earn the next rung by demonstrated behavior, not by scheduling it because the roadmap said so.
- It can fail silently. It keeps producing fluent, plausible, confident output while its real performance slides for months, in a direction no instrument on the team is pointed at, because the dashboards measure what they measured at launch.
- It is often faceless. The person who lives with its decision, the claimant, the patient, the applicant, never sees the interface and was never in the room when the team designed it.

None of that is a productivity problem. It is a different product, and it needs a different team.

## Why the team model actually differs

Here is the part most teams miss. The first model makes the team smaller. The second model makes it larger, and in a specific direction.

Building a conventional product faster is a convergence story. The crafts collapse toward judgment, and a lean pod of generalists can carry the throughput of a team twice its size.

Building an agentic product is a different shape, because every agentic product is really two products. The first is the agent, the thing that decides and acts, the part everyone means when they say they are building an agent. The second is the layer that supervises it: how a human sees what the agent is doing, intervenes before it does something irreversible, investigates when it goes wrong, and stays accountable for the result.

Every team knows how to build the first. The second is the one they forget. And the second needs owners the old product triad never had:

- Someone who can say whether the agent is still correct, not just still running.
- Someone whose actual job is to watch the running agent in production.
- Someone who knows what the agent cannot see.
- Someone who holds the interest of the person who is not in the room.

The lean pod deletes those seats. The agentic product depends on them. That is the whole tension, and it is why you cannot run an agentic team on a conventional team's org chart, however good the agent is.

Some organizations are trying to add supervision back through a separate risk, governance, or safety team. That helps, but it rarely lands, because those roles are given a mandate without real authority and sit outside the pod's charter, watching from across the room instead of owning a seat in it. Supervision that cannot stop the agent is not supervision. It is commentary.

## There is a line on the autonomy ladder, and the pod is built for below it

The two stories are not really two products. They are two halves of one ladder, and there is a line across it.

Below the line, the system proposes and a human executes. Rung one, it suggests. Rung two, it drafts and a person commits. Mistakes are recoverable by construction, because nothing reached the world without a human hand on it. This is the governance posture we have run for two decades on workflow and process automation. We know how to do this. The AI pod is the right team for it.

Above the line, the system touches state. It acts with approval, then acts with oversight, then acts on its own. And at that line, supervision stops being a review step a person does at the end and becomes a product the team has to build: how you see what the agent did, how you stop it before the irreversible action lands, how you investigate when it goes wrong, how you stay accountable for it.

This is the part that matters for anyone reorganizing right now. The pod is the correct, efficient answer for rungs one and two. The trouble is that no company stays on rungs one and two. The whole direction of travel is up the ladder, toward agents that act, and the team that was perfect for "AI helps us build faster" is missing exactly the seats that "the agent acts on its own" requires.

## The quiet bet companies are making, and may lose

Here is the move I watch with some worry. A company sees that AI now does the production work, cuts its experienced product people, and runs lean. While the products stay on the low rungs, this looks brilliant. Then it starts shipping higher up the ladder, because that is where the value is, and the judgment it cut, who decides whether the agent should have acted, whether it is drifting, whether it is safe for the person on the receiving end, is exactly what the higher rungs demand more of, not less. The senior judgment was removed in the season it looked optional, and it is needed most in the season when it becomes load-bearing.

The trap is self-concealing. That judgment was earned by people doing the production work the agent now does, so cutting the people removes today's senior judgment and the apprenticeship that would have produced tomorrow's. The dashboards look better than ever, right up until the system needs a human who understands it and there is no longer one in the room.

## The room I keep coming back to

Before I spent fifteen years building enterprise products, I trained as a physician, and there is one room in the hospital that settles this whole argument for me.

The intensive care unit is the most automated environment in the building. Ventilators breathe for patients. Pumps titrate fluids and drugs automatically. Monitors track every vital sign continuously and alarm on their own. Sepsis-prediction models flag deterioration before a human would. By the measure of how much the machines do on their own, the ICU should need the fewest people in the building.

It has the most. The highest staff-to-patient ratio in the building sits in the room with the most automation, and it is not just the densest staffing, it is the most senior. ICU nurses and intensivists are among the most experienced and most heavily certified people in the hospital. That is not an accident. When a patient on all that automation starts to crash, the machines do not fix it. The judgment in the room does, and only deep judgment is fast enough to catch what is going wrong and decide what to do about it before it is too late. You staff for the bad night, not the good one.

Nobody walks into an ICU, sees the machines doing the work, and concludes the nurses can go home. The ratio is high, and the people are senior, *because* of what the machines are doing, not despite it. The more a system acts on its own in a place where being wrong is irreversible, the more supervision it earns, and the more experienced that supervision has to be.

That is the exact inverse of the reorganization logic running through the industry right now. The pod sees AI automate the work and concludes: cut the team. The ICU, the one place humanity has the deepest experience with autonomous systems making consequential decisions, did the opposite, and it did it for a reason. Automation does not remove the human. It changes the human's job from doing the task to watching the thing that does, and that job gets bigger, and needs more experience behind it, as the stakes and the autonomy rise.

## The distinction is the point

I am not arguing against the AI pod. It is the right structure for building conventional products faster, and for the lower rungs of the ladder, and most teams should adopt some version of it. I am arguing that the industry has one well-funded, well-named answer for how AI changes the team, and it answers only the part of the ladder we already knew how to govern. It optimizes the building of the thing and says almost nothing about supervising the thing once it acts.

So before your team reorganizes around AI, it is worth asking which of the two things you are building, conventional products faster, or products that act on their own, and which rung you are on today versus the rung you will be on in a year. The team that is right for where you are can be exactly wrong for where you are heading, and the gap does not show up on the dashboard. It shows up in the incident.

Here is the version of the question that I think actually decides it. It is Friday night. An agentic product that has been running fine for months is now doing something wrong in production, quietly and at scale. Customers are angry, systems are down, and the dashboards that looked green all quarter are no help, because the failure is in the judgment, not the uptime. Who do you want on that call? You want the most experienced person you have, the one with the judgment to see what is actually happening and the standing to stop it. That is the ICU answer. The lean pod, optimized for the good night, is the org chart that cut that person two quarters ago because the agent made them look optional.

That second team, the one the agentic product forces into being, the seats it needs, the seams where it fails, and who owns what when the software acts on its own, is the subject of my next book, *The Agentic AI Team*.

The short version is the one I will leave you with. Every team knows how to build the agent. The team that knows how to supervise it, and the experienced people you will want in the room on the bad night, do not exist on most org charts yet. And the architecture that does not exist yet is not a person. It is a team.
