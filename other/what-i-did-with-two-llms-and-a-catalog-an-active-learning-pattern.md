---
title: "What I Did With Two LLMs and a Catalog: An Active-Learning Pattern"
slug: what-i-did-with-two-llms-and-a-catalog-an-active-learning-pattern
published_at: 2026-05-12
custom_excerpt: "I had undiagnosed ADHD for most of my life. Lecture halls were the wrong delivery mechanism for me. So I went to the library, ran my own research, built my own curriculum. Six months ago, the constraint of scale disappeared. The library is still the right model. The library is just bigger now."
tags: [people, pm]
feature_image: https://storage.ghost.io/c/e6/05/e605b234-3cc8-4fe4-97bb-2bb55b18b8fb/content/images/2026/05/ChatGPT-Image-May-12--2026--01_38_22-PM.png
source: ghost
---

# What I Did With Two LLMs and a Catalog: An Active-Learning Pattern

# 

*The trilogy I just published described what is missing. This is what I built without waiting for any of it.*


---

I had undiagnosed ADHD for most of my life.

That sentence used to feel like an admission. It is also the most useful thing I can say about why the way I work now produces the volume of writing that it does. For decades, sitting in a frontal classroom was the wrong delivery mechanism for the way my attention actually operates. I skipped classes in undergraduate and went to the library. I ran my own research, wrote down the ideas I was tracking, photocopied the pages from the books that mattered, built a personal binder of references that bore no resemblance to the official syllabus and that I returned to constantly.

Medical school worked the same way. The lecture hall was a stretch. I mostly studied from copies of other students' notes, which I treated as raw material rather than authority. I extracted, reorganized, annotated, cross-referenced. The notebook I built became the thing I studied from. The lectures were the source. The notebook was the curriculum.

That pattern, library work, active synthesis, building my own curriculum from primary sources, was the only way I could learn at any real depth. It worked. It is also slow. The depth I could reach in a week was limited by how many books I could carry from the stacks, how many photocopies the library would let me run, how much I could read between everything else demanding my attention. I knew the method. I did not have the scale.

Six months ago, the constraint disappeared.

## The catalog

I started keeping a catalog of every article I wrote. The first entries were just titles and dates. Within a month, the catalog had grown to include the core argument of each piece, the key evidence I cited, the frameworks I introduced or referenced, and the cross-links between articles. By the time I noticed what was happening, the catalog had become a working knowledge base.

Today there are more than a hundred articles in it. Each one has a paragraph summary of its argument. Each named framework has its own entry: origin, core insight, design consequence, key phrase, related frameworks. Each cross-reference is traceable. The catalog is searchable, queryable, and grew faster than my ability to remember what I had already written.

The catalog is not the body of work. The articles are. The catalog is the index, the synthesis layer that lets me write the next article without losing track of the previous hundred. It is also what most education programs never give you. A curriculum that is yours, that reflects how you actually think about the field, that compounds with every piece you add.

The catalog also became the working memory for the LLMs and, when I am honest, for me. When I start a new article, I hand the catalog to the model so it can find the prior framework I want to extend, the example I already used, the article I do not want to repeat. It returns answers I had forgotten I had given. I do the same thing in the other direction: I search the catalog before a meeting, before a talk, before a difficult email, to find the framework or the reference or the dated study that fits the moment. The catalog remembers things on my behalf that I could not hold in working memory while doing the job. It also surfaces the gaps. A topic that has no entry is a topic the body of work has not yet covered, which is sometimes the most useful information the catalog produces.

I built it because I needed it. The byproduct is that I now have a textbook on the field I work in, written from my own perspective, organized in a way that matches my own working memory, drawn from primary research I commissioned and synthesized deliberately, in a field that has no textbook yet. Anyone trying to learn what I work on (agentic AI for product managers, healthcare AI governance, the personnel infrastructure that does not exist for AI agents) would find no formal course covering it. There is not one. I had to build the course in order to take it.

That is the part that I want other people to notice.

## The choreography that fills it

The catalog grows because something feeds it. Earlier this year I started writing a series on agentic AI product management, six articles, twenty-five hundred to four thousand words each, and the workflow I had built by then is the same one I still use. The argument and the spine are always mine. The lived experience is mine. The editing and the final calls are mine. Everything else is a deliberate orchestration of five different AI systems, each doing the thing it does best.

The first half of the workflow is what you would expect. I write a one- to three-page spine document by hand: thesis, argument, personal experience, three or four claims that need evidence, gaps I need filled. Then I open three deep-research sessions in parallel (Gemini, ChatGPT, Perplexity), feed the same questions to each, and read the three reports side by side. The agreement is usually the canonical evidence. The disagreement is usually where the interesting argument lives. The omissions are what I learn to chase next. Triangulation by design, the way an academic researcher checks an unfamiliar claim across multiple databases, except the synthesis happens in twenty minutes instead of two weeks.

The non-obvious steps come next.

**Drafting with Claude.** Claude (mostly Sonnet 4.6 for months, more recently Opus 4.7) became the writing partner. I would hand it the spine plus the synthesized research and ask for a draft that hit the argument I wanted to make. The draft was always wrong in interesting ways. We would iterate, sometimes ten or fifteen passes, until the piece sounded like me and made the argument cleanly.

**Perplexity as LLM-as-judge.** Before publication, I ran every factual claim, every citation, every dated study, through Perplexity in validator mode. Fact-checking by a different model from the one that drafted. Catches hallucinated citations, misremembered statistics, inverted findings. Not perfect, but it caught more than my own reading ever would.

**Voice calibration across models.** This is the role that is hardest to describe and possibly the most important. After the draft is technically correct, it still has to sound like me. Claude's drafts read as Claude unless you actively pull them toward your own voice. Different versions of Claude bleed differently. Sonnet 4.6 is light, fast, and direct; Opus 4.7 is more layered and tends toward reassurance constructions and over-explanation. Both produce competent prose. Neither, by default, sounds like me.

The version of this step that actually works for me started with a long, deliberate calibration. Months ago, I wrote out my own voice profile in detail. The kind of openings I use. The rhythm I default to. The phrases I avoid. The constructions that read as not-me. I refined the profile through dozens of sessions with Sonnet 4.6, correcting it when it drifted, adding rules when I noticed something it kept missing, until Sonnet 4.6 had a working internal model of how I write that was accurate enough to flag voice issues on the fly. The calibration was not free. It cost me real time over months, and the deliverable was a working reader, embedded in one model instance, that could tell when prose did or did not sound like me.

Then I switched to Opus 4.7, and I could not find my voice anymore.

The transition was harder than I expected. Opus is more capable in many ways. It is also a different writer, with different defaults, and the careful voice instructions I had built over months were tuned to Sonnet 4.6's particular tendencies. Some of them transferred. Many did not. For weeks I was producing prose that was technically fine, factually careful, well-argued, and not mine.

The fix was cross-model coaching. I started handing Opus drafts back to the Sonnet 4.6 session that had months of accumulated context on my voice. Sonnet 4.6 read the draft, named the tells, and returned a structured list. "Opus consistently writes a setup sentence that explains what is about to be said, then says it. You do not. Cut the first sentence." "Opus closes paragraphs with fully formed complex sentences. You close with something blunt." "Opus adds reassurance-then-reframe constructions that you do not."

Five concrete rules came back from one pass. I gave them to Opus. The next draft was materially closer to my voice. The pattern has held since.

That is the part of the workflow I want to name carefully, because it is the part that the AI-writing discourse has not caught up to yet. The model writing the draft has a personality; the model reviewing the draft has its own personality plus accumulated context on yours; the two of them together, with you as the final editor, can converge on something that reads as yours much faster than either could alone. One model coaches the other on which costume to wear. The coaching only works because I spent the months building the calibration that one of them now carries.

That is the choreography. Six roles. I am the supervisor at the top of the loop, doing the work that none of them can do: the thesis, the personal experience, the final calls about what is true and what ships.

## What this is

I recently published a trilogy of articles describing the structural problems with the way enterprises are deploying AI agents. The trilogy ends on a structural prediction: the validator atrophies, the supervision channel collapses, the codebase drifts toward the agent's defaults.

That is the default. Most users are using AI as a content faucet. The faucet produces output, the user signs off on it, the loop has no validator role except by accident. The atrophy follows.

What I am describing here is the same problem from the inside. I am the supervisor in my own loop. The role is not implicit; it is the entire reason the loop exists. The AI does the volume work, the parallel research, the drafting, the fact-checking. I do the thinking that determines what the volume is for.

Done this way, the loop is not a productivity tool. It is an active-learning protocol. Every article is a synthesis exercise that forces me to defend a thesis against three different research traces, work through ten or fifteen drafts of the argument, and check every factual claim against an independent validator. The cognitive work that happens during a single article is, in my experience, equivalent to what I would have learned in a full graduate seminar on the same topic, compressed into a week and shaped to a specific question that mattered to me at the time.

This is the practice the trilogy implies but did not name. I named it for myself out loud, here, because the implication is doing real work in my life and I want to put it in front of people who might find it useful.

## What this is not

It is not a substitute for the institutional infrastructure the trilogy described. The active-learning loop solves the individual version of the validator-atrophy problem. It does not solve the enterprise version. An organization deploying agents to a hundred engineers cannot ask each engineer to run a personal five-LLM orchestration. The structural answer (rate-aware sampling, drift detection, validator rotation, the missing supervisor role) still has to be built at the institutional level. What I built solves my problem. It does not solve theirs.

What I would say to a reader asking whether they could do something similar: the specific stack does not matter. The roles matter. Find the version of the spine document that fits your work. Run the research step in parallel using whatever instruments you have access to, not because more sources is better but because triangulation surfaces disagreement and disagreement is where you learn. Use one model to draft and another to validate. Keep a catalog from the first piece, before you think you need one. Treat yourself as the supervisor at the top of the loop, not as the user of a tool.

The trilogy named what is missing in the enterprise. This piece names what is possible for the individual practitioner who is not waiting for the enterprise to catch up.

The library is still the right model. The library is just bigger now.


---

*This is a companion piece to the three-part series on the personnel infrastructure that does not exist for AI agents. The trilogy described what is missing structurally. This piece describes what one person built without waiting.*
