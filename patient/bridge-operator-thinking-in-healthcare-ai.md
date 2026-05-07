# The 60-Point Gap: Why We're Measuring the Wrong Customer

## The 60-Point Failure

A study published in Nature in early 2026 tested large language models on medical triage scenarios. The headlines focused on the accuracy gap: 94.9% when evaluated against medical licensing exam questions, 34.5% when tested with real people.

That's a 60-point collapse. Same model. Same task. Different conditions.

Most people read that and conclude: benchmarks don't predict real-world performance. True. But the gap points to something deeper. It reveals a layer of the problem we haven't solved yet: interaction design. How do we deploy general-purpose LLMs into healthcare contexts where actual panicked people, not calm researchers, interact with them?

I realized this while reading the study's methodology. Then I thought about my son when he was three years old. Three in the morning. 103-degree fever. Screaming. My husband and I both awake, panicked, no pediatrician on call, wondering if we should go to the ER or wait until morning. That's not a scenario a physician would create for a test. That's terror and sleep deprivation and fragments of information assembled under maximum cognitive load.

That's the gap the Nature study didn't measure.

## What the Study Actually Tested

The Nature researchers did something important: they tested real members of the public using LLMs on everyday medical scenarios. Three physicians created ten vignettes framed as at-home situations. Then they recruited 1,298 lay participants from the UK. Each person was given two scenarios and asked to decide on a disposition and list relevant conditions.

The answer: 34.5% of the time. No better than controls. Sometimes worse.

And this is from calm, focused people sitting in front of laptops, not experiencing any real pain or distress. Not a parent at 3am with a screaming child. Not someone experiencing chest pain and terror. Not a person in actual crisis.

But here's what the study still doesn't capture: it operates on scripted vignettes, not on raw, panicked self-reporting. The information is complete. The scenarios are readable. A real person at 3am, sleep-deprived and terrified, doesn't describe their symptoms that way. They fragment. They omit. They ask the wrong questions because they don't know what questions to ask.

The study's own transcript analysis shows exactly this problem: users frequently don't provide enough information; models mention multiple conditions and users fail to pick up the relevant one; models give inconsistent answers; people don't know what follow-up questions to ask. These are the failures that happen when you put a generic LLM in a chat box and let an untrained person try to get medical triage guidance.

## What the Interaction Failure Reveals

I've spent two decades in product management thinking about how that role is changing. The shift has a name: from bridge operator to bridge architect.

A bridge operator facilitates between two existing sides. They connect users to information. They assume the two sides already exist and just need connecting.

Bridge architect thinking is different. You design the decision system itself. You start with the actual end customer, a panicked parent at 3am, a person experiencing chest pain, someone without medical training under time pressure, unable to provide complete information, and you design backward from there.

The Nature study reveals what happens when you apply bridge operator thinking to a general-purpose LLM in a healthcare context. Someone deploys a tool. Tests it with curated scenarios. Ships it. Then real people try to use it for triage, and the system fails because it was never designed for that interaction.

The paper shows this explicitly: users provide incomplete information; models mention relevant conditions but users don't act on them; there's no scaffolding to extract what's actually needed. The authors themselves call for "moving toward increasingly realistic conditions" and systematic human user testing before deployment.

That diagnosis is sound. But it points toward a design philosophy problem. The system has two conflicting customers. Customer one: the benchmark, optimized for accuracy on structured medical questions. Customer two: the panicked person at 3am, wanting guidance they can understand. The benchmark wants structured input. The panicked person provides fragmented input.

When you optimize for one (which general-purpose LLMs naturally do), you fail the other (which is what the study showed).

## The Training Data Gap

LLMs trained on documented clinical cases can't answer questions at the moment those cases were undocumented.

A patient arrives at an ER in septic shock. That moment, the decision to triage, is not well documented. Most of the clinical story happened before: the phone call to 911, the field assessment, the vital signs measured by the paramedic. The model learned from the documented end of the story. It's being deployed at the undocumented beginning.

The Nature study's transcript analysis reveals what happens when untrained people use LLMs for triage. The LLM answers what it's asked, but it doesn't push back. It doesn't ask: "Tell me more about the chest pain. When did it start? Are you short of breath?" It doesn't say "I need more information to give you reliable guidance."

That's a design failure. The interaction is essentially a generic chat box. No structured triage flow. No mandatory follow-up questions. No escalation pathways. Just a space where someone types and hopes the right information emerges. Nobody architected the interaction for the user who doesn't know how to ask medical questions.

## What Bridge Architect Thinking Looks Like

If you start with the actual end customer, the panicked person at 3am, and design backward, everything changes.

You start with: "Given that this person is panicked, sleep-deprived, unable to articulate their symptoms clearly, without medical training, and under time pressure, how do we design a system that gets them to the right care?"

I learned this viscerally years ago in a hospital during an emergency. A perfectly designed blood bank system. Multiple checkboxes. Validation points. Each step protecting against a real risk. Then a patient started crashing on the operating table. I had to log in with a different username and password, click through a multi-step wizard, step four, step five. By step four the patient was dying. My attending looked at me and said "take the patient label, run to the blood bank." I dropped the mouse and ran. The system was designed by someone who had never been in an operating room at 3am. It enforced perfect governance but forgot about the customer who needed the blood in the next ninety seconds.

The answer isn't just a better model. It's a compound system: model plus interface plus interaction design plus human escalation plus governance. Each component serves the customer, not the benchmark.

It means building in user guidance ("Tell me more about..."). It means the AI flags uncertainty and suggests talking to a real clinician. It means refusing to provide triage guidance and routing to nurse triage lines instead. It means measuring outcomes: did the person get to the right care pathway.

None of that is happening because most healthcare AI products were designed with bridge operator thinking.

## What the Study Reveals (And What's Still Missing)

The Nature study is valuable. It moves beyond benchmarks and shows what happens when real people try to use LLMs for medical guidance. The 60-point gap is data we didn't have before.

But the study operates at one layer of the problem. It answers: "If we give untrained people a chat interface and an LLM, can they get reliable triage guidance?" Answer: not reliably.

The deeper question is: "How do we design a system where untrained people in distress can reliably get guidance?" That requires more than testing. It requires designing.

The Nature study didn't explore structured interaction patterns (mandatory symptom elicitation, explicit uncertainty statements, escalation pathways). It didn't measure outcomes at all. It tested model-plus-chat-box in isolation, not model-plus-designed-interaction-plus-governance as a compound system.

## The Implication

Nobody gets promoted for building a system where the panicked end user is the primary customer, not the benchmark. So we keep deploying general-purpose LLMs into healthcare contexts and waiting to see what fails.

Bridge architect thinking means starting with the end customer, the panicked person at 3am with a screaming child with fever, unsure if they should go to the hospital, and designing backward. It means accepting that a general-purpose chat interface is insufficient for triage. It means building interaction patterns, escalation pathways, and governance before deployment, not after.

Most healthcare AI deployments are still bridge operator thinking in a bridge architect world. Until that changes, we'll keep getting the Nature study results: brilliant models that fail when they meet actual panicked people trying to decide if something is serious enough to act on.

The study didn't prove LLMs are bad at triage. It revealed that deploying them without architectural scaffolding puts the burden on the user to provide perfect information when they're terrified.

That's a design problem, not a model problem. Which means it's a harder problem to fix than improving the model. But it's the only thing that actually matters when someone at 3am is wondering if they should take their child to the hospital.

---

**Reference:** Bean AM et al., "Reliability of LLMs as medical assistants for the general public: a randomized preregistered study," *Nature Medicine*, Volume 32, published online January 2026, pp. 609-615. DOI: https://doi.org/10.1038/s41591-025-04074-y
