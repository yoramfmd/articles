---
title: "The Command Line"
slug: the-command-line
published_at: 2026-08-13T04:10:34.000Z
custom_excerpt: "The word \"prompt\" was not invented for AI. It was on the screen in 1993, the C colon and the blinking line, waiting for you to learn the machine's language. We are teaching doctors DOS again. The interface will absorb the commands, the way it always does. What it cannot absorb is judgment."
tags: [healthai, signals]
feature_image: https://storage.ghost.io/c/e6/05/e605b234-3cc8-4fe4-97bb-2bb55b18b8fb/content/images/2026/08/ChatGPT-Image-Aug-12--2026--09_09_21-PM.png
source: ghost
---

In my medical school years in Jerusalem I had a side job that had nothing to do with medicine, or so I thought at the time. I was the computer instructor at the faculty. Physicians twice my age would sit next to me in front of a machine the color of old teeth, and I would teach them to find their own files.

The finding was the hard part. There was no desktop, no folder to click, no search box. There was a black screen, a blinking cursor, a pile of black five-and-a-quarter-inch floppy disks, and a file was a path you had to speak precisely: cd, dir, the exact name, the exact slash. I wrote the commands on index cards. The cardiologist kept his card taped inside a drawer, and when the card failed him he did not try a variation; he waited for me. He was one of the sharpest diagnosticians in the building. In front of that cursor, his expertise had no purchase at all.

What strikes me now is not that the commands were hard. It is how seriously we all took them. Departments ran courses. People were sent to training. Knowing DOS was, for a few years, a professional distinction worth putting on paper. And then windows and icons arrived, and the entire skill dissolved so completely that it is difficult today to explain what exactly we had been teaching. Not one of those physicians ever typed a path again. The files were still there. The judgment about what the files meant was still theirs. Only the interface layer had evaporated, taking our courses with it.

---

I thought of the cardiologist's index card this month while reading one of the new AI manuals for professionals. It was a good book of its kind, earnest and careful. It taught prompting techniques, temperature settings, how to run a local model, how to wire tools together. And a few pages in I realized I had read this book before, in 1993, when it was teaching cd and dir.

Most people have forgotten that we did not even coin a new word for it. The thing the cardiologist typed into, the C colon backslash and the blinking line waiting for his command, was called **the prompt**. That was its name for fifteen years, the prompt, the place where you spoke to the machine in its language and it did nothing until you got the syntax right. The word has now been reissued to a new generation that believes it was invented for AI. It was not. It is the oldest word in this story, and it means exactly what it meant then: the machine is waiting for you to learn its language, because it has not yet learned yours.

We are in the index-card phase of AI. The techniques being taught with such seriousness, the prompt patterns, the parameter dials, the home-built pipelines, are commands spoken to an interface that is still primitive, and the reward for learning them is real but expiring. Ninety percent of what these manuals teach will disappear into better interaction design, the way the command line disappeared into the desktop, because that is what interfaces do: they absorb the mechanics and return them as a button. I argued a while ago that prompt engineering is a temporary skill. The argument generalizes. Every skill defined by the current shape of the interface is temporary by construction.

Which raises the question the manuals never quite ask: if the interface layer is going to evaporate, what is worth teaching?

Here is the distinction I keep drawing in my books and in every session I run, and it is the whole of my answer. There is tools proficiency and there is AI proficiency, and they are not points on one scale. Tools proficiency is knowing this month's commands: which model, which setting, which incantation. AI proficiency is the mental change: understanding that the system is not a database of truth, that it fails fluently, that its confidence and its correctness are uncorrelated, that its output is a sample from a distribution and not a fact. Tools proficiency ages like the index card. AI proficiency transfers across every interface that will ever be built, because it is not knowledge about the tool. It is knowledge about what kind of thing the tool is.

The old proverb says that if you give a man a fish you feed him for a day, and if you teach him to fish you feed him for a lifetime. The manuals believe they are teaching fishing. They are not; they are teaching this season's rod, and the rods are being replaced every few months now. What feeds a professional for a lifetime is neither the fish nor the rod. It is knowing how to read the water: which catch is safe, which is spoiled, which glitters and should not be eaten. Teach a clinician the rod and you have prepared them for a product cycle. Teach them the water and you have prepared them for the technology.

The distinction sounds abstract until someone acts on the wrong half of it, so let me make it concrete. A spreadsheet made every analyst faster and made no company better at analysis; the analysts who thrived were the ones whose value had never been the mechanics. The AI tools on my own desk are doing for knowledge work what the spreadsheet did for analysis, and they will be as unremarkable within a decade. That is the tool. The transformation is elsewhere: for the first time the system does not just retrieve or calculate but decides and acts, and the professional's job shifts from operating it to judging it. A profession can miss that shift entirely while acing every prompting course, the way a department could send everyone to DOS training and still not understand what a database was about to do to medical records.

---

And there is a version of this confusion that worries me more than wasted training hours, because it has patients in it. The same manuals that teach the rod are teaching professionals to build. Wire a local model to your files. Assemble your own pipeline. The ambitious reader hears the next step coming: the clinic manager who believes that, given a weekend and a coding agent, he can produce his own scheduling system, his own note summarizer, eventually his own little EHR.

He can, in the sense that it will run. That is precisely the problem. The building was never the hard part; a coding agent will produce a working prototype of almost anything you can describe. What the weekend project does not come with is everything that makes software safe to point at patients: evaluation against the cases that do not match cleanly, a defined boundary where its authority stops, a record a reviewer can audit, a named person who answers when it is wrong. Enterprise software earns those properties slowly and expensively, and regulated software earns them under oath. A self-brewed tool in a clinic is unregulated software in a regulated room, and its most dangerous property is that it works in the demo. Enthusiasts, and I am one, should absolutely spend their weekends this way, on their own workflows, at their own risk. The line is drawn where the output touches a patient who never agreed to be part of the experiment.

The cardiologist with the index card understood something his course instructors did not teach him, and it is why I remember him fondly rather than as a cautionary tale. When the command failed, he stopped. He did not improvise syntax at a machine he did not understand; he knew the difference between the part of his work where his judgment was sovereign and the part where he was a guest. That instinct, knowing which side of the line you are standing on, is the thing I would put in every AI curriculum for every profession, and it is the one thing no interface will ever absorb on our behalf.

The commands I taught in Jerusalem are gone. Nobody misses them. The diagnosticians' judgment outlived every machine in that room, and it will outlive these machines too, but only for the professionals who understood which of the two they were being paid for. The manuals teach the cursor. The work is the water.

*This article is part of an ongoing series exploring how AI is integrating into medical practice and the systems built around it.  my books can be found at *[https://agenticaiproductmanagement.com/](https://agenticaiproductmanagement.com/)

---