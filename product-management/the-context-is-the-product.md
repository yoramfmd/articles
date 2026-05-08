# The Context Is the Product

*In healthcare, AI can already predict. The hard problem is reasoning. And reasoning changes everything about who is valuable.*

---

In my previous piece, I argued that AI made prediction cheap and the value shifted to whoever owns the best data. A physician friend who read it sent me a message: "You are describing us. We have been sitting on the most valuable data in the world for thirty years and treating it as a billing problem."

He was right. And healthcare is where the argument gets most interesting, because in clinical settings, prediction was never the hardest problem. The hard problem is reasoning. And reasoning, it turns out, changes not just what data is valuable, but who is valuable.

---

### Prediction Is Already Table Stakes

The first wave of healthcare AI was built on prediction: sepsis risk scores, readmission models, imaging classifiers, deterioration alerts. Many of these work. The sepsis prediction model at your hospital is probably already running, alerting someone on a screen somewhere that a patient's risk score has crossed a threshold.

But here is what that model does not do. It does not tell you what to do about the seventy-three-year-old whose sepsis score is rising but who has a DNR, a history of difficult intravenous access, end-stage renal disease, and a daughter flying in from overseas who has not spoken to her father in two years and needs to be part of whatever conversation happens next. The model gave you a number. Everything that follows is reasoning: clinical, ethical, social, logistical. And that reasoning depends entirely on context that no algorithm generated.

This is the gap between what healthcare AI can do today and what the clinical encounter requires. Prediction tells you something is happening. Reasoning tells you what it means for this patient, in this moment, given everything you know about them. Those are not the same problem.

---

### From Prediction to Reasoning: The Economic Logic Extends

In 2018, economists Agrawal, Gans, and Goldfarb argued in "Prediction Machines" that AI is a dramatic drop in the cost of prediction, and that the value shifts to the complements: data, judgment, action. In 2022 they extended the argument in "Power and Prediction", moving from the economics of prediction to the economics of decision-making. Who defines the problem the AI reasons about? Who curates the inputs? Who is accountable for the output? In enterprise software, these are organizational questions. In healthcare, they are clinical, legal, and deeply personal.

The economic mechanism still holds: when a cognitive capability becomes cheap, the value shifts to whatever complements it. But in a reasoning world, the complement is not simply structured data. It is context: rich, complete, multi-modal clinical context that the AI can reason over accurately. The quality of the reasoning is bounded by the quality of the context. A reasoning system given incomplete or inaccurate clinical inputs will produce confident, well-articulated, wrong conclusions. The AI does not know what it does not know. The physician does.

The context is the product. And constructing it is a clinical skill.

---

### The Physician as Context Architect

Think about what a skilled physician does in a complex clinical encounter, before any AI is involved.

They take a history: not just the presenting complaint, but the timeline of symptoms the patient almost did not mention, the medication filled at a different pharmacy, the episode six weeks ago that seemed unrelated at the time. They perform a physical examination that surfaces findings no sensor has captured: the subtle change in mentation, the skin findings, the quality of breath sounds on the left base. They aggregate data from sources that were never designed to talk to each other: the structured EHR, the nursing notes written at three in the morning, the paper discharge summary faxed from the rehabilitation facility, the patient's own account of what changed and when.

All of that becomes the context on which reasoning operates. Feed a capable reasoning AI a thin, incomplete clinical picture and you get thin, incomplete clinical reasoning, expressed with the fluency and confidence of something that has read every medical textbook ever written. Feed it the complete, curated, multi-modal picture that a skilled physician constructs, and you get reasoning that reflects the actual complexity of the patient in front of you.

The physician, in this framing, is not being replaced by the AI. They are the person who makes the AI useful. They are the context architect.

Feed a reasoning AI a thin clinical picture and you get thin clinical reasoning, expressed with the confidence of something that has read every medical textbook ever written.

---

### The Skills We Deprioritized Are Now the Most Valuable

This has an uncomfortable implication for how medicine has evolved over the past thirty years.

The skills that become most valuable in an AI-reasoning world are the oldest ones. History-taking. Physical examination. The ability to synthesize across structured and unstructured sources and construct a coherent clinical picture from heterogeneous, sometimes contradictory information. These are the skills that were taught before imaging and laboratory medicine made pattern recognition the dominant clinical competency.

In a fee-for-service, high-throughput clinical environment, the physician who spent forty minutes with a patient taking a comprehensive history was inefficient. The system rewarded procedures, volume, and speed. History-taking was what you did while waiting for the scan. The physical examination became a billing requirement as much as a diagnostic act.

In a world where AI reasons over clinical context, that forty-minute conversation is not inefficiency. It is the construction of the epistemic foundation on which every downstream clinical decision rests. The physician who is best at eliciting the complete story, integrating the paper record, and contributing structured observations to the AI's reasoning layer is not practicing old medicine. They are practicing the most valuable medicine available.

---

### What This Means for Healthcare AI Products

If you are designing healthcare AI products and spending most of your time on the model, you have the same problem I described in my previous piece. The model will be a commodity. What will not be a commodity is the clinical context layer.

The healthcare AI products that create durable value will be the ones that make the physician's context-construction capability more powerful: the interface that helps structure and contribute clinical observations efficiently, the pipeline that aggregates the nursing home fax and the unstructured note alongside the structured EHR, the workflow that surfaces the right information at the right moment in the clinical encounter without adding documentation burden. These are hard, unglamorous product problems. They do not demo as well as a large language model generating a differential diagnosis. But they are where the actual clinical value lives.

The specification question from my previous piece applies here too. Before calling a clinical AI product an agent, you need to answer: which decisions does it make, under whose authority, what happens when it is wrong, and who is responsible for the context it received? In healthcare, that last question is not a product edge case. It is the clinical encounter itself.

In enterprise software, the data moat belongs to whoever accumulated the most operational records. In healthcare the moat is constructed fresh with every patient encounter, by a physician who knows how to ask the right questions, examine what matters, and aggregate what exists across paper and systems and the patient's own imperfect memory.

AI made reasoning cheap. The complement to cheap reasoning in a clinical setting is not a database. It is a physician who is expert at constructing the complete picture that reasoning requires. That skill is old, it is irreplaceable, and in an AI world it is more valuable than it has been in thirty years.

The doctor who listens carefully is no longer just being thorough. They are building the product.

---

*This piece is the second in a series. The first, "What Do We Do With the Frameworks?", makes the economic case for why the data layer matters more than the model layer in an AI-first world.*
