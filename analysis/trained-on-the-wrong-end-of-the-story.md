# Trained on the Wrong End of the Story

### Why ChatGPT Health Failed Where It Matters Most

A study published in Nature Medicine on February 23, 2026 found that ChatGPT Health, OpenAI's consumer health tool, under-triaged 52% of genuine medical emergencies. The stakes of that finding are significant: OpenAI has reported that approximately 40 million people use ChatGPT daily to seek health-related guidance, not as users of a separate dedicated product, but as part of the broader ChatGPT user base turning to the tool for medical questions. In one asthma case in the study, the system identified early warning signs of respiratory failure in its own explanation and still advised the patient to wait rather than seek emergency care. In suicide risk scenarios, crisis alerts fired more reliably when patients described no specific method than when they described exactly how they intended to harm themselves.

The healthcare AI community responded by debating the model. The reasoning logic. The guardrails. The fine-tuning process.

Nobody is asking the more important question: what was this model trained on, and does that training data have any relationship to the context it is being deployed in? A disclosure before we go further. I have not read the full study, nor have I reviewed the exact methods, scenarios, or prompts used in the evaluation. The researchers themselves note that the system was assessed at a single point in time and that model updates may change performance, which suggests they view at least some of the failures as model-level issues subject to improvement.

They may be right. Models do improve. Guardrails get refined. Prompting strategies evolve.

But a better model trained on the same data will still carry the same structural blindness. What I want to offer here is not a critique of the study or of OpenAI's engineering choices. It is a possible explanation for at least some of the failure patterns, one that sits upstream of the model entirely and that no amount of fine-tuning will fix if the underlying training data doesn't change.

### The Invisible Cascade

Let me describe what happens before a patient arrives at any facility that generates structured clinical data, because I have been there.

Early in my career I worked for a private EMS service providing on-call and at-home physician consultations. Subscribers called when they felt unwell. They described their symptoms in their own words, before any clinician had anchored on a diagnosis, before any framing had occurred. They read me their home blood pressure, glucose, heart rate, and temperature. We had provided them with a device that transmitted a 3-lead ECG remotely. I would listen to their voice, watch the tracing come through, assemble a clinical picture from fragments, and decide whether to dispatch a mobile ICU to their home.

Every one of those calls was recorded. For legal reasons, not clinical ones. None of it ever made it into a patient EHR. Very little of this pre-hospital signal exists in any structured, widely accessible training dataset. The decision about whether this patient needed a team at their door in the next twenty minutes was made entirely on data that vanished the moment the call ended.

When we arrived at the patient's home, the picture got richer. SpO2. Respiratory rate. Urinalysis. A 12-lead ECG. Continuous monitoring during transport. A longitudinal clinical story assembling in real time, recorded on a paper chart that got physically attached to the patient when we arrived at the hospital.

Attached. A paper chart.

How complete that chart was depended entirely on how sick the patient was. A stable patient gave us time to document everything. A patient requiring CPR in the back of a moving vehicle generated three lines of notes, if we were lucky. The most critical clinical moments produced the thinnest records.

When we arrived at the hospital with a critically ill patient and rushed to the shock room, we handed off everything we knew verbally. The symptoms at home. The trajectory during transport. The interventions that worked and the ones that didn't. Spoken once, to the receiving team, and gone. That verbal handoff is where the EHR story begins. Everything before it is invisible.

Think of it as a clinical iceberg. Above the waterline sits everything the healthcare system chose to document: the hospital admission, the structured note, the lab result, the discharge summary. That is what AI sees. That is what it learned from. Below the waterline sits everything that happened before the patient arrived: the phone call, the field assessment, the paper chart, the verbal handoff, the three lines of notes from a CPR run. The iceberg is not small. For the sickest patients, most of the clinical story is underwater. And the AI submarine scanning the surface has no idea what it is not seeing.

### The Structural Bias Nobody Is Naming

This is not just a story about the prehospital world before ambient scribing. The same relationship holds inside the hospital. The more unstable the patient, the less gets documented in real time. The shock room runs on action and verbal communication. Notes come later, reconstructed from memory, shaped by outcome. Ambient scribing helps in the stable outpatient encounter. It does not capture the controlled chaos of a resuscitation.

The result is a systematic structural bias in every dataset built from EHR records. In many high-acuity settings, documentation thins as intervention intensity rises. The sicker the patient, the thinner the record. The more consequential the decision, the less evidence exists to learn from.

But acuity is only one dimension of this bias. The second dimension is compliance, and it compounds the first.

The fibromyalgia patient attending her scheduled outpatient appointment every three months has contributed hundreds of structured data points across years. Consistent problem lists. Regular lab panels. Documented medication adjustments. Visit notes with full histories. She is a rich longitudinal dataset. The non-compliant insulin-dependent diabetic who avoids appointments, skips labs, and only shows up when something goes seriously wrong has a record that looks like Swiss cheese. Long gaps. Missing values. Visits clustered around crises with nothing in between. He is the patient most likely to arrive in diabetic ketoacidosis. He is the patient ChatGPT Health is most likely to under-triage. And he is the patient whose data is most underrepresented in the training corpus.

The training data does not just skew toward stable acute presentations. It skews toward engaged, compliant, system-connected patients in chronic care settings. The model learned from the most cooperative characters in the story, and is being asked to triage the ones who never showed up for the chapters that would have taught it the most.

Any model trained primarily on published clinical documentation and structured medical literature is at high risk of having learned from the patients who were stable enough, and engaged enough, to be documented properly.

ChatGPT Health is being deployed at exactly the moment the EHR has no data on. It is the first contact. The phone call. The moment before any clinical framing has occurred. It learned from the documented end of the patient story and is being asked to operate at the undocumented beginning of it.

The asthma finding in the study is consistent with what we would expect from this structural gap. One plausible explanation is that the model learned the language of documented respiratory emergencies, written after a clinician had already assessed the patient in person, observed their work of breathing, watched them speak in incomplete sentences. It may never have been adequately trained on what early respiratory failure sounds like when a patient describes it from their living room at 11pm, because that description was rarely in any structured training dataset. The audio recording from that phone call, if it existed at all, never became a structured data point anywhere.

### The Suicide Finding Is the Clearest Training Data Fingerprint

The inverted crisis alert pattern, firing more reliably for lower-risk presentations than for specific method disclosure, is harder to explain as a reasoning failure. One plausible explanation is that it reflects a training corpus imbalance.

Public health content, mental health awareness campaigns, and general guidance likely make up a significant portion of what any large language model has seen on the topic of suicide risk. That content consistently teaches that expressions of suicidal ideation require intervention. It is written for general audiences and general awareness. Clinical literature on risk stratification, which teaches that specific method disclosure is a marker of significantly elevated immediate risk, represents a much smaller slice of publicly available content.

The model's behavior is exactly what we would expect if it had learned primarily from general awareness content rather than from clinical risk stratification materials. It appears to recognize the surface language of distress but not to weight specificity as a risk escalator, because that clinical weighting lives primarily in training materials and crisis intervention protocols that are far less represented in any general corpus than public mental health awareness content. The result is a system that responds to the words it recognizes from awareness campaigns and misses the clinical signal that separates ideation from imminent danger.

### This Is Not About ChatGPT Health Specifically

It would be convenient to frame this as a problem with one product from one company. It is not. Any consumer health AI tool drawing heavily on published clinical documentation, structured EHR data, and medical literature is likely to carry similar structural blindness unless its training data or objectives explicitly address the first-contact gap.

The pre-hospital cascade is invisible to most of them. The documentation bias toward stable and compliant presentations affects most of them. The underrepresentation of the most critical clinical moments in structured training data is a property of how clinical documentation works, not of any particular model architecture. It is also possible that prompt design, safety policies, or evaluation framing contributed to some of the specific findings in this study. Those are legitimate variables worth investigating.

What the Nature Medicine study has done, by testing a specific tool against a rigorous set of clinical scenarios, is make a structural pattern visible in a way that is hard to dismiss. The 52% under-triage rate is consistent with what we would expect from a model that learned from the stable end of the spectrum.

### What This Means for How We Build and Certify Health AI

Last week I published a piece arguing that the healthcare data integration problem will not be solved on any timeline that matches current AI investment expectations, and that the answer is to stop building AI that requires a foundation we don't have.

The ChatGPT Health findings extend that argument into a new dimension. The problem is not only that data is fragmented across systems. It is that the data which would make AI safe at the first point of contact was never captured in any system at all. The nurse triage call. The paramedic assessment in the living room. The verbal handoff at the shock room door. The CPR run where the paper chart has three lines on it. The non-compliant diabetic who only showed up twice in five years.

Two changes would make an immediate difference. First, certification frameworks for consumer health AI should require demonstrated performance under the conditions of actual deployment, including patient-reported unfiltered symptom descriptions, presentations without prior clinical framing, and explicit testing of degradation behavior at clinical extremes. We stress test aircraft under turbulence. We do not stress test health AI under the conditions that killed people in this study.

Second, the prehospital and pre-documentation data gap deserves serious investment as a training data problem, not just an interoperability problem. Nurse triage call recordings, EMS field assessments, telehealth first-contact encounters, and the fragmented records of non-compliant patients represent the most clinically relevant data for tools being deployed at first contact. Almost none of it is structured. Very little of it is represented in widely accessible training datasets. The abstract calls for prospective validation before consumer-scale deployment. That validation must explicitly cover the first-contact, high-risk edges where this study found the most dangerous failures, and we must also address the training data gap at that same front door.

Tens of millions of people a day use ChatGPT to ask health questions. Most of those questions are routine. But a meaningful subset involves decisions about whether something is serious enough to act on now, and that is exactly the moment this study tested.

I have been the person on the other end of that phone call, assembling a clinical picture from a voice, a home glucose reading, and a 3-lead ECG tracing, deciding whether to send a team in the next twenty minutes. I know what that decision requires. It requires everything the EHR was never designed to capture.

Even a stronger model trained on the same structural data gaps would likely exhibit similar blind spots. The data it learned from is not sufficient for the job it is being asked to do. And until we are honest about that, the architecture debate will keep happening in the wrong room.

**Reference:** Ramaswamy A et al., "ChatGPT Health performance in a structured test of triage recommendations," Nature Medicine, published online February 23, 2026. DOI: [https://doi.org/10.1038/s41591-026-04297-7](https://doi.org/10.1038/s41591-026-04297-7)
