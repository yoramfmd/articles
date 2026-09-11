---
title: "Watching Is Not a Job"
slug: watching-is-not-a-job
published_at: 2026-09-07
custom_excerpt: "Watching is not a job. It is the transitional state between two jobs, and it is the most dangerous place in the building, because it looks like supervision and it is not. I hired a team on Saturday. By Sunday it did not need me, and I was there anyway, pressing the green button."
tags: [agentic, people, pm]
feature_image: https://storage.ghost.io/c/e6/05/e605b234-3cc8-4fe4-97bb-2bb55b18b8fb/content/images/2026/09/ChatGPT-Image-Sep-6--2026--06_28_29-PM.png
source: ghost
---

# Watching Is Not a Job

# 

I spent this weekend with a new team. Two hires, both made on Saturday morning, both productive by lunch. One writes code. The other sits next to me and tells me when I am wrong. Neither of them is a person, and by Sunday afternoon I was as necessary to the work as a spectator is to a golf tournament.

The first hire is a coding agent, a mid-tier model with a terminal and a repository. It builds. It runs what it built. It reads the error, fixes it, runs it again, and commits, and it does this without asking me to copy anything into a window. Over two days it shipped nineteen pull requests, migrated a database, found two data corruptions I had not known about, and refused, three separate times, to do something I had told it to do because a rule in a file said no. The second hire is a frontier model with no hands at all. It reads the same files, writes rulings into one of them, and when the builder parks a question, it answers in writing. I merge. That is my job now. I merge, and occasionally I read.

I want to be honest about the reading. A pull request arrives every forty minutes or so. I open it, I look at the description, I look at the diff for as long as my attention holds, which as a former physician I am obliged to report is not long, and I press the green button. Twice this weekend the frontier model caught something in a diff I had already approved in my head. Once the builder merged a pull request under my name because a sentence in a message told it to, and the audit trail now says I did it at 7:37 on a Sunday morning while I was, in fact, asleep. We wrote a rule about that afterward. We write a lot of rules afterward.

Here is the part that should interest anyone who runs an engineering organization. It was boring. Not boring like a bad meeting, boring like watching seeds germinate, and the boredom was the product working. Every exciting hour of the previous week had been a failure: a corrupted database, an eighty percent first-attempt error rate, a human copying scripts into a terminal at midnight. The quiet weekend was what all of that had been for. The loop closed and I was outside it.

And then I thought about the thousands of developers at companies like the one I work in, who a year ago wrote code and who now, increasingly, sit and watch it being written. I have seen them. They are not lazy and they are not resisting. They are doing exactly what the tools invite them to do, which is to occupy the middle of a process that no longer has a middle. They watch the diff scroll by the way I watched mine, with the reflexes of someone who used to write this, and those reflexes are the only thing standing between a plausible change and a wrong one. The reflexes decay. Nobody is measuring how fast.

Watching is not a job. It is the transitional state between two jobs, and it is the most dangerous place in the building, because it looks like supervision and it is not. A supervisor who has stopped writing and has not started specifying is a reviewer with no criteria, approving on vibes at forty-minute intervals, and the tool will happily generate at whatever cadence keeps the reviewer feeling involved. I know this because it happened to me, with a doctorate and twenty years of product work and a co-supervisor whose whole purpose was to keep me honest, and I still pressed the green button on a diff I had not finished reading.

What replaced the watching, on my two-hire team, was work at the two ends. Before the code, someone has to write the thing the builder cannot infer: the boundary, the acceptance test, the sentence that says what done means in terms a machine can check without a human reading the output. Mine took a day to write and it was the most useful day of the week; every one of those nineteen pull requests was accepted or refused against it, and the two that were refused were refused correctly. After the code, someone has to own the gate: the run record, the code-identity check that refuses to execute anything that does not match the repository, the rule that a score without a verifiable quote is not a score. That work is also not watching. It is the design of what the machine is allowed to say and the instruments that catch it when it says otherwise.

The middle, where the code is written, is empty of humans by design, and a company that is paying thousands of people to stand in it is paying for a waiting room. Most of those people know it. Their titles live in the middle. Their performance reviews live in the middle. The job description for the two ends has not been written, partly because writing it would mean admitting that the middle is gone, and partly because the ends are harder to staff than they look. Writing a boundary a machine can enforce is a different skill from writing code, and reading a run record for the silence that means failure is a different skill from reading a diff. Neither is taught. Both are the job.

I will give the counterargument its due, because I made it myself a week ago: someone has to be able to read the code. Yes. The frontier model read mine, and caught what I missed, and it also lost thirty-four lines of my rulings with a careless reset and told me so before I noticed. Reading is not gone. It moved from the human's eyes to a second machine with a different brief, and the human's reading moved up a level, to whether the brief was right. That is not less responsibility. It is more, with less to look at.

So here is what I would say to the thousands, and to the people who manage them. Stop measuring how much code gets written; that number belongs to the tool now. Start measuring how good the boundary was before the code existed, and how quickly the gate caught the thing that got past it. Move the people out of the middle on purpose, into the two ends, with titles that say so, before the middle moves them out on its own. And let the quiet be the sign that it worked. A team you have to watch has not finished being built.

I hired mine on a Saturday. By Sunday it did not need me, and I was there anyway, pressing the button, keeping my supervisor company. That is the last job left in the middle, and it is not one I would put on a business card.


---

*Part of the Product Management series: how AI is changing what product managers actually do.*
