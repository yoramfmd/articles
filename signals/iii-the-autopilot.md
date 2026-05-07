---
title: The Autopilot
slug: iii-the-autopilot
published: 2026-01-03
excerpt: In 2013, the FDA approved a machine that could sedate patients without an anesthesiologist. By 2016, it was dead. No safety scandal. No patient harm. It simply failed to sell.
---

*From cockpit instruments to closed-loop control*

In May 2013, after years of regulatory struggle, the FDA granted premarket approval to a device called Sedasys. Built by Johnson & Johnson's Ethicon division, it was a computerized system that administered propofol for colonoscopy sedation, monitored vitals, and adjusted dosing automatically. Routine sedation for routine procedures, managed by a machine. No anesthesiologist required.

Less than three years later, J&J pulled it from the market. Sales had been dismal. The American Society of Anesthesiologists had fought the device from the start. The reimbursement model never supported it. And the restrictive FDA labeling, which limited the device to the healthiest patients undergoing the simplest procedures, shrank the addressable market to almost nothing.

Sedasys became healthcare's exhibit A against automation. *You can't automate clinical judgment,* the critics said. *The system was too rigid. The doctors pushed back. The market said no.*

They were right about all of that. And they were wrong about what it meant.

Sedasys didn't fail because automation in anesthesia is impossible. It failed because it was the wrong architecture at the wrong time, sold with the wrong positioning to the wrong stakeholders. A rule-based system trying to navigate a problem that demanded adaptiveness. A product marketed as a replacement for the physician, which guaranteed political resistance. And a reimbursement landscape with no code, no pathway, and no incentive to accommodate it.

The story of AI in anesthesia didn't end with Sedasys. It barely began there.

I came to anesthesiology by an unusual route. After medical school I trained in radiology, the specialty I wrote about in the first article of this series. But something in me wanted to be closer to the machine, not the image. So I left clinical medicine and spent eight years in technology, first at Microsoft, then at SAP, working as a product manager, building products, leading global teams, learning what digital transformation actually means when you're the one shipping the software.

People asked me constantly: *Don't you miss being a physician?* For a long time the honest answer was no. Then, gradually, it was yes. I chose the residency that fit me best: anesthesiology and intensive care.

Many clinicians won't understand the choice in these terms, but for me anesthesiology was the most technology-dense specialty in medicine. Fast, intensive, patient responses measured in seconds. The operating room is a real-time system. Every patient is instrumented with sensors, every physiological variable is digitized and streaming, feedback loops are immediate. It's the Internet of Things, except the sensors are attached to real people and lives are at stake. For someone with my background, it was the most exciting clinical environment imaginable, with the one caveat that you need to master physiology and pharmacology to survive in it.

That dual perspective, clinician and product manager, is why I see the Sedasys story differently from most physicians. When an anesthesiologist looks at Sedasys, they see a threat vanquished. When a product manager looks at Sedasys, they see a go-to-market failure that taught the industry exactly what not to do. Both readings are correct. But the second is the one that matters for what comes next

To understand anesthesia, forget the popular image of someone counting backward from ten. That's the first thirty seconds. The other three hours are the job.

I describe it this way: anesthesiology is very much like flying a plane. You start by thoroughly checking the patient and the equipment. You attach the lines and electrodes, make sure everything is connected. Then you induce anesthesia, put the patient to sleep, and from that point on you're running on autopilot, trying to keep the patient stable while the surgical team acts like a group of hijackers trying to crash the plane.

I say that with affection, but also with precision. The surgeon opens the abdomen and blood pressure drops. The orthopedist reams a femur and fat emboli hit the lungs. Every surgical maneuver is a physiological insult, and the anesthesiologist's job is to absorb it, compensate, and keep hemodynamics within a livable range. At the end, you wake the patient up and hopefully return them to the state where they started.

The cognitive load is enormous. Monitors everywhere, visual and auditory signals, devices demanding real-time response. And since nearly everything in that environment is already digitized, it is the perfect setting for automation and AI.

The aviation analogy isn't marketing. It is the literal engineering lineage of the specialty. And it turns out to be the best framework for understanding where AI in anesthesia is heading.

In the early 1970s, a team at Massachusetts General Hospital led by Jeffrey Cooper built the Boston Anesthesia System, a prototype that was, by the standards of the time, radical. It was the first anesthesia machine designed using human-factors principles borrowed directly from aviation cockpit design, and the first to incorporate computer-based operations. It integrated multiple physiological data streams into a single display, automated gas flow calculations, and included programmable alarms with adjustable thresholds. It won a scientific exhibit award at the ASA annual meeting in 1976 and, though never commercially produced, established the conceptual template for every anesthesia workstation that followed.

The parallel to aviation was explicit and deliberate. By the 1970s, the aviation industry had already learned a painful lesson: cockpits filled with disconnected gauges and incompatible displays overwhelmed pilots and caused fatal errors. The response was the "glass cockpit," an integrated information environment that consolidated critical data into a coherent visual hierarchy. Cooper's team applied the same logic to the operating room. The result, a workstation that organized physiology the way a flight deck organizes flight parameters, became the ancestor of every modern anesthesia machine.

But there's a deeper parallel that matters more, and it's the one that explains where AI in anesthesia is actually going. It isn't about a single product or a single algorithm. It's about a design philosophy that aviation worked out decades ago and that anesthesia is now recapitulating.

Airbus calls it fly-by-wire.

Modern Airbus aircraft don't give the pilot direct mechanical control of the flight surfaces. Instead, the pilot's inputs pass through a computer that interprets them within a framework of control laws: Normal Law, with full envelope protection; Alternate Law, with partial protections; and Direct Law, with minimal automation. In Normal Law, the default, the computer will not allow the aircraft to stall, overspeed, or exceed safe bank angles, no matter what the pilot does with the stick. The system enforces safe limits even if pilot input exceeds them.

The pilot is never removed. Automation changes modes, but authority remains clearly structured. The pilot can override. The pilot can disengage. The system operates within boundaries defined by humans.

This is not full autonomy. It is layered autonomy, and the distinction matters enormously.

Anesthesia, without anyone using the Airbus terminology, has been building toward the same architecture for decades. And the Sedasys failure makes much more sense through this lens. Sedasys tried to skip the layered approach entirely. It went straight from manual control to something close to full automation, removing the anesthesiologist from the loop rather than restructuring the physician's role within it. In Airbus terms, Sedasys tried to jump from Direct Law to a fully autonomous flight, skipping Normal Law and Alternate Law entirely. No wonder it crashed.

What has actually been developing in anesthesia, step by step, is a fly-by-wire architecture. And each layer maps cleanly to the Airbus model.

**Layer one: envelope protection.**

In an Airbus, envelope protection means the aircraft will not allow the pilot to exceed safe physical limits. The plane won't stall. It won't overspeed. It won't roll past a certain angle.

In 1994, Aspect Medical Systems introduced the Bispectral Index monitor, BIS, and it represented the first step toward something analogous in anesthesia: physiological envelope protection.

Before BIS, "how asleep is this patient?" was answered by clinical judgment: heart rate, blood pressure, movement, tears. These were indirect, unreliable clues. A patient could be dangerously light under anesthesia and show no cardiovascular signs until they woke up on the table, paralyzed and in pain.

BIS placed a sensor on the patient's forehead, captured the brain's raw electrical activity, processed it through an algorithm, and reduced that complex signal to a single number from 0 to 100. Between 40 and 60 meant appropriate surgical anesthesia. Above 60, too light. Below 40, too deep. The FDA cleared it in 1996, and by 2003 the agency recognized its potential to reduce intraoperative awareness.

BIS was, in essence, a sedation depth guardrail. Not a hard boundary like an Airbus envelope, because human physiology is probabilistic and noisy rather than deterministic and physics-based. But the principle was the same: give the operator a clear, continuous signal that indicates when the system is approaching its safe limits.

For builders and product managers, BIS is worth studying for a reason that transcends neuroscience. It succeeded because it reduced an impossibly complex signal to one actionable number. Not a waveform. Not a panel of values. One number, on one screen, updated in real time. Simplicity of output, not sophistication of algorithm, drove adoption. This is a principle that recurs across every successful clinical AI product: the value is proportional to the clarity of what it communicates, not the complexity of what it computes.

BIS established the sensor. What was still missing was the system that would take the reading and act on it.

**Layer two: predictive alerting.**

In aviation, the next step beyond envelope protection is predictive warning. The aircraft doesn't just prevent you from exceeding limits; it tells you when you're trending toward them. Ground proximity warnings, wind shear alerts, traffic collision avoidance: systems that watch the trajectory and flag danger before it arrives.

Edwards Lifesciences' Hypotension Prediction Index, or HPI, brought this concept to the operating room. Intraoperative hypotension, a sustained drop in blood pressure below safe thresholds, is common and consequential. Even brief episodes are associated with increased risk of heart attack, kidney injury, and death. For the anesthesiologist, managing blood pressure is constant work, but by the time the number on the monitor drops, the event is already underway. You're always reacting.

HPI changed the timing. The software analyzes the shape of the arterial blood pressure waveform using a machine learning model trained on thousands of patients. It generates an index from 0 to 100 that estimates the likelihood of a hypotensive episode within the next fifteen minutes. It doesn't tell you what to do. It tells you what's about to happen and gives you time to prevent it.

The clinical experience is transformative. Instead of watching blood pressure drop and scrambling, you see the index climbing and make a calm, proactive decision: give fluids, start a vasopressor, adjust anesthetic depth. You're ahead of the physiology instead of behind it.

Note what HPI does not do. It doesn't administer fluid. It doesn't start the vasopressor. It doesn't touch the patient. It predicts and displays. The physician decides and acts. In Airbus terms, this is a caution alert on the primary flight display. The automation is watching the trajectory, the pilot is flying the plane. That's why HPI got adopted without the firestorm that consumed Sedasys.

But the gap between prediction and action was always going to close.

**Layer three: assisted control.**

In an Airbus, autopilot handles cruise stability, fuel optimization, and navigation precision. The pilot sets the parameters, the system executes, and the pilot can disengage at any moment.

Target-controlled infusion, or TCI, has been the anesthesia equivalent for decades, though it has never received regulatory approval in the United States. Instead of manually setting a drug infusion rate, the anesthesiologist sets a target concentration in the blood or brain. A computer continuously adjusts the infusion rate using pharmacokinetic models calibrated for the patient's age, weight, and other factors. The machine handles the math. The human handles the judgment.

TCI is technically open-loop: the computer adjusts based on its model but doesn't receive direct feedback about actual drug effect. The anesthesiologist closes the loop manually by watching the patient.

True closed-loop systems connect the output back to the input. The sensor is BIS or a similar monitor. The actuator is the infusion pump. The controller is an algorithm that reads one and adjusts the other. These systems have been tested in thousands of patients across dozens of studies. The results are consistent: more precise depth control than manual titration, less total drug used, less variability between practitioners, no compromise in safety. A three-drug closed-loop system has been approved in China. None is commercially available in the United States yet.

The crucial point for the anesthesiologist: closed-loop anesthesia is closer to autopilot than to a self-flying plane. Manual override is always available. The system operates within boundaries the physician defines. It doesn't remove the pilot from the cockpit. It removes the tedium from the flight.

**The common principle: cognitive offloading.**

Both domains face the same fundamental problem. An Airbus cockpit streams thousands of parameters. An operating room streams hundreds. The human operator is overwhelmed with data. The solution is not to remove the human but to distribute the load between human and machine, each doing what they do best.

In aviation, autopilot handles cruise stability and navigation. The pilot focuses on judgment, abnormal events, and situational awareness. In the OR, AI handles pattern recognition, sedation depth, ventilator optimization. The clinician focuses on interpretation, context, and patient-specific nuance.

This is augmentation, not automation. And it is an engineering principle with fifty years of evidence behind it.

The best anesthesiologists I trained with weren't the fastest at pushing drugs. They were the most aware. They saw things developing before anyone else in the room, not because they watched more monitors, but because they had the cognitive bandwidth to think. Anything that handles the mechanical routine, the titration, the ventilator adjustments, the fluid calculations, creates more of that bandwidth. It doesn't replace judgment. It creates the conditions for judgment to operate at its highest level.

**The honest difference.**

Intellectual honesty requires naming it. Airbus envelope protections are deterministic and physics-based. An aircraft's stall speed at a given weight is a known quantity. The boundaries are hard.

Human physiology is probabilistic and noisy. Two patients of identical age and weight may respond to the same drug dose in dramatically different ways. Genetic variation, organ function, concurrent medications, a hundred variables interact in ways no model fully predicts. The envelope shifts from patient to patient and from minute to minute.

That uncertainty is where medicine becomes harder than aviation. It's why closed-loop systems require wider safety margins, more conservative algorithms, and an engaged human who can recognize when the model no longer fits the patient in front of them. It's also, at the technical level, why Sedasys failed. Its rigid rules couldn't handle patient variability. Modern closed-loop systems address this with machine learning models that adapt to the individual patient's responses in real time, learning how *this* patient behaves right now rather than assuming they'll behave like the average. That's the architectural difference between what failed in 2016 and what comes next.

**The next cockpit.**

Imagine the preoperative visit. Today, the anesthesiologist manually synthesizes a complex patient record into an anesthetic plan. Now imagine a system that ingests the same data, applies models trained on hundreds of thousands of cases, and generates a personalized flight plan: flagging pharmacogenomic risks, adjusting for cardiac history, recommending a tailored dosing strategy. The anesthesiologist reviews it, modifies it, proceeds.

During the case, closed-loop infusion maintains anesthetic depth. Predictive monitoring watches for hemodynamic instability. The ventilator auto-adjusts based on real-time lung compliance. The anesthesiologist oversees all of it, free to focus on the patient rather than the plumbing.

In Airbus terms: the flight management system has calculated the route. Autopilot is holding altitude. Envelope protection is active. And the pilot, unburdened from the mechanical work of flying, is scanning the horizon, ready to take manual control the instant the situation demands it

**The forward provocation.**

The next version of "AI in anesthesia is failing" will center on control. Critics will argue that closed-loop systems remove the human from life-critical decisions, that a software error could be catastrophic, that we're moving too fast.

The objection will ignore decades of precedent in both fields. Anesthesia has been automating gradually for its entire history. The ventilator replaced manual bagging. The pulse oximeter replaced the finger on the pulse. The infusion pump replaced drip counting. At each step, a task requiring constant attention was delegated to a machine, and the physician's role shifted toward higher-order oversight.

Aviation followed the same arc over a longer timeline. Manual flying gave way to autopilot, then autothrottle, then autoland. At each step, critics warned that automation would erode skills. They weren't entirely wrong; automation complacency is real. But the response wasn't to reject automation. It was to redesign training, mandate manual proficiency checks, and build clear authority hierarchies. The result: commercial aviation became the safest form of transportation in human history.

The same design principles apply. The risk isn't automation. It's automation without the right training, the right override protocols, and the right culture of vigilance.

Meanwhile, somewhere right now, an anesthesiologist is sitting at the head of an operating table. The surgeon is three hours into a complex case, and the blood pressure is starting to drift. Ten years ago, she would have noticed the drop after it happened and scrambled to correct it. Today, a predictive algorithm flagged the trend five minutes ago, and the fluids are already running. The patient never destabilized. The surgeon never knew.

She glances at the monitors, confirms stability, and turns her attention back to the surgical field. She's not watching numbers. She's watching for the moment the case stops being routine.

That's not a machine replacing a physician. That's a physician with a better cockpit.
