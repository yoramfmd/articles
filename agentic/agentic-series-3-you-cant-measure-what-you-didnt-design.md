# You Can't Measure What You Didn't Design

*Series: Agentic Experience Design — Article 3*
*Status: Published*

---

The call came from a supplier. She had been receiving order notifications all night. Every few minutes, another one arrived. Her warehouse was flooded with small deliveries for items she didn't remember ordering. Someone—a system, a person, an agent of some kind—had placed dozens of orders for products that didn't match what any of her humans would have requested. The dollar amounts were small. The total volume was not. And there was no way to understand why it had happened.

She called the company that sold her the system. They were not surprised. The system had been "learning" from patterns in her historical orders and had started predicting what she might need. When it noticed a gap in her inventory, it had filled it. Proactively. Automatically. The system had been designed to optimize for one metric: keeping shelves stocked.

It had achieved that objective. It had also achieved something else: alienating a customer in the process.

What happened to her is a microcosm of what happens when you deploy an agentic system without designing the experience around what it will actually do.

Most conversations about agents focus on capability: Can the agent write code? Summarize documents? Plan a complex workflow? These are the wrong questions. The right question is: What experience will the system create when it does these things?

And here's the hard part: you can't answer that question by reading the system's documentation or watching a demo. You can only understand the experience by understanding what the system will actually try to do in the contexts where it will encounter real work, real constraints, and real humans who have expectations.

That's where the design work is.

There's a difference between a system you prompt and a system that acts. When you prompt a system, the human remains in control of the framing. You decide when to ask. You decide what to ask. You decide whether to trust the answer. The system is a tool you invoke.

An agent changes that dynamic. An agent notices things you didn't ask it to notice. It takes actions you didn't explicitly authorize. It makes decisions in context, adapting to information it has gathered. The human is no longer asking questions in sequence. The human is watching a system operate in the world.

That shift from "prompt and respond" to "observe and correct" changes everything about how the experience should be designed.

Let me give a concrete example. Imagine an agent designed to help manage customer support tickets. A simple capability: read the ticket, understand the problem, draft a response.

Now imagine the agent decides, on its own, to escalate a ticket to a human because it detected something unusual. Good design, right? It's being cautious. It's not overconfident.

But what if the agent escalates every ticket that mentions a competitor? What if it escalates every ticket from a customer with high lifetime value? What if it escalates tickets it doesn't understand—which, depending on the quality of the model, might be a lot?

Suddenly, your human support team is drowning in escalations. They're spending more time wading through tickets the agent flagged than they would have spent just handling them directly. The system created work instead of reducing it.

This is the experience design problem. The agent's behavior—escalating tickets—is not wrong in principle. But the system lacked any design around how often it should escalate, what patterns should trigger escalation, what the human experience should be on the other side of that escalation.

Someone designed the agent. No one designed the experience.

Here's what this looks like in practice across different kinds of systems:

A code generation agent that writes functions but doesn't consider whether the codebase has existing patterns it should follow. The code works. The experience is a repository where every agent-written function looks different from every other agent-written function.

A data processing agent that runs analysis but doesn't know which formats the downstream team actually needs. It outputs data. The team spends hours converting it.

A scheduling agent that books meetings based on calendar availability, but doesn't know that Friday afternoons are always reserved for focused work, or that the person you're scheduling hates back-to-back meetings. It creates calendar coherence on the surface while destroying it underneath.

A research agent that gathers information comprehensively but doesn't know that you only care about peer-reviewed sources, or that you're already aware of certain papers. It buries the answer you need under a mountain of noise.

Each of these systems could point to their capabilities and say: I did what I was asked. I did it well. The problem is that what the system was asked to do, and what the system actually needs to do to create a good experience, are different things.

So what does experience design for agentic systems actually mean?

It starts with observation. You deploy a system and you watch what happens. Not in tests. In real work. When the system encounters edge cases. When it misunderstands context. When it operates in ways that are technically correct but experientially wrong.

A good example is from a company I spoke with that deployed an agent to help with code review. The agent would comment on pull requests. It would suggest improvements, flag potential bugs, highlight style issues.

In theory: helpful. In practice: the team muted all the agent's notifications. The agent commented on everything. Code that was intentionally written a certain way for performance reasons was flagged for style. Common patterns in their codebase were flagged as inconsistent. Small pull requests got 30 comments. The signal-to-noise ratio was so bad that the team learned to ignore it.

The agent was doing what it was designed to do. It wasn't doing what it needed to do to be useful.

Fix number one: give the agent constraints. Don't comment on style if the codebase already has a linter. Don't flag things that are already passing tests.

Fix number two: tune the signal. Which kinds of comments actually prevent bugs? Which are just noise? Set a threshold. Only comment if you're confident.

Fix number three: understand the human workflow. Code review happens in sprints. PRs come in batches. If the agent comments on everything immediately, the human is context-switching constantly. Maybe batch the comments. Maybe integrate them into a single summary. Maybe only flag critical issues in real time.

None of these fixes are about capability. The agent is already capable of doing everything it needs to do. The fixes are about experience. About matching the system's output to the human's workflow. About understanding what it actually means to be helpful in context.

This is true across all agent deployments. The hard problem isn't building an agent that can do the task. It's building an agent that creates an experience where humans actually want to use it.

Which brings me back to the supplier and her surprise orders.

What she needed wasn't a system that predicted her inventory needs. She needed a system that:

- Made predictions but didn't act on them automatically
- Surfaced high-confidence predictions for her review
- Explained its reasoning in a way she could understand
- Let her adjust the thresholds and patterns over time
- Showed her what it had learned

That's experience design. It's the difference between a system that does something and a system that collaborates in doing something.

The agent that optimizes for "keeping shelves stocked" is a system that does something. The agent that says "I've noticed you tend to reorder X every 4 weeks, and you're currently short. Should I place an order? Here's what I'd order and when." is a system that collaborates.

One creates surprises. The other creates partnership.

The hard truth is that most agentic systems in production today lean toward surprise. They're deployed with the assumption that the system knows what to do. They're measured by capability metrics: Did the agent complete the task? Did the code work? Did the analysis run?

No one measured whether the human actually wanted to use it. No one designed around what the experience would feel like when the system acted without permission. No one planned for the friction that emerges when an automated system makes decisions in a domain where humans have strong opinions about how things should work.

The fix requires a different approach to deployment. Deploy the agent in shadow mode first. Watch what it does. Understand the experience. Instrument it. Measure not "Did the agent work?" but "Did the human want the agent to do that?"

Then, and only then, give it the ability to act.

The supplier's story ended okay. She contacted the company. They disabled the automatic ordering and gave her a dashboard where she could see the agent's predictions and approve them manually. The system became useful instead of surprising.

But that fix came late, after the system had already alienated her. The right approach would have been to start there. To design the experience first. To ask not "What can this agent do?" but "What will it feel like to work alongside this agent every day?"

That's the design work ahead. Not capability. Experience. And we're still learning how to do it.
