# Do No Harm, Encoded

### Why Healthcare Needs an AI Constitution

**In 1942, Isaac Asimov wrote three laws.**

A robot may not injure a human being, or through inaction, allow a human being to come to harm. A robot must obey orders, except when they conflict with that first rule. A robot must protect its own existence, unless that conflicts with the first two.

Asimov was writing science fiction. He was also thinking more rigorously about machine ethics than most of the healthcare industry has in the eighty years since.

He understood that constraining intelligent systems requires a hierarchy of non-negotiable rules, not a list of suggestions. The first law must always override the second. Helpfulness must always yield to safety. Those constraints must be built into the system, not left in a policy document nobody consults when the model runs. In that sense, Asimov's three laws were never just rules. They were constitutional-level directives: foundational, hierarchical, and impossible to override in the name of convenience or optimization.

Asimov also understood the limits of his own framework. He spent decades writing stories about what happens when the three laws fail, not because the laws were wrong but because encoding ethics as rules, however carefully designed, always encounters reality in ways the rules did not anticipate. He was not arguing against the laws. He was arguing for taking them seriously enough to study their failures.

We are deploying AI into clinical settings at scale. We have not built the equivalent of Asimov's three laws for healthcare. The consequences of that gap are already visible.

### The Oath We Took and the One We Didn't

Before I was allowed near a patient, I took an oath.

Not a compliance training. Not a policy acknowledgment. An oath. A public commitment, in front of colleagues and faculty, to place the wellbeing of the patient above everything else, to do no harm, *primum non nocere*, to respect autonomy, to act within the boundaries of my competence, and to escalate when those boundaries were reached. That oath was not enforced by a supervisor watching my every decision. It was internalized. It became part of how I reasoned before I acted.

The Hippocratic tradition is not perfect and it is not static. It has evolved over centuries to reflect changing medical ethics and patient rights. But at its core it represents something important: a domain-specific ethical constitution that every practitioner carries into the room, that operates at the moment of decision, that cannot be switched off when it becomes inconvenient.

Now consider the AI systems being deployed into those same decisions. They did not take an oath. They went through regulatory review, safety testing, validation on curated datasets, and compliance sign-off. All of that matters. None of it is the same thing as a constitution that operates at runtime, at the moment a recommendation is generated.

We have a two-tier system. Human clinicians carry an ethical invariant into every decision. The AI systems working alongside them do not. That asymmetry should bother us more than it does.

### What We Have and Why It Is Not Enough

Healthcare has ethics. Healthcare AI has governance. They are not the same thing.

The WHO, AMA, National Academy of Medicine, and frameworks like FUTURE-AI have all produced serious guidance on ethics and governance of AI in health. These are genuine efforts and they deserve credit.

But they share a structural limitation. They are design-time and deployment-time frameworks. They govern how AI is built, tested, approved, and monitored.

They do not sit between the model's reasoning and its output and ask, right now, before this reaches a patient: does this recommendation violate a non-negotiable principle?

The gap is not ethical thinking. The gap is enforcement at the moment it counts. A physician who is rushed, under pressure, or having a bad day still carries the oath. It does not switch off. An AI system operating under the same conditions has only the guardrails set during development, which may or may not be calibrated for the specific clinical situation it is now facing.

### Constitution Is a Concept, Not a Document

Before going further it is worth being precise about what a constitution means in this context.

Asimov offered one version: a small, hierarchical set of absolute rules. The three laws are the right architecture. They are not sufficient engineering.

Most responsible AI frameworks offer another version: broad ethical principles. Do no harm. Respect autonomy. Preserve equity. Operate transparently. These are value statements that require interpretation. They guide design decisions. They do not operate at inference time.

Neither is sufficient alone. Healthcare needs both, structured as two distinct layers.

**Layer one: ethical principles.** The non-negotiable values that cannot be traded away regardless of context. They define what the system is for and what it is never permitted to optimize against.

**Layer two: enforced constraints.** The runtime rules that translate those principles into architecture. No autonomous high-risk decision without human confirmation. No output beyond validated clinical scope. Mandatory uncertainty disclosure when data is incomplete. Escalation when risk threshold is exceeded. No optimization logic that overrides clinical safety requirements.

The principles tell you what you believe. The constraints tell you what the system is actually required to do before it is allowed to speak.

Most current frameworks have layer one. Almost none have layer two in a form that is clinically grounded and enforced at inference time.

One further complication worth naming: a constitution for mental health AI does not look identical to a constitution for oncology AI or emergency triage. The ethical core is shared. The constraint layer is not. Mental health AI serving patients in crisis requires an escalation bias that would be paralyzing for a dermatology classifier. A healthcare AI constitution is not one document. It is a framework for building domain-specific constitutions, each with the same ethical principles and tailored runtime constraints.

### The Closest Thing That Exists

The closest existing implementation was not built for healthcare.

Anthropic has been developing constitutional AI since 2022. Its published constitution defines an explicit priority order: broadly safe first, broadly ethical second, compliant with guidelines third, genuinely helpful fourth. Safety always beats helpfulness. In 2025 it introduced Constitutional Classifiers, a runtime enforcement layer that screens outputs before they reach the user. Think of it as the system asking itself, before responding, whether the output violates a non-negotiable principle, and refusing to proceed if it does.

The rules being enforced are not universal. Asking how to build a nuclear weapon triggers a hard block regardless of context. A question involving violence is handled with more contextual reasoning, distinguishing a thriller writer from someone expressing clear intent to harm. The same logic applies to healthcare: "do no harm" in clinical triage means never tell a patient with signs of respiratory failure to wait at home. The mechanism is the same. The domain-specific rules are not, and that is precisely the work that remains to be done.

Anthropic released its constitution under a Creative Commons CC0 license, meaning anyone can build on it freely. The mechanism exists. The healthcare-specific version does not.

### What a Constitution Would Have Caught

A study published in Nature Medicine in February 2026 tested ChatGPT Health against 60 structured clinical scenarios across 21 specialties. The system under-triaged 52% of genuine medical emergencies. In one case involving early signs of respiratory failure, the model identified the danger in its own explanation and still advised the patient to wait. In suicide risk scenarios, crisis alerts fired more reliably when patients described no specific method than when they described exactly how they intended to harm themselves.

These are not knowledge failures. In the respiratory case, the model knew. It articulated the risk and then ignored it in its output. That is a constraint failure. A runtime layer asking does this recommendation increase risk to the patient would have blocked that answer before it reached the user.

The suicide result is a direct analogue to Asimov's first law. A simple enforced rule, specific method disclosure triggers mandatory escalation regardless of other factors, would encode the constraint clinically: the system may not, through inaction, allow a human being to come to harm.

The model had the information it needed. Nothing was architecturally required to act on it.

### The Challenge

I want to be precise about what I am and am not arguing.

I am not proposing a specific healthcare AI constitution. A framework written by one person is an opinion. A framework developed through consensus across AMA, WHO, NAM, clinical informatics societies, AI developers, patient advocates, and ethicists across specialties and jurisdictions is something worth enforcing. Those are not the same thing, and I am not the right author.

The absence of a runtime-enforced ethical constraint layer in healthcare AI is a structural gap that no amount of governance documentation or post-hoc safety monitoring will close.

The organizations with the legitimacy to close that gap know who they are. The AI companies deploying into healthcare have already demonstrated that the mechanism exists and works. Anthropic released the framework for anyone to build on. The clinical and ethical communities have the domain knowledge to extend it. The open question is not whether this is possible. It is whether the urgency is felt.

Every physician who graduated from medical school took an oath before they were allowed near a patient. We did not consider that optional, or too abstract to operationalize. We considered it the minimum requirement for someone with the power to cause harm.

Healthcare AI has that power. It does not yet have the equivalent requirement.

That is the work ahead: not writing a perfect constitution, but building a framework rigorous enough to catch the cases that matter most, humble enough to acknowledge what it does not know, and honest enough to escalate rather than guess when a patient's life is on the line.

Clinicians take an oath requiring all three of those things before they are allowed into a clinical setting. That is not too high a bar. It should not be too high a bar for the systems working alongside us now.
