# Your Agent Worked. Your Users Bypassed It.

When I was a resident in anesthesiology, the operating-room monitors beeped constantly. They beeped for the things that mattered: a drop in oxygen saturation, an arrhythmia, a blood pressure trend heading somewhere uncomfortable. They also beeped when someone leaned on a cable, when an SpO2 probe slipped off a finger, when a pressure transducer briefly zeroed out during a position change. The beep for "your patient is desaturating" and the beep for "I dropped the lead on the floor" sounded the same. After enough hours in the room, we stopped hearing most of them.

That is alert fatigue, and it cost the field decades to solve. Designers tried everything at the interface. Different tones. Smarter filtering. Color-coded priorities. None of it worked at scale. The real problem was never the alert. It was that the system around the alert, the workflow, the staffing, the institutional tolerance for noise, had never been redesigned with the alert in mind. What fixed alert fatigue in the hospitals that actually fixed it was not better alarm tones. It was protocol design. Escalation rules. Who gets paged for what. When silencing an alert is permitted, and when it is not.

I thought about this the other day, reading a quiet paper that is going to matter more than most people realize. It is called "Expecting Automation: How Users Miss Valuable Experiences in Generative AI," by Aeneas Stankowski at the German Research Center for AI (DFKI), presented at the AutomationXP workshop at CHI 2026, with SAP as the research partner and host organization.

The prototype the team built is a conversational AI designed to help employees set better goals. It did not generate one-line goal statements. It asked questions. It walked users through dimensions of their work they had not thought about. It was built to prompt reflection, not just to produce output. In structured sessions with fifteen SAP employees, ninety-three percent said they would adopt it if it were available.

Then the team made it available.

The same users who called the experience "productive rigor" in the structured sessions started answering the AI's questions with questions of their own. They asked it to skip the thinking and just write the goal. They redirected the interaction back to output. The interface had not changed. The users had not changed. What changed was everything else.

The study is small. Fifteen participants, one company, one task type, in a context where goal-setting had already eroded into a compliance exercise. Generalization is an open question. But the mechanism the paper surfaces is recognizable enough to take seriously at this sample size.

The researchers gave it a name: automation expectation. It is the orientation users bring with them before they ever touch your product. By the time they get to your AI, they have already learned from every other AI tool they have used that the deal is simple: hand off work, receive a result. When your product asks them to do something different, they push back, because the muscle memory is not there.

This is not the same as automation complacency, the older idea about people trusting a reliable system too much over time. Automation expectation is more like a pre-existing condition. The user has already decided how the interaction is going to go before you ever meet them.

If you stop the analysis there, the easy conclusion is that the users are the problem. Train them. Onboard them harder. Add a tooltip.

The paper does not stop there, and neither should we. The same users did engage with the reflective interaction in the structured sessions, and did find it valuable, and did say they would adopt it. What was different about the structured session was not the interface.

It was the sixty-minute calendar block. It was the accountability of sitting with researchers who would ask follow-up questions. It was the shared understanding that reflection was the point of the exercise, not an obstacle to getting back to the backlog.

Remove those three things, and the product becomes unusable even though the product is identical.

I have argued in a few previous pieces that the modern PM is not a bridge anymore. The job has expanded to include a second product that sits alongside the AI itself: the supervisory system around it. The paper does not use that phrase. It does name every piece that belongs to one: bounded commitment, research accountability, contextual timing, organizational reinforcement. How users know what the AI is doing. How they intervene when they need to. Whether the workflow around the AI actually supports the engagement the AI was designed to invite.

The Stankowski paper is the clearest empirical example I have seen of what happens when only the first product gets built. The AI performed well under structured evaluation. The supervisory system around it existed only inside a sixty-minute research session, and nobody had built a version of it into the production environment. When the session ended, the conditions that made the AI usable ended with it.

Here is the part the paper gestures at but does not quite say out loud. The supervisory system is not a UX problem, or at least not only one.

The three things the structured session supplied, bounded time, external accountability, a frame that reflection was the point, are organizational design. They come from how the company schedules work, how it evaluates people, and what it rewards them for producing. You cannot replicate those at the interface layer without also changing what your organization counts as valuable. You can add tooltips. You can timebox the interaction. You can surface a progress bar that shows cognitive outcomes. None of those substitute for an organization that actually pays people to think.

There is one other finding worth pulling forward. The paper asked participants to choose which dimension of their goals to work on. One option, Adaptable, was selected by only five out of fifteen. It was not a popular choice. When users did pick it, that dimension produced the highest rate of genuine new insight in the entire study, at ninety-two percent. The users who needed it most were the least likely to pick it. That is the product problem in miniature: people cannot reliably choose the experience that will help them most, because they cannot see its value in advance. Leaving the choice entirely to the user systematically under-deploys the features that justify the tool.

This is why I get suspicious when the prescription stops at "design smarter environments." It is softer than what the data suggests. The environment that matters is the incentive structure, and incentive structures are changed in quarterly reviews and compensation plans, not in product design sessions.

The PMs who will do well in the next few years are the ones who stop treating the supervisory system as a polish step at the end of a feature and start treating it as real work that belongs in the roadmap next to the model, the integrations, and the latency budget. The ones who will do very well are the ones who understand that when the organization is not cooperating, the product's job is to make that visible rather than pretend it can be papered over with a better screen.

Ninety-three percent is a real number, and it is a real warning. The lab is a beautiful lie. The real question is not whether you can build an AI users love in a controlled demo. The real question is whether the environment you are deploying into rewards the behavior your product requires.

Where technology meets people, the people bring their whole environment with them. And the environment wins.

---

*Reference: Stankowski, A. (2026). "Expecting Automation: How Users Miss Valuable Experiences in Generative AI." AutomationXP26 Workshop at the 2026 CHI Conference on Human Factors in Computing Systems, Barcelona, Spain. Research funded by SAP in collaboration with DFKI.*
