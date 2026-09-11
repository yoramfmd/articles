---
title: Tesla Removed the Steering Wheel. That Was the Honest Part.
slug: tesla-removed-the-steering-wheel-that-was-the-honest-part
published: 2026-08-07
excerpt: A Cybercab was filmed with no steering wheel. Removing it was the honest part. The rungs below it, hands on the wheel, eyes on the road, ready to take over, were never supervision. They were accountability. Most enterprise AI is still on rung three.
url: https://data-decisions-and-clinics.com/tesla-removed-the-steering-wheel-that-was-the-honest-part/
tags: Agentic AI, Product Management
source: ghost-api-pull-2026-08-16
---

There is a bag hanging on every anesthesia machine.

It has been there my whole career and it was there long before that. The machine ventilates better than a person with a bag and a watch, more consistently, hour after hour, and by any reasonable measure the automation won that argument decades ago. Nobody took the bag out of the room.

The circuit still disconnects. The reservoir is still reachable. The reason is not sentiment. The specialty decided that the anesthesiologist has to remain physically able to do the thing the machine is doing, and has to stay in the room while it does it. The affordance was preserved deliberately, and so was the skill.

I thought about that bag last week, looking at photographs of a car with no steering wheel.

### Five Rungs, and I Could Recite Them

A Cybercab was filmed on a residential street in west Los Angeles at the start of August. Two seats, no wheel, three hundred miles of projected range, a target price under thirty thousand dollars. No rollout timeline published.

What struck me was not the car. It was that I could recite the whole sequence that got us here without looking anything up, because I have watched the same sequence run inside enterprise software for twenty years.

Drive the car.

Keep your hands on the wheel while the car drives.

Watch the road while the car drives.

Be ready to take over if something goes wrong.

Sit back. You are a passenger.

That is the autonomy ladder, and this is the first time most people will see the top rung in a photograph. Every rung was justified by the safety record of the rung below it. That is the part worth arguing about, because each of those records was a record of the machine, and the question each rung was actually answering was about the human.

### Nobody Measured the Middle

At no point in that sequence did anyone establish that the person on rung two, three, or four was doing anything.

Hands on the wheel is not supervision. It is a hand on a wheel. The system can detect torque on the rim. It cannot detect whether you are looking at the road, holding a model of what the car is about to do, or capable of forming an intention fast enough to act on it.

Watching the road while a competent system drives is worse, not better, because human vigilance under low event rates degrades on a schedule that has been documented since the nineteen forties. And "be ready to take over if something goes wrong" asks a person who has not driven for forty minutes to outperform, in about a second and a half, a system that has been driving continuously and has more sensors than they do.

Those three rungs were never supervision states. They were accountability states. The wheel was there so that when it failed, a person had been in a position to prevent it.

Which is why taking it out is the honest move. A steering wheel nobody is expected to use, in a car nobody is expected to watch, answers a liability question rather than a safety one. Remove it and the real question becomes unavoidable. Whose failure is this now?

### An Affordance and a Prop Are Different Things

That is the distinction the autonomy ladder erases.

An affordance is a control the operator is expected, and periodically required, to use. A prop is a control that exists so somebody can be said to have had the option.

Aviation understands this and enforces it. Pilots demonstrate manual proficiency on a schedule, which is the only reason "the pilot can always take over" means anything at all. Anesthesia understands it, which is why the bag is still hanging there and why you are expected to know how to use it. A control with no practice requirement attached is a prop, and it will not save you.

Ask which one you shipped. Most of us have shipped props.

### I Have Shipped the Enterprise Version

Twenty years of product management across enterprise platforms and regulated health tech, and I have put a confirmation step in front of an automated action more times than I can count.

Some of those were real. A person read the thing, understood it, and sometimes said no.

Plenty were not. The step existed because the risk review needed a human in the flow, and the fastest way to get a human in the flow is to add a dialog. Nobody asked what the person would need to know to answer well, whether they would have that at the moment of asking, or how long a considered answer takes against the rate at which the dialogs arrive. We shipped the affordance. We did not ship the conditions that make it mean anything.

The enterprise ladder is running right now with the same five rungs. The analyst does the work. The analyst does the work with a suggestion panel open. The analyst reviews what the system produced. The analyst gets pinged only on exceptions. The analyst is removed, and the removal is justified by an approval rate that was ninety-eight percent for eighteen months.

That ninety-eight percent is a record of the system. It is being read as a record of the human and it is not one. A person approving ninety-eight percent of items may be exercising excellent judgment on a system that is right ninety-eight percent of the time, or may be clicking. The log looks identical. That is not a data gap you can close later. It is a measurement nobody designed, and the removal decision is being made on its absence.

### The Test That Separates Two Cases

Let me be careful, because the reflexive position, that removing the human is always wrong, is not one I hold.

Sometimes the human should come out. If the loop was already empty, keeping a person in it is worse than removing them. It costs money, it slows the system, and it manufactures a false assurance that someone is watching. Radiology is walking into this directly. The UK is looking hard at autonomous reporting of normal chest films, a European conformity mark for it already exists, and the radiologist shortfall is real. There is a defensible version of that decision.

So the question is not whether to take the human out. It is which of two situations you are in, and they sound identical in a steering committee.

The first is that the loop was already empty. Removing the person removes a cost and a fiction. This is the honest case, and you can only claim it if you can produce evidence the human was not contributing. Override rate over time. Time spent per item against the time a considered review would take. Disagreement rate on a seeded sample where you already know the answer. If those show a reviewer who stopped functioning eleven months ago, take them out and say so plainly.

The second is that the human was contributing and you are removing them to save money. That is also a legitimate business decision, and it is a different one, because it converts a caught error into a shipped error at some rate you now own. The test is whether you can state that rate.

Force the distinction, because the second case is almost always presented as the first. Nobody stands up and says the reviewer was catching things and we are accepting those failures now. They say the system has matured. Both sentences are compatible with the same approval log, which is exactly why the log cannot settle it.

And one more thing disappears when the human comes out, which I think is the most underrated part. Remove the reader and you lose the discrepancy audit. The human was not only catching errors. The human was how you found out the system had drifted. Take them out and you need a new drift detector, budgeted and built, or you have removed your instrument at the same moment you increased your exposure.

### Three Questions Before You Climb

What evidence do we have that the human at the current rung is doing anything? Not that they are present. That they are functioning.

If we remove them, what detects drift afterward, and who owns it?

And is the control we are leaving behind an affordance or a prop? If nobody is ever required to exercise it, and no practice keeps anyone able to, it is a prop.

Tesla answered the third question by taking the wheel out. Whatever else you think of that car, it is a clearer statement than a wheel nobody touches.

Most enterprise AI is still on rung three, holding the wheel, calling it oversight, and getting ready to cite the safety record as the reason to let go. The record is real.

It is just not a record of you.

---

*References: The Cybercab sighting in west Los Angeles, August 2026, reported by Yahoo Autos. Nash, Vaz, Malter and colleagues, "Autonomous Reporting of 'Normal' Chest X-rays by Artificial Intelligence in the United Kingdom; Can We Take the Human Out of the Loop?", BJR Artificial Intelligence, 2026, open access.*
