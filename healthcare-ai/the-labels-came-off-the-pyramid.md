---
title: The Labels Came Off the Pyramid
slug: the-labels-came-off-the-pyramid
published: 2026-08-07
excerpt: A new paper rebuilds the DIKW pyramid for medicine and shows where AI actually breaks. Strong on the arrows nobody worried about, weak on the one the structure depends on. The pyramid always assumed you could tell which layer you were standing on. That assumption is gone.
url: https://data-decisions-and-clinics.com/the-labels-came-off-the-pyramid/
tags: Healthcare AI, Agentic AI, Product Management
source: ghost-api-pull-2026-08-16
---

The first time a radiologist dictates a report, somebody explains the thing that actually matters, and it is not about the images.

It is that the person reading the report will almost certainly never look at the film.

The surgeon reads the paragraph. The referring physician reads the paragraph. A discharge summary quotes it, and six months later somebody makes a decision from that quote. Everything the radiologist saw, everything weighed, every alternative considered and set aside, compresses into a few sentences of confident prose and then travels onward without its author.

That is why the hedging vocabulary exists. Cannot exclude. Recommend clinical correlation. Findings are nonspecific. Those phrases are the only mechanism available for telling a reader who cannot see the images how much weight the sentence will bear.

I have been thinking about that responsibility since reading a new perspective piece in npj Digital Medicine, because it is the same problem, scaled up until it stops being about one report and starts being about how an entire profession knows anything at all.

### A Pyramid Everyone Uses and Nobody Examines

Anyone who has worked in data has drawn the DIKW pyramid. Data at the bottom. Information above it. Knowledge above that. Wisdom at the top. It shows up in every data strategy deck ever made, usually in the first five slides, usually as decoration.

It is worth remembering where it comes from. The usual trail leads back to a T.S. Eliot poem from the nineteen thirties, which asks where the wisdom went that we lost in knowledge, and where the knowledge went that we lost in information. It was a lament, not an architecture. We made it into a staircase.

The authors of this paper, a group from University College London, Moorfields and Tsinghua, use a version tuned for medicine. Data, information, evidence, practice. Raw observations become information when someone organizes and contextualizes them. Information becomes evidence when it meets methodological standards. Evidence becomes practice when it is synthesized into guidance somebody can act on.

Their example is one I know well. A retinal photograph is data. A grader who looks at that photograph, labels the microaneurysms and hemorrhages and assigns a severity, has produced information. Cohort studies and trials that establish how often retinopathy progresses and whether early treatment preserves sight are evidence. The recommendation that adults with diabetes get regular eye examinations is practice.

Here is the part the enterprise version of the pyramid quietly deleted.

In a data architecture, the arrows between the layers are pipelines. Something moves and gets transformed. In medicine, the arrows are appraisal. Each one is a human act, with a named method, performed by somebody accountable for having performed it. The pyramid was never really about the layers. It was always about what happens between them.

### Where the Machines Are Good, and Where They Are Not

The paper collects what large language models can currently do across this workflow, and the pattern is sharper than I expected.

Filtering titles and abstracts, approaching human performance. Full-text screening, comparable to humans under good conditions. Pulling structured data out of supplied text, better than ninety-eight percent accurate on pre-specified elements. Recognizing the components of a clinical question, around eighty percent.

Read that list again and notice what it is. Every one of those is a move within a layer, or the arrow from data to information. Sorting, extracting, reorganizing, summarizing. The machines are genuinely strong there, and pretending otherwise is not skepticism, it is denial.

Now the failures, and they land in a suspiciously specific place.

That eighty percent on question components conceals much higher error rates on the items involving causal inference. Full-text screening, which looks human-comparable in favorable conditions, degrades sharply when the include and exclude piles are evenly balanced, approaching no useful discriminating power at all. Sit with that one. Balanced piles are exactly what a genuinely contested clinical question looks like. The tool works where the answer was obvious and fails where you needed help.

And at the steps that assess risk of bias and grade the strength of a body of evidence, which are precisely the transitions that move information into evidence, the paper's judgment is blunt. Even capable systems reproduce text that mimics the language of appraisal without performing the evaluative reasoning that gives the appraisal its meaning.

So the strength is in the arrows nobody was worried about, and the weakness is in the one arrow the entire structure depends on.

### Three Ways to Break the Structure

The authors name three failure modes and I think they are worth carrying around.

Information with no data underneath it. A confident statement, a citation that is fabricated or misquoted or simply does not support the claim attached to it.

Data amplified without becoming information. Volume that adds nothing, papers that are technically new and substantively identical to what already existed.

Information without verification. Even when the sources are real, the systems rarely expose the chain, and they are poor at signaling how uncertain they are.

Their conclusion from this is the sentence I would put in front of anyone building a data product. Large language models are rendering the evidential status of their outputs invisible to the reader.

### The Pyramid Assumed You Could Tell

That sentence is where this stops being a medical argument and becomes a product one.

Every version of the pyramid, in every industry, quietly assumed a thing that used to be true. You could tell which layer you were standing on by looking. A spreadsheet of readings looked like data. A dashboard looked like information. A validated model with a card attached looked like knowledge. A guideline looked like guidance. The form told you the status, and the form was reliable because producing each one required a different amount of work by different people with different training.

The labels have come off. Every layer now arrives in the same wrapper, which is fluent, structured, confident prose. A summary of three papers and a summary of three hundred read identically. A synthesis grounded in verified sources and one assembled from a model's memory read identically. The signal that used to tell you where you were standing was never explicitly designed. It was a side effect of how expensive each layer was to produce.

And that is the second thing worth naming. The pyramid had a cost gradient. Climbing it was expensive, and the expense was the quality control. Nobody produced a systematic review casually. The friction was doing real work, invisibly, on everyone's behalf.

That friction is now close to zero, and we did not replace what it was doing.

### Evidential Literacy Is the Competency

The paper argues that understanding this hierarchy is a core professional skill rather than an academic nicety, and makes a point I want to put in product terms.

Someone who cannot tell whether an output has evidentiary status, or merely resembles it, cannot meaningfully oversee the system they are accountable for.

That is a supervision argument wearing an epistemology costume, and it applies well outside medicine. If your reviewer cannot tell which layer an output belongs to, their approval carries no information. They are not validating. They are witnessing.

There is a related line from Cochrane's position on AI in evidence synthesis that belongs on a wall somewhere. Users are ultimately responsible for the downstream outputs. Not the tool. Not the vendor. The person who passed it along.

Which points at something concrete you can actually build. If an output is going to travel without its author, then the layer has to travel with it. What is this made of. What was checked, by what method, by whom. Where does the chain break. Medicine spent decades building that vocabulary and calls it a hierarchy of evidence. Most data products have nothing equivalent, and the reason is not difficulty. It is that the pipeline was never asked to carry it, because the form used to say it for us.

I should be fair about what this paper is. It is a perspective, an argument rather than a study, published ahead of final editing, written by people who work in exactly the field their example comes from. It does not prove anything. It organizes something that was already true and gives it a shape you can use.

### Back to the Report

Everything weighed, compressed into a few sentences, traveling onward without its author.

That was always the deal in a radiology report, and medicine handled it by building an entire register of language whose only job is to tell a reader how much weight a sentence will bear. Cannot exclude. Findings are nonspecific. It is not hedging. It is a status label, attached at the source, by the person who did the looking.

We are now generating that kind of output at a scale nobody has ever had to handle, in a form that carries no label at all.

Eliot asked where the knowledge went that we lost in information. The uncomfortable answer is that we did not lose it. We just stopped being able to tell the difference.

---

*Reference: Wu, Y., Ong, A. Y., Hu, K., Wong, T. Y., and Keane, P. A. (2026). "Fast information and slow evidence in the large language models era." npj Digital Medicine. Open access. This is a Perspective piece, published as an accepted manuscript ahead of final editing. The DIKW hierarchy is usually traced to T.S. Eliot's "The Rock" (1934) by way of Russell Ackoff's "From Data to Wisdom" (1989).*
