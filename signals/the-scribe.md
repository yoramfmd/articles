---
title: The Scribe
slug: the-scribe
published: 2026-01-06
excerpt: In the 1990s, a non-Jewish friend of mine wrote clinical notes for observant physicians who could not work on the Sabbath. Today, ambient AI does the same job. Who owns what the scribe writes?
url: https://data-decisions-and-clinics.ghost.io/the-scribe/
---

# The Scribe

My roommate had an unusual job.

We were medical students in Jerusalem in the late 1980s. He worked part-time at a religious hospital across the city, and the work he did there had nothing to do with his medical training. On Friday evenings, when the Jewish Sabbath began, he and other non-Jewish medical students would arrive at the hospital and stay until Saturday night. Their job was to write.

Observant physicians at that hospital were not permitted to write on the Sabbath. Religious law defined what constituted work, and writing was on the list. So when an observant physician needed to document a clinical encounter, my roommate was present. The physician spoke. My roommate wrote. The words entered the medical record.

He was not a nurse. He had no clinical training that would have allowed him to interpret what he was transcribing. He was a hand with a pen, present in the room because the physician's hand was not available. The documentation was real. The physician's voice was real. The clinical act was the physician's. And the hand holding the pen was someone else's.

I think about that arrangement more than I probably should.

---

The scribe is not a modern invention. Clinical documentation has required an intermediary since before the hospital existed in its current form. The ancient physician observed and reasoned; the scribe recorded. The ward nurse documented physician orders through the night. The medical secretary typed the dictated letter. In each arrangement, the same structural tension: the intermediary needed enough understanding to write accurately, but not so much autonomy that they were making clinical decisions. The physician was responsible for what the record said. Someone else was putting it there.

The Shabbat Writer arrangement worked because the boundary was explicit. Religious law defined who could write, when, and why the separation was permitted. Everyone in the room understood the structure. The record was the physician's. The hand was borrowed, not responsible. The physician owned the act; someone else held the pen.

The question the arrangement raised: when the voice and the record are separated by an intermediary, who owns the clinical act? In that context, the answer was built into the institutional framework that made the arrangement possible.

What happened next was that the intermediary left the room. And the answer became much harder to give.

---

From the 1990s into the 2000s, a large industry emerged around physician documentation. Physicians in the United States dictated clinical notes into recording systems. Transcriptionists in India and Pakistan listened and typed. Tens of thousands of people employed to be the physician's scribe, from a different country, in a different time zone, with no clinical background and no knowledge of the patient.

The Shabbat Writer arrangement, at industrial scale, with the accountability structure removed.

The religious framework that made the original arrangement coherent had defined clear boundaries: clinical authority, explicit structure, the physician present. That framework was replaced by a commercial arrangement that relied on the assumption that the physician would review and sign carefully. In practice, the review was often cursory. The physician's name went on the note. The physician had not written it. In many cases, the physician had not fully read it either.

The transcriptionist could not know when a dictation error was clinically significant. A wrong drug name. A missed negation: "no chest pain" transcribed as "chest pain." A confused unit of measurement. The transcriptionist typed what they heard. The error entered the record. The physician signed. The scribe had left the room. The responsibility had not gone with them.

---

The next attempt to solve this problem did not rethink the structure. It tried to automate the intermediary.

Dragon NaturallySpeaking launched in 1997 and changed the direction of the industry. Voice-to-text had arrived. The transcriptionist could, in theory, be replaced by software.

What the first-generation systems could do: convert speech to text with reasonable accuracy, given a trained voice profile and a quiet environment. What they could not do: understand clinical context.

The word "name" was transcribed as "name." Whether it referred to a drug name, a disease name, a family member's name, or the patient's own name was invisible to the system. "She was started on Metformin" and "her mother was started on Metformin" produced identical transcription; the clinical significance of the two sentences is entirely different.

Physicians adapted. They learned to dictate in a rigid, over-specified way. The scribe had been replaced by a machine that required the physician to do the interpretive work the scribe had previously done in the room.

---

The breakthrough, when it came, was not louder or faster. It was comprehension: the ability to recognize who did what, what mattered clinically, and where that information belonged.

Modern ambient clinical intelligence, including DAX Copilot, Abridge, Suki, and Epic's embedded ambient AI, introduced something the prior generation of tools had never had: named entity recognition combined with structured data extraction. The AI recognizes clinical context. It knows that "name" in the sentence "she was started on Metformin" refers to a medication. It knows that "started" implies a new prescription, not a continuation.

This is not transcription. It is comprehension. The physician speaks naturally. The documentation structures itself.

What is preserved from the original arrangement: the physician reviews. The physician signs. The clinical act remains the physician's in law and in practice.

What is new and unresolved: the intermediary now has opinions. It infers. It structures ambiguous information according to its training, not according to an explicit instruction from the physician. When it infers incorrectly and the physician signs without reading carefully, the error propagation is faster and the audit trail is harder to interpret than anything the offshore transcriptionist industry produced.

There is a subtler thing worth naming. Writing a clinical note was itself a cognitive act. Forcing yourself to articulate the impression was the moment of clinical commitment. When the ambient AI writes the impression based on what was said aloud during the encounter, the physician reviews rather than constructs. Whether the commitment is the same is a genuine question.

---

I am no longer a practicing physician. I am a senior product manager at SAP, and I use Microsoft Copilot in Teams meetings. The same core capabilities that made ambient clinical intelligence possible are now running in enterprise software.

The Shabbat Writer was present because the law required him to be. The meeting summarizer is present because the IT administrator enabled the feature. The physician in Jerusalem knew that someone was writing for them, understood why, and reviewed the record. The product manager in Irvine often clicks "looks good" without reading closely.

The question the Shabbat Writer raised has escaped the clinic. It is now the question every knowledge worker should be asking about every documented meeting, every auto-generated summary, every action item that appeared in someone's task list because the AI inferred it from a sentence that was spoken in passing.

---

My roommate wrote what my colleagues said. The offshore transcriptionist typed what they heard. Dragon transcribed phonemes. DAX Copilot recognizes and structures what it hears. Microsoft Copilot summarizes, prioritizes, and assigns.

As the intermediary became more capable at each step, the physician, or now the knowledge worker, became more likely to accept the record without examining it carefully.

The intermediary has changed. The structure has not. And the question of who is responsible for what the scribe writes remains exactly as unresolved as it was in the apartment where my roommate told me about his Friday evenings in the hospital.

He thought of it as an interesting job.

I am still thinking about it.

---

*This is part of the Signals Series — [data-decisions-and-clinics.ghost.io](https://data-decisions-and-clinics.ghost.io)*