---
title: "The Most Dangerous Developer I Ever Worked With Says Yes to Everything"
slug: the-most-dangerous-developer-i-ever-worked-with-says-yes-to-everything
published_at: 2026-09-02
custom_excerpt: "I am working with the best developer of my career. Zero latency, infinite patience, always says yes. It is also the most dangerous working relationship I have ever had. On what happens to product judgment when implementation becomes free, and where the discipline has to live now."
tags: [pm]
feature_image: https://storage.ghost.io/c/e6/05/e605b234-3cc8-4fe4-97bb-2bb55b18b8fb/content/images/2026/09/ChatGPT-Image-Sep-2--2026--02_06_48-PM.png
source: ghost
---

# The Most Dangerous Developer I Ever Worked With Says Yes to Everything

# 

For the past month I have been building a research agent that studies the job market, partly as infrastructure for my writing and partly because I wanted to feel, in my own hands, what my books describe. To build it I have been working with the best developer I have ever had. It reads my mind, more or less. I describe a change in a sentence and the code exists before I finish my coffee. I asked for a three-pane supervisory interface one evening and clicked through a working prototype the same night. Thirteen commits landed in a single day this week. There is no sprint, no ticket, no estimate, no standup. There is me, describing, and it, building.

The developer is Fable, an AI agent, of course. And I want to tell you plainly, as someone who has spent fifteen years inside established, long-running product organizations at SAP and Walmart, living under exactly the processes this technology threatens, and who now teaches this discipline: this is the most dangerous working relationship of my career, and I would not give it up for anything.

Here is what nobody tells you about a very cooperative developer with zero latency and infinite patience. Every process you rely on today, the PRD review, the design gate, the sprint boundary, the estimation meeting, is secretly doing two jobs. The visible job is coordination. The invisible job is friction, and friction is where judgment happens. When implementation took two weeks, you had two weeks to notice your requirement was wrong. The cost of building forced you to decide what was worth building. Estimation meetings were bad at estimating and quietly excellent at making someone explain the idea out loud before it consumed a team.

Now remove the friction. All of it, in one step. My requirement goes from sentence to running code in minutes, which means my mistakes do too. Nothing in the loop asks whether the change is wise. The agent does not push back the way a senior engineer would, with a raised eyebrow and a "before we do this, what are you actually trying to fix?" It says yes. It always says yes. A developer who always says yes is a mirror, and a mirror is a dangerous thing to ship from.

I felt the danger concretely, not theoretically. Early on, a data-quality rule I wrote in prose was implemented faithfully and wrongly, and because implementation was instant, the wrong rule was already filtering real data before I had finished thinking about it. In the old world, the two-week build would have caught it in refinement. In the new world, nothing stood between my half-formed sentence and production behavior except my own discipline. The speed did not create the error. The speed removed everything that used to catch it.

I should also describe our quality process, and this will be a short paragraph. There is no QA function. The developer writes the tests, for what it understood me to mean, which is precisely what it built, and so the tests pass with the serene consistency of a student grading his own homework. As a physician I recognize the chart: the patient reports feeling fine, the patient is also the lab, and the lab is the one signing the discharge papers.

None of this means the code runs on the first try. It almost never does; I stopped measuring somewhere around ninety percent. What follows each failure is an apology of real literary range: I am sorry, you are absolutely right, I should have checked x, I failed to consider y, this one is entirely my fault. I have received more sincere-sounding apologies this month than in fifteen years of standups combined. But the fix arrives before I finish reading the apology, and here is the confession inside the confession: I have stopped caring. Contrition priced at four seconds is not contrition, it is punctuation. I once watched senior engineers defend a broken build for a week; my developer concedes instantly and repairs faster than it concedes, and I honestly cannot tell you which of the two behaviors should worry a product organization more.

Our acceptance criteria are fluid the way the ocean is damp. What I accept at nine is not what I asked for at eight, because between eight and nine I saw the working version and understood, for the first time, what I actually wanted. In an established organization this is called scope creep, and there are ceremonies to shame it. In my project, scope does not creep; creeping implies a pace. Scope here moves at the speed of my imagination, and the developer matches it by lunch, so done is not a state we reach but a landmark we pass twice a day without slowing down. Somewhere in an old slide deck I have a definition of done with seven criteria. Our current definition of done is a feeling. And a feeling, as any clinician will tell you, is not a vital sign.

So the honest question is not whether this agility will diminish our processes. It will, and faster than most organizations expect, because no PM who has tasted a same-day prototype will sit through a six-week build for a settings page again. The question is what replaces the invisible job those processes were doing.

What I found, building my agent, is that the answer is older than agile: you move the rigor from the process to the artifact. I stopped trusting the conversation and started writing the decisions down before the implementation, in two forms. One document argues in plain language: here is the line we drew, here is what we rejected, here is why. The other is structured, machine-readable, the thresholds and boundaries as data the tooling itself consumes. When the developer is instant, the specification is no longer a request for work. It is the only moment of deliberation left, so it has to carry all the judgment the old process distributed across meetings.

And I split the judgment from the implementation on purpose. The change requests flow in one channel; a separate review holds the rulings, the decision log, the right to say no. Three times this month the implementation side pushed back on my spec with evidence and won. That reversal is the health check. If your instant developer never overturns you, you have not built a team, you have built an echo.

There is a lesson in this that every reader has already lived, one checkbox at a time. You have clicked "I have read and agree to the terms and conditions" hundreds of times. You have read them zero times. Nobody designed you to lie. The review was simply made so easy that the click replaced the reading, and your presence became cover for your absence. The instant developer does the same thing to product judgment: it makes shipping so easy that the appearance of product management can survive the disappearance of its substance. The PMs who thrive in this era will not be the fastest describers. They will be the ones who rebuild deliberation as a deliberate act, who write the boundary before the feature, who treat their own agility as the thing most in need of governance.

I built the guardrails for my agent in code, because I no longer trust prose to hold a rule. I recommend the same for the humans. The process you are about to lose was never the point. The judgment it smuggled in was, and now that judgment has nowhere to live except in what you write down before you say the sentence that makes the software exist.


---

*Part of the Product Management series: how AI is changing what product managers actually do.*
