---
title: "Earn Your Way Out of the Loop. Then Show the Receipt."
slug: earn-your-way-out-of-the-loop-then-show-the-receipt
published_at: 2026-07-18
custom_excerpt: "The Claude Code team ships most of its code through an agent that acts on its own. The six lessons everyone is copying are real. But in a regulated enterprise, earning your way out of the loop only counts when the receipt is an audit trail, not one person's memory.  "
tags: [agentic]
feature_image: https://storage.ghost.io/c/e6/05/e605b234-3cc8-4fe4-97bb-2bb55b18b8fb/content/images/2026/07/ChatGPT-Image-Jul-18--2026--04_01_37-PM.png
source: ghost
---

# Earn Your Way Out of the Loop. Then Show the Receipt.

An AI agent merges 65 percent of one Anthropic team's pull requests. Nobody prompts it to start.

That number spent the week traveling around my feed, usually attached to a tidy list of lessons about how software gets built now. The lessons trace back to a fireside chat Simon Willison hosted with Cat Wu and Thariq Shihipar from the Claude Code team. I went back to the source, because the version circulating had quietly acquired specifics the speakers never said, and because the real account is more useful than the summary.

Here is what was actually said. The 65 percent is not a lone coder with a fast autocomplete. It is Claude Tag, the team's Slack-native agent that Cat Wu calls the evolution of Claude Code. It is "multiplayer by default" and "proactive instead of reactive." You point it at a channel, it watches for events like a bug report, and it opens the pull request and tags the right engineer on its own. Internally it merges 65 percent of their product engineering team's PRs. Thariq Shihipar described the human side as a delegation curve that moved with each model generation: from reviewing every permission prompt to stepping back and handing off the menial implementation. The scarce skill, he said, has flipped from execution to product sense, deciding what is worth building. Rewrites stopped being taboo because a codebase is a spec, often the only copy of the spec you have. System prompts got shorter, moving away from over-constraining the model with examples. And Cat Wu named the thing AI still cannot do: taste, the design judgment that turns a correct output into a good one.

Every one of those observations is real. I have watched versions of all of them in my own work. The lessons are not wrong. They are just reported from a specific room, and the room does most of the quiet work.

## The room, not just the lesson

The room in that talk is a small team of expert engineers, shipping software where a bad merge is caught by a test suite and rolled back in minutes. The reviewer grew up writing the code by hand, so their pattern recognition is intact. The consequences are recoverable. The person who earned the trust in the agent is usually the same person still holding the loop next week.

Change any one of those conditions and the lessons hold but the assumptions underneath them break. I build data and AI products in enterprise and regulated settings, where the blast radius is larger, the reviewer may never have done the underlying work by hand, and the outcome touches a customer, a patient, or a balance sheet. This is the translation the six-lesson summaries skip, and it is the whole job.

## Earned, not scheduled

"You earn your way out of the loop" is the best line in the talk, and it is exactly right. Trust in an agent should be collected like a receipt, not taken as a leap. I have written before that autonomy should be earned, not scheduled: you move an agent up the ladder from suggesting to acting because it has demonstrated competence in the specific failure modes that matter, not because it has crossed a review count or a go-live date.

But in a team, and especially in a regulated one, that receipt cannot live in one person's head. The engineer who spent six weeks watching where the agent caught every mistake has built a private, unwritten model of when to trust it. The moment they go on leave, change teams, or hand the workflow to someone more junior, the receipt is gone and the autonomy stays. What earned the trust was tacit. What inherited it is exposed.

So the enterprise version of "earn your way out of the loop" has a second clause the solo version does not need. The receipt has to become an audit surface: a reconstructable record of what the agent did, under what authority, and who carries the outcome. That is one of the four design artifacts every agentic product needs whether or not anyone designs it. Underbuild it and you get the worst pairing available: an agent acting with autonomy nobody can account for, reviewed by a human whose trust nobody can transfer. The receipt is not paperwork you add after the fact. It is the thing that lets the next person take their hands off the loop safely.

## "Use your judgement" is a governance decision

One of Simon Willison's takeaways was to stop dictating how the model works and let it use its own judgement. Instead of a rule like "only write tests for larger features," you tell the model to decide for itself when a test is warranted. For a solo developer burning through a token budget, that is a smart efficiency move, and it points at something deeper that Thariq confirmed: shorter prompts, less over-constraint, more context, produce better work. Rigid rules break on the case sitting in front of them. Context beats rules.

I agree with the mechanism and I want to be precise about what it costs. In an enterprise, "use your judgement" is not a prompt-engineering preference. It is a delegation of authority, and delegated authority without a boundary is scheduled autonomy wearing a friendlier word. The same instinct that makes the model better, giving it your context instead of your restrictions, is also the instinct that makes it accountable, because that context is the audit trail. The configuration file where you write down how your team actually works is doing two jobs at once. It is the agent's onboarding packet, and it is the record of what "good" was supposed to mean when something later goes wrong. If your team has not written that file, your product is being shipped by a worker you never onboarded, and "it used its judgement" is not an answer you can give a regulator.

## Taste has to become legible

The third lesson is the one I think matters most, and it is where Cat Wu and the summaries actually agree. When execution gets cheap, the scarce skill becomes taste: knowing which thing is worth building at all. Cat Wu's own frontier is the same coin from the other side, the observation that models can follow a detailed spec but still cannot produce delight. Taste is the bottleneck now.

Here is the part that does not survive the move from a solo shop to a team. One founder's instinct about what is worth building is a competitive advantage precisely because it lives in their head. Inside an organization, that same instinct is a single point of failure. If "which thing is worth building" is something only the smartest person in the room can feel, the agent cannot act on it and the team cannot scale it. Taste has to become legible: written down, argued in the open, encoded where both the team and the agent can read it. The uncomfortable implication is that the skill everyone is now told to develop, taste, only becomes an organizational asset when you do the unglamorous work of making it explicit. Otherwise you have automated the doing and left the deciding trapped in one person.

## The lesson transfers. The room does not.

The Claude Code team showed a real and near future, and they were honest about the conditions that made it work. The trouble is not in what they said. It is in what gets stripped when the story is retold: the small team becomes any team, the recoverable consequence becomes any consequence, the expert reviewer becomes any reviewer, and the private receipt becomes proof.

Earn your way out of the loop, yes. Then show the receipt, because in a room where the outcome matters and the reviewer might not be you, the receipt is the product. Let the model use its judgement, yes, once you have decided how much authority you are delegating and where the record of that decision lives. Develop taste, absolutely, and then take the harder step of making it something other than a feeling. This is the work at the place where technology meets people. The demo is the easy half. The system that lets a stranger trust it next week is the half that does not fit in a list.


---

*This article is part of an ongoing series on AI product design, healthcare data, and the human side of technology adoption.*

*Sources: the fireside chat (Simon Willison with Cat Wu and Thariq Shihipar, AI Engineer World's Fair); Simon Willison, "Fable's judgement" (simonwillison.net, 3 July 2026); StartupHub.ai write-up of the talk (15 July 2026).*
