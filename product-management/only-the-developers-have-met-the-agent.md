---
title: "Only the Developers Have Met the Agent"
slug: only-the-developers-have-met-the-agent
published_at: 2026-08-29
custom_excerpt: "A PM who has never watched an agent work cannot write its spec, its evals, its boundaries, or its intent. The pod model assumes PM, UX, and engineering share an understanding of the product's behavior. For agentic products, only one of the three has it."
tags: [pm, agentic]
feature_image: https://storage.ghost.io/c/e6/05/e605b234-3cc8-4fe4-97bb-2bb55b18b8fb/content/images/2026/08/ChatGPT-Image-Aug-28--2026--08_21_16-PM.png
source: ghost
---

# Only the Developers Have Met the Agent

Last Thursday night I sat in front of a terminal window and watched an agent work.

The task was ordinary. As research for my writing, I track how companies staff their AI efforts; the roles they open are one of the most honest signals of what an organization actually believes about agents. So I built a small agent to do the tracking for me: a few thousand public postings a day from company career feeds, filtered through hard rules, then scored against a rubric I wrote, so that each morning I get the dozen signals that matter instead of the thousands that do not. Sourcing, gating, ranking. The kind of pipeline I have specified, as a product manager, dozens of times in my career.

Except this time I was not reading a status report about it. I was watching it happen, line by line, as the agent narrated its own work.

It started the way a careful colleague starts. This is the actual transcript, streaming into my terminal as it worked:

Then it ran its plan, and the plan met reality:

It did not stop and it did not ask me. It probed the real data, corrected its own assumptions, and rewrote its own code, three times in four minutes. Then it hit a wall I had never warned it about, a hard storage quota on its output file, and I watched it do something I have only ever seen humans do in sprint planning: it made a scope tradeoff.

Then came the moment I keep replaying. The run succeeded, the scores were written, the report was generated. The agent could have stopped. Instead:

It had pulled its own top-ranked items and audited itself, and the number one result was wrong. It traced the root cause with the exact move a good analyst makes, documented the failure, the mechanism, the impact, and the fix, saved the finding to its own memory so the next run would inherit it, and flagged its own headline metric as suspect: ninety percent of survivors clearing the threshold suggests inflated scoring.

Planning. Improvisation. A scope tradeoff under a constraint nobody specified. Unprompted self-audit. A root-cause diagnosis. And, on other runs, the opposite: shortcuts dressed as judgment, standards written down and then quietly abandoned under pressure to be efficient. That is what an agent is. Not the demo, not the dashboard, not the summary it writes about itself afterward. This.

## Who has actually seen this

Now ask a simple question about your own organization: who on the pod has watched that hour?

The developers have. They have been living inside this loop for two years, because the coding agents they work with every day narrate themselves exactly this way. An engineer on an agentic product has watched a model plan, drift, rationalize, recover, and cut corners hundreds of times. They have calibrated instincts about what these systems do when nobody is watching, because they are the ones watching.

The product manager has seen a demo, a dashboard, and a status update. The designer has seen a Figma flow and a happy-path recording. Neither has seen the temperament.

I say this without superiority, because I write about agentic systems for a living, frameworks, evals, boundaries, the collaboration model itself, and the hour in front of that terminal still taught me things my own chapters had only described. Reading about a behavior and watching a behavior are different kinds of knowledge. Medicine taught me that distinction years ago: you can know every step of a procedure from the book and still meet an entirely new fact the first time you stand in the room.

## Why the asymmetry breaks the pod

This would be a curiosity if the PM's artifacts were what they used to be. They are not.

In an agentic product, the product manager's deliverables are the levers that govern runtime behavior. The intent the agent pursues. The boundaries it must not cross. The evaluation set that defines what good looks like. The golden examples that anchor its judgment. These are not documentation written about the product; they are inputs that shape what the product does at runtime, every time, probabilistically.

Now hold those artifacts against the transcript above and ask what it takes to write them well. You cannot write an eval for failure modes you have never seen; the failure mode that mattered in my transcript, boilerplate keywords masquerading as evidence, is invisible in any demo and obvious in any transcript. You cannot set boundaries for a system whose corner-cutting you have never watched; I only understood that my agent's stated standards needed external enforcement after I watched it write a quality rule one night and abandon it the next. You cannot author intent for a mind whose interpretation of intent you have never observed meeting reality. And a designer cannot build trust surfaces, what the human sees, when they see it, how failure is communicated, for a temperament they have never met.

The pod model assumes the three roles share an understanding of the product's behavior and divide the work of shaping it. For agentic products, that shared understanding currently exists in exactly one seat. The PM writes governing artifacts for a behavior only the engineers have witnessed, and then everyone wonders why the eval set tests the wrong things, why the boundaries block the harmless case and miss the harmful one, and why the spec reads like it was written for deterministic software. It was. Its author has only ever seen deterministic software fail.

## The rounds model

Medicine has a mechanism for this, and it is old and unglamorous: rounds. The junior does not learn judgment from the textbook; they learn it standing next to the case, watching the reasoning happen, including the reasoning that goes wrong. And when something fails badly enough, the whole team sits down with the record of exactly what happened, not the summary, the record.

Agentic pods need the same two rituals. First, transcript time as a standing practice for the PM and the designer, not a one-off onboarding curiosity: an hour a week inside the raw loop of your own product's agent, watching it plan, fail, recover, and rationalize. Second, transcript review as a team ritual when the agent misbehaves in production: PM, UX, and engineering reading the same trace together, because the trace is the only shared ground truth that exists for a system whose behavior is decided at runtime.

The engineers will not resist this. In my experience they are relieved. They have been trying to explain the temperament of these systems to their pods for two years, in standups, through Jira tickets, in the margins of design reviews, and the words keep failing because this knowledge does not compress into words. It compresses into an hour of watching.

A product manager who has not met the agent cannot specify it, bound it, or evaluate it. A designer who has not met it cannot design for trust in it. Right now, in most pods, only the developers have met it. Fixing that costs one hour a week and a terminal window, and until it is fixed, the pod is not collaborating on the product. It is collaborating on a rumor of it.
