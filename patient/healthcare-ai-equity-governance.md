# The Patients Healthcare AI Was Not Built For Are Now Its Most Frequent Users

I have spent most of my career as a product manager at enterprise companies including SAP, Microsoft, and Walmart. Across every industry and every product, one lesson has held: data is the foundation of everything. But there is a caveat that gets skipped more often than it should. The data only works if it comes from the right people.

If I am planning a new manufacturing and logistics platform for a boutique craft brewery, I do not go interview Budweiser as my primary source of data. Their workflows, their scale, and their needs are fundamentally different from the customers I am designing for. The data I collect will be accurate. It will just be wrong for the product I am building.

A new KFF poll, published March 2026, suggests that healthcare AI made exactly this mistake, at scale, and that the consequences are now visible in the data.

---

## The Data Does Not Match the User

About 1 in 3 Americans used AI for health information in the past year. That number looks like adoption progress until you ask who is driving it.

Uninsured adults are twice as likely as insured adults to use AI for mental health advice. Among AI health users ages 18 to 29, 38% cited not having a provider or not being able to get an appointment as a major reason they turned to AI. Among AI health users with household incomes under $40,000, one-third cited cost as a major reason they used a chatbot instead of a doctor. Black and Hispanic adults are using AI for mental health information at higher rates than White adults.

These are not early adopters experimenting with technology. These are people who have been failed by the healthcare system and are using whatever is available to fill the gap.

Now consider who shaped the consumer and clinical AI products they are using. Most were developed, validated, and refined through research and data drawn predominantly from insured patients with consistent access to care. Those are the patients whose records appear in electronic health record systems. Those are the users who appeared in early usability studies and adoption cohorts. Those are the people who shaped what these models learned health questions look like and what a useful health answer sounds like.

Budweiser was interviewed. The craft brewery never got a call.

The populations now relying on healthcare AI most heavily present differently. Their health conditions reflect different social determinants and disease burdens. Their relationship to the healthcare system, shaped in many cases by generations of inadequate or harmful care, is largely absent from the research and data that built these tools. A 92% satisfaction rate across all users can coexist with significant failures at the demographic level, because satisfaction is self-reported by people with no baseline for comparison. If AI is your only source of health information, you may not know what a better answer would have looked like.

---

## A Pattern That Was Already Named

This is not a new problem. There is a documented pattern in health technology adoption called the inverse equity hypothesis. New interventions tend to reach more advantaged groups first, delivering early benefits to the populations least in need, with gaps widening before diffusion eventually narrows them.

A recent JAMA Health Forum editorial raised concern that clinical AI in medicine risks following this same pattern. Early deployment is concentrating in academic medical centers and well-resourced health systems. Safety-net institutions and rural hospitals are largely watching from a distance. The patients who carry the highest burden of chronic disease, who have the most to gain from AI-assisted care, are last in line for clinically supervised AI.

The KFF data adds a complicating layer. Consumer AI has created a parallel track that no health system planned for. Underserved populations are not waiting for the academic medical center to complete its AI rollout. They are using ChatGPT, Gemini, and Claude on their phones, right now, to look up symptoms, interpret lab results, and decide whether something is serious enough to justify the cost of a visit. Consumer AI has filled part of the access gap without being designed for the people most likely to use it under pressure, and without being validated on them.

---

## The Governance Gap

Clinical AI deployed inside regulated health systems has at least a framework for accountability. FDA guidance on clinical decision support tools, HIPAA requirements, institutional review processes, and the presence of a licensed clinician in the loop all create some structure, even if imperfect.

Consumer AI used for health advice largely operates without equivalent structure.

When an uninsured 24-year-old uses a general-purpose AI to interpret abnormal lab results and decides not to follow up with a doctor, accountability is diffuse and often unclear. No one configured the tool for this use case. No one validated it on this population. The mechanism connecting an AI output to a downstream health decision, and that decision to any outcome, is absent. Responsibility for what happens next is difficult to locate.

The KFF data found that 42% of people who used AI for physical health information did not follow up with a doctor. For mental health, 58% did not follow up with a professional. For a significant share of users, the AI interaction is not a step in the care process. It is the entire care process.

The question I apply to every AI product I work on is: who owns the decision when the system gets something wrong, and what happens to the person affected? For consumer health AI, that question does not yet have a clear answer.

---

## The Privacy Paradox

Seventy-seven percent of adults say they are concerned about the privacy of personal medical information shared with AI tools. That concern is consistent across age groups, including among people who actively use AI for health. It is not a knowledge gap. People understand the risk.

Yet among those who used AI for health information, 41% uploaded personal medical data, including test results and doctor's notes. Among adults 18 to 29, nearly 1 in 5 of all adults in that age group has done this.

From a product standpoint, this is not a consent problem. It is a constraint problem. When you cannot afford a provider visit, uploading your lab results to an AI and asking what they mean is not reckless. It is the most practical option available. People are making reasonable decisions under unreasonable constraints.

What is not reasonable is treating this as a user behavior question rather than a design and governance question. When people upload protected health information without meaningful informed consent and without clarity on how that data may be used, that is a gap in product design. The obligation to close it belongs to the teams building and deploying these systems.

---

## What Getting This Right Actually Requires

Equity in healthcare AI is not a model card checkbox. It is a sequence of product decisions made at every stage of the lifecycle, and it requires someone to make them deliberately rather than defaulting to the path of least resistance.

It starts with data collection. If the populations most likely to use your product in high-stakes situations are underrepresented in your research, your model has a known failure mode that aggregate accuracy will never surface. The fix is not statistical. It is a sourcing decision. Go talk to the right customers.

It continues with deployment assumptions. Most consumer AI health tools were not designed to be primary care substitutes. They are being used that way regardless. Designing with that reality in mind, rather than for the idealized case of a supplementary tool for an insured, engaged patient, requires a different set of tradeoffs and a different definition of done.

It extends to accountability architecture. Someone has to be responsible for the performance of AI in healthcare contexts, including the consumer contexts that fall outside regulated settings. That accountability cannot be transferred entirely to users who lack the clinical knowledge to evaluate what they are receiving.

And it requires product teams to actively look for the users who do not appear in their analytics. The populations most likely to be harmed by a failure in consumer health AI are the same populations least likely to appear in usability research, least likely to file a complaint, and least likely to be present when roadmap decisions get made. Their absence from the process is not evidence that they are unaffected by the product.

---

## What the Data Is Telling Us

The KFF poll is not a story about AI adoption. It is a story about access failure. AI is filling a void that the healthcare system created and has not solved. The people using it most urgently are doing so because the alternative, a timely and affordable provider visit, is not available to them.

From a product perspective, that is a design and accountability gap hiding inside a utilization metric. The data exists to understand who is actually using these tools and why. The research methods exist to include underserved populations in discovery. The technical capability exists to evaluate demographic-specific performance before launch.

What has been missing is the deliberate choice to use them.

The people who will never be in the room when you design your AI health product are in the data. They are using it now. The question is whether anyone on the product team is treating them as a design constituency rather than an afterthought.

---

*Sources: KFF Tracking Poll on Health Information and Trust, March 2026. JAMA Health Forum editorial on inverse equity and AI in medicine.*
