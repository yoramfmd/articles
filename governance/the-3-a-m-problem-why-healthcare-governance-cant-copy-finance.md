# The 3 a.m. Problem: Why Healthcare Governance Can't Copy Finance

I was a young intern in anesthesiology when I first encountered the disconnect between how governance is supposed to work and how it actually needs to work in healthcare.

On a Tuesday morning in March, I was preparing for what was supposed to be an uncomplicated bowel resection alongside an experienced attending anesthesiologist. Cancer removal. Young patient. We attached all the tubes and wires. We got ready for the surgical team. Everything was going according to plan.

Then, about an hour into the surgery, one of the surgeons said something you never want to hear: "Oops."

A major artery had been accidentally cut. What seemed like a smooth flight had become an emergency. We were monitoring the situation on our side, but as time passed, volume depletion increased and the patient became unstable. This was not an anticipated event. We had no ready-to-use blood in the room.

My attending looked at me and said: "Get blood. Now."

I ran to the nearest computer. The hospital had just implemented a new blood bank system built on SAP's ERP platform by a software partner, specifically designed with governance in mind. Blood products are dangerous. Giving the wrong blood type kills a patient. So the system required multiple checkboxes, signature steps, validation points. Each step necessary. Each step protecting against a real risk.

I had to log in with a different username and password than the one I used for the patient file, since that was considered more secure. Then the system presented me with a multi-step wizard, filled with options, buttons and lists of values. Step one. Step two. Step three. Step four.

By step four, the patient was crashing.

My attending looked at me and made a decision. He said: "Take the patient label. Run to the blood bank."

I dropped the mouse and ran. I told the blood bank staff we have a patient crashing on the bed. They handed me two units immediately. I ran back upstairs. The patient survived.

The system had done its job perfectly. It had enforced governance. It had created audit trails. It had protected against the wrong blood type being given to the wrong patient. But it had not accounted for the moment when governance itself becomes the problem.

Here's what the product manager who designed that system probably didn't know: he was modeling healthcare after banking.

The PM was probably envisioning a physician sitting in an air-conditioned office, unhurried, spending time filling out forms. Clicking checkboxes. Verifying details. Taking their time to get it right. This is how banking works. A customer sits down. A banker takes their information. Forms get filled. Approvals flow through. Everyone has time.

In banking, the world is relatively stable. A transaction follows a known path. A customer initiates a request. The system validates it. The system approves it. The system executes it. Variability is a problem. You want the same process, applied the same way, every time. That's how you prevent fraud. That's how you ensure compliance.

In healthcare at three a.m., there is no known path. A patient arrives in the ED in septic shock. A woman in labor develops complications. A child has an allergic reaction. A patient's heart rate suddenly drops during routine surgery. These events don't follow a process. They demand immediate action in conditions of radical uncertainty.

The product manager probably never spent time in a hospital ED or an operating room. He designed the system around an imaginary scenario that doesn't actually exist.

To be clear: this is not SAP's fault. I spent most of my professional life as a product manager and strategist at SAP. I know that SAP's ERP platform is brilliant at what it does. It runs complex business processes for the world's largest companies. It handles governance, auditability, and compliance better than almost any enterprise software platform. The problem wasn't the platform. The problem was how a software partner chose to implement it in healthcare by building rigid governance into the UI itself, creating workflows that were better suited for banking than for clinical emergencies. They didn't understand that healthcare doesn't work like a bank or a manufacturing plant.

Healthcare is full of moments where the textbook governance doesn't fit the moment.

A trauma patient arrives with a penetrating chest wound. The ED physician doesn't have time to verify insurance, confirm allergies, or complete a full history. He needs to act. The governance that protects against medication errors in a stable patient becomes a liability when the patient will die without immediate intervention.

A woman in active labor develops signs of fetal distress. The obstetrician needs to make a decision about emergency delivery in seconds, not minutes. The normal approval workflows for surgical intervention don't fit the moment.

A patient in the ICU has a severe allergic reaction. The critical care team needs to administer epinephrine immediately. They don't have time to wait for pharmacy verification or second signatures.

In each of these moments, hospitals have learned over decades to relax certain guardrails. Not because governance doesn't matter. But because the risk of following the normal process is greater than the risk of deviating from it.

A financial institution never faces this calculus. A banking transaction can be delayed. A customer can wait. The cost of caution is low. In healthcare, the cost of caution can be death.

The problem is that healthcare AI governance is being built by people trained to think like bankers, not clinicians.

They want to identify best practices and enforce them uniformly. They want to remove variability. They want to design systems that work the same way in calm and in chaos. They don't understand that the right governance in a scheduled surgery is not the right governance in an emergency.

This is dangerous because it creates a false choice: follow the system or break the rules. A clinician in the blood bank situation had to choose between waiting for the system to approve blood products and getting blood to a crashing patient. There was no middle ground.

The blood bank system wasn't designed to accommodate emergency scenarios because its architects didn't think in emergency scenarios. They thought in transactions. Standardized, repeatable, verifiable transactions. Like a bank transfer. Like a purchase order.

But healthcare is not a series of transactions. It's a series of crises of varying severity, punctuated by periods of routine. What works at one p.m. does not work at three a.m. What is appropriate governance for a scheduled surgery is not appropriate governance for hemorrhagic shock.

Good healthcare governance has always understood this. Trauma protocols include explicit procedures for bypassing normal approval chains. ICU teams have standing orders for life-saving interventions that don't wait for standard verification. Operating rooms have emergency procedures that suspend certain safeguards when the alternative is worse.

But these exist because clinicians designed them. They understand that governance should scale with risk, not with process.

Healthcare AI systems need to build this in from the start. Not as an override button people press when frustrated. But as a fundamental principle: governance should be context-aware.

What healthcare needs is **adaptive governance**: governance that enforces rigor without sacrificing responsiveness. A routine lab order goes through standard validation. An emergency lab order during a code blue goes through expedited validation, with different criteria. A scheduled medication order requires standard approvals. A medication for respiratory distress goes through a fast-track workflow. A blood product for hemorrhagic shock can be accessed with minimal delay, because the risk of delay is greater than the risk of the process being slightly less rigorous.

When someone deviates from governance in an emergency, the system captures why. Not to punish them, but to learn. The first time someone bypasses a step might be an error. The hundredth time in the same scenario is a signal that the governance is wrong.

Adaptive governance means:

- Context-aware rules that shift based on clinical acuity
- Structured override rights, not hidden workarounds
- Audit trails that capture not just what happened, but why
- Learning loops that improve the system when it fails in emergencies

This is sophisticated governance. It's harder to design than static rules. It requires clinicians in the room from the beginning. But it's the only kind that will actually work in healthcare.

The blood bank system wasn't wrong. It was incomplete. It enforced safety without modeling urgency. Healthcare AI governance must do both.

My attending anesthesiologist made the right call by overriding the system. But he only could because he had the authority. Many clinicians don't. And when AI systems don't have emergency modes built in, clinicians won't be able to override them at all. They'll either ignore the system entirely or follow it into tragedy.

Healthcare AI governance will fail if it's designed by people who've never been in an operating room at three a.m. It will fail if it enforces the same governance protocol in all circumstances. It will fail if it removes the clinician's ability to recognize context and adapt.

But if we build adaptive governance into the architecture from the start, we can have systems that are both safe and fast. Systems that clinicians can trust. Systems that actually work when mostly needed.

That's the lesson from the blood bank. That's what healthcare AI needs to learn.
