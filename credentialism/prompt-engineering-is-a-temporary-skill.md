# Prompt Engineering Is a Temporary Skill

The first personal computer I owned was a Sinclair ZX81 with 1KB of memory. The only way to communicate with it was by writing programs in Basic. I was in elementary school, and the gap between what I wanted to do and what the machine needed me to say to make it happen felt like the most natural thing in the world. You spoke the machine's language. That was just how it worked.

In middle school I took my first official computer course as part of an enrichment program. We had access to a DEC PDP-11, which communicated through long strips of punched paper tape. You wrote your instructions offline, punched them into the tape, fed the tape into the machine, and waited. I learned the workaround. I got good at it.

Over the years I paid that price again and again. Microsoft DOS. Early HTML. CSS edited in Vi, where the keystrokes bore no relationship to the actions they performed. Each interface had its gap between what I wanted to express and what the machine needed me to say. Each gap had its workaround. I learned them all. Some I got genuinely skilled at.

When I first encountered AI prompt engineering, I felt something familiar: that particular gap again, and the familiar decision to lean into it rather than wait. Only this time the stakes were higher, and so was the investment.

So I did. I have written more prompts than I can count. I have built persistent AI personas with documented failure modes and run them against real product decisions. I have run full design thinking sessions with nine AI agents arguing across five structured phases for under ten dollars in API fees. I have built what some practitioners call digital twins: agents grounded not in invented characters but in the documented decision frameworks of specific people, with named mechanisms and named blind spots that make them argue in ways generic agents simply do not.

I had no choice. When you spend more time communicating with an AI than with most of the people in your life, you learn to speak its language well.

All of it works genuinely well. And I keep having the same thought: there must be a better way to do this.

That thought is also familiar. I have had it before, about every interface I have ever learned well.

There is one more signal that tells me this time is no different. Think about who is currently using AI and how. A developer writing a mobile application. An accountant reviewing tax deferrals. A graphic designer creating a logo. A film director rendering a scene. A composer working with audio. A product manager running market research. Every one of them is using the exact same interface to communicate with the machine: a text box, natural language, one surface for every domain.

That has never been true of mature technology. Developers have IDEs with syntax awareness and type systems. Designers have visual tools with layers and component libraries. Composers have DAWs with waveforms and MIDI tracks. Mature interfaces specialize because specialization closes the gap between how a domain thinks and what the tool needs to understand. The current AI interface has done the opposite: it has collapsed every domain into the same text box and asked everyone to become fluent in expressing their domain knowledge as natural language instructions to a machine. That is not a feature. It is the undifferentiated state of a technology that has not yet learned how its users actually work.

When those domain-specific interfaces arrive, and they will, the text box will look like the paper tape looked to me when the terminal finally arrived.

---

## What It Enables Right Now

Prompt engineering is not a single skill. It is a progression, and understanding that progression matters before dismissing the skill or over-investing in it.

At its simplest it is a framed question: give the model a role, a context, a task, and constraints, and the output improves immediately. At its more sophisticated levels it becomes something different: a persistent collaborator with a documented epistemic framework, a council of agents with irreconcilable perspectives that generates the kind of friction good human meetings produce at their best and almost never produce on schedule.

Three patterns within that progression produce the most consistent value, and they are worth naming specifically because they are closer to interface design than verbal persuasion.

Grounding constrains the model to use retrieved documents, cite specific sources, and acknowledge when the evidence is insufficient. This is how reliable information retrieval systems are built. It reduces hallucination and requires deliberate design.

Tool-calling defines which tools are available to the model and when to use them. These patterns are what make agentic systems function today. Getting the interaction right between a model and its surrounding tools requires careful specification.

Reasoning-control shapes the effort and format of the output: requesting a summary rather than a raw chain of steps, specifying output schema for downstream processing, tuning how much reasoning surfaces before the model concludes. These produce results that matter for production reliability.

These three will persist in some form even as the more artisanal parts of the skill disappear. The practical decision rule is clear: use text prompts for fast iteration and diverse tasks; move to more structured approaches when the task is stable, repeated at scale, and too costly to control through prompting alone.

The practitioner who masters these levels is already moving toward something that looks less like prompt engineering and more like systems design. The job title is following the same direction: what was called "Prompt Engineer" in 2023 is increasingly called "Context Architect" today, with responsibilities that span retrieval design, agent orchestration, and evaluation methodology alongside the prompt itself. Whether that trajectory continues or accelerates is a forecast, not a fact. The direction, at least, is clear.

---

## The Direction the Technology Is Moving

Here is where the pattern becomes harder to ignore.

Research on DeepSeek-R1 found that few-shot prompting degraded performance on reasoning benchmarks compared to simpler zero-shot approaches for that model. The technique considered essential practice for earlier models produced worse results on a newer one. Researchers called this the "reversal of few-shot efficacy," and it points to a meaningful shift: as reasoning models internalize more of the logical scaffolding that users once had to provide explicitly, elaborate prompt structure can interfere with the model's own reasoning rather than augment it.

Not every model behaves this way, and not every prompt pattern is becoming less useful. But the direction of travel is consistent: the prompting requirement is decreasing as model capability increases, and the craft that mattered most in 2022 is already less central than it was.

One study found that even carefully designed expert prompts satisfy requirements on the first try only 40 to 60 percent of the time, while automated optimization approaches, which treat prompts as parameters to tune rather than text to craft, brought that figure to 85 percent after a few iterations. The assembly-language-to-compiler transition has already begun. The courses teaching assembly language are still shipping.

---

## What Survives, and What to Do About It

Knowing what job you are trying to do does not disappear when the interface improves. Knowing what good output looks like does not disappear. Knowing when the result is wrong, and why, and what to do about it: this is judgment, and it becomes more valuable as the tooling matures, not less, because the tooling surfaces more output faster and someone still has to evaluate it.

For product managers specifically, the durable investments are evaluation and task specification. What does a good response look like? Where does the model fail, and which failure modes are acceptable? The better you can articulate the job, the constraints, and the success criteria, the more useful any AI tool becomes. This is product thinking applied to AI outputs, the same discipline that produces clear acceptance criteria and useful requirements documents. It transfers cleanly to whatever interface follows this one.

What transfers less cleanly is deep fluency in prompting patterns that will look significantly different in two years. The models are getting better at inferring intent. Investment in understanding their current quirks has a short return window. Investment in understanding the job those models are being asked to do does not expire.

These skills are bigger than prompt engineering. They existed before LLMs and they will exist after whatever interface comes next.

I learned DOS. I learned early HTML. I learned to edit CSS in Vi. I got genuine value from each and moved on when the interface changed. The practitioners who made those transitions well understood what they were trying to accomplish, not just the workarounds they had mastered. The ones who had only learned the workarounds were briefly stranded by the next interface before catching up.

Prompt engineering is the same test, running right now. Learn it. Go as deep as you can. The skills you build at the higher levels will transfer.

Just know what kind of skill it is.

---

*Yoram Friedman, MD is a physician and senior product manager at SAP Business Data Cloud. He holds three Harvard Medical School executive education certificates in healthcare digital transformation and AI.*
