---
title: "The Sixth Archetype Anthropic Forgot"
slug: the-sixth-archetype-anthropic-forgot
published_at: 2026-07-03
custom_excerpt: "Anthropic mapped product work into five archetypes: Prototyper, Builder, Sweeper, Grower, Maintainer. All five stop the moment the thing ships. But an agent keeps deciding after you let go of it, and there is a sixth archetype no one drew: the one who watches it decide."
tags: [pm, agentic]
feature_image: https://storage.ghost.io/c/e6/05/e605b234-3cc8-4fe4-97bb-2bb55b18b8fb/content/images/2026/07/ChatGPT-Image-Jul-3--2026--08_19_05-AM.png
source: ghost
---

# The Sixth Archetype Anthropic Forgot

*The discourse found the new skill. It put it at the wrong end of the pipeline.*


---

There was a time when photography was a planned profession. Film gave you thirty-six frames, each one cost money, and none of them existed until a lab developed the roll days later. So the work happened before the shutter. You scouted the location, waited for the light, composed the frame in your head, and spent the shot only when the picture was already made. Scarcity forced planning, and planning was the craft.

Digital removed the scarcity. A frame costs nothing now, so you do not plan the one shot; you take a thousand and throw away nine hundred. The craft did not disappear. It moved. It went from planning the picture to choosing among the pictures, from the setup to the edit. The photographer with an eye still gets the keeper. The amateur with the same camera gets a thousand mediocre frames and no way to tell which one is good.

Product work is having its film-to-digital moment, and the people closest to it have named the new skill well.

## The craft moved to the edit

Boris Cherny, who built Claude Code, posted a small framework that has been passed around all week. As engineering, product, design, and data science melt together, he argues, job titles stop meaning much, and what is left is five archetypes: the Prototyper who churns ideas, the Builder who makes them production-grade, the Sweeper who simplifies and unships, the Grower who pushes toward fit, the Maintainer who keeps a mature system alive. They cut across function, not along it. At Anthropic everyone holds the same title and everyone codes, so the archetype, not the badge, tells you what a person actually does.

Aakash Gupta gave the underlying skill a name: taste at speed. Evaluate working software fast, kill most of it, ship the survivors. He is careful to call it a filtering function, not an acceleration function. The eighty percent kill rate is the point. Without taste, speed just means building the wrong thing faster. And in a sharp response, the writer paddo added the line that holds the whole thing together: agents add, they do not subtract. A model will generate a hundred versions, but knowing which one should exist is judgment it does not have. Delegate the toil, keep the taste.

All of this is right, and it is the photography shift exactly. Building got cheap, so the craft moved from planning the shot to choosing the frame. The lineage is older than the AI framing, as paddo notes: Cringely split teams into commandos, infantry, and police in 1992; Wardley into pioneers, settlers, and town planners; Thiel into zero-to-one and one-to-n. What is new is only that lifecycle phase, once the secondary axis, became the primary one. When the camera is free, the eye is the whole job.

And the culling itself is not new, only its position. The industry spent twenty years learning that you cannot plan your way to a good product, you find it by throwing most attempts away. Lean Startup made a virtue of it. A/B testing industrialized it, shipping forty versions of a button to live traffic and keeping the one that won. But all of that culling happened after the thing shipped, paid for in engineering hours and read off a dashboard as user data. What the cheap prototype changed is the cost and the position: the cull moved upstream, off the live product and onto the contact sheet. You no longer ship an MVP to a thousand users to learn it was the wrong idea. The agent generates a hundred versions on Tuesday, and taste kills ninety-nine by Wednesday, before a user sees one.

I have no argument with any of it. I want to point at the thing it leaves out, because the same people who named the new skill put it at the wrong end of the pipeline.

## You do not ship the photo. You ship the photographer.

Every archetype in that list acts on software up to the moment it ships. The Prototyper explores, the Builder hardens, the Sweeper trims, and taste at speed is the judgment that picks the frame before the client ever sees the contact sheet. It is all build-time work. It ends at the shutter.

A photograph is inert. Once you choose the keeper, it is finished; it will never take another picture. And this is the point where an agentic product stops behaving like a photograph. You do not ship the photo. You ship the photographer.

An agent keeps deciding after you release it. It shoots at weddings you are not attending, composes in the room, in real time, on a day no one can re-run. Shipping it is not choosing the best of a thousand frames. It is hiring an eye you will not be standing behind, and then living with the pictures it takes when you are not there. Taste at speed cannot reach that moment, because there is no prototype to kill. There is a live agent making the call, and a client who still holds you responsible for it.

This is why the printing-press analogy Boris likes, cheap printing that ended the scribes and created the authors, only takes you halfway. A printing press is a tool. It prints what you set and nothing else. A photographer is an agent: they exercise judgment when you are not there. The press can carry *building got cheap*. Only the photographer can carry *you delegated the taste*.

## The sixth archetype

So there is a sixth archetype, and it is not on anyone's list.

Taste at speed is the photographer culling the shoot before the client sees it. The sixth archetype is the photo editor who reviews that photographer's work across every future assignment, not once at hiring, but shoot after shoot, because now someone else's eye is choosing the keeper and the consequences are still yours. Call it the Supervisor. Its job is not to build the agent or to pick the best version of it before launch. Its job is to watch the released agent decide, catch the wedding where it framed the shot wrong, and stop the picture before it goes to print. Swap the wedding for a loan decision, a triage queue, a non-refundable booking, and the shot prints the instant the agent takes it, with no editor in the room.

Notice what is strange about this archetype. It has no thirty-year lineage. Cringely did not need it, Wardley did not need it, Thiel did not need it, because in every prior version of the pipeline the thing you shipped held still. The Supervisor exists only when a teammate is probabilistic, when the product keeps making judgment calls after you let go of it. It is new for precisely the reason the whole category is new. You cannot find it in the old frameworks because the old frameworks never had a member of the team who was not a person.

The closest the old world came was the A/B test, and the gap is the whole point. An A/B test watched the shipped product too, but it watched a number, click-through, conversion, retention, and culled by data anyone could read off a dashboard. The Supervisor watches a judgment, the call the agent just made in a room no dashboard was pointed at. You can automate watching a number. Watching a judgment is the taste the discourse just moved to build time, needed again at run time, where it is harder to get and no one has staffed it.

## Why the map leaves it out

There is a reason the most-shared "future of roles" posts of the month describe everything around this seat and never name it. The people drawing the maps are builders describing build work. Their world is prototypes and pull requests and the judgment that gets exercised before the ship gate, and from inside that world the supervision of a running agent is not a role, it is an afterthought that belongs to someone else.

But supervision has never fit the categories we already have. A new hire has HR. A contractor has procurement. A vendor has vendor management. A running agent making unattended decisions fits none of them, so it falls to whoever built it, which means the builder is grading their own homework at the exact moment the stakes go live. The seat that should hold it has not been drawn on the org chart yet. That is not negligence. It is a category the industry has not built yet, showing up as a blank space in the map everyone is sharing.

## Function melts at build, and hardens at run

The strongest claim in the discourse is that function dissolves entirely, that the engineer and the PM and the designer collapse into one person directing agents, and that soon everyone is a builder. Half of that is true, and the half that is true is the half you can see.

At build time, function does melt. One fluent person can run all five archetypes, take the idea, prototype it, harden it, trim it, because the agent absorbs the toil inside each one. That is real, and it is happening.

At run time, function hardens again, and it hardens for a reason the build-time view cannot see. The whole value of the Supervisor is that they are not the builder. A photographer cannot be their own editor at the wedding they are shooting; the eye that made the picture is the last one that can judge it clean. The moment you need someone to catch the agent's bad call in production, you need someone whose judgment is independent of the person who shipped it, and independence is a role boundary, the oldest one there is. The agentic team is not post-role. It is role-melted on the channel that builds the agent and role-split on the channel that watches it. Anyone who has run a bank knows the shape: the people who validate the models do not report to the desk that runs them, because supervision that answers to the thing it supervises is not supervision.

## The keeper is not the last decision anymore

Film taught a generation of photographers that the decisive moment was the shutter. Digital moved it to the edit. The archetype discourse is the record of product people learning the same lesson: when building is free, the work is choosing.

But an agent moves the decisive moment one step further than the edit, past the ship gate, into every unattended call it makes on your behalf after you have stopped looking. The keeper is no longer the last decision you make. It is the first of many the agent will make without you. Someone has to be the eye on that work, shoot after shoot, and it cannot be the person who took the picture.

That seat is the whole subject of the book I just finished, which asks one question across three hundred pages: who owns what when the software acts on its own. The five archetypes describe the team that builds the agent. The sixth describes the team that survives it.


---
