---
title: The Second Ear
slug: the-second-eye
published: 2026-01-02
excerpt: "When was the last time you trusted a machine with a life-or-death decision? If you've ever had an ECG, the answer is: already. Since 1982, ECG machines have printed automated interpretations, computers reading your heart and offering a clinical opinion long before we called it AI."
url: https://data-decisions-and-clinics.ghost.io/the-second-eye/
---

*From reading the heart's signals to navigating its arteries*

A cardiologist once told me about a close call early in her career. The automated ECG interpretation printed "Normal Sinus Rhythm." She almost signed off. Something nagged at her to look at the actual tracing. Good thing she did. The algorithm had completely missed a dangerous arrhythmia called Wolff-Parkinson-White syndrome, a condition where an extra electrical pathway in the heart can trigger life-threatening rapid rhythms.

The patient was fine. The algorithm was wrong. And legally, the responsibility would have been entirely hers.

That was 2002. Not the age of large language models and foundation models. The "AI" in question was a signal-processing chip inside a machine that most physicians treated like a printer.

In the first article of this series, I traced how radiology moved from hand-coded rules to foundation models that reason across the whole body. Cardiology's story follows the same arc, but with a twist. Here, the algorithms didn't stay on the screen. They moved from interpreting the heart's signals to physically navigating its arteries. And the question of accountability stopped being theoretical long before anyone noticed.

If you want to understand how deeply algorithms are already embedded in medicine, cardiology is the place to look. Not because it's the most advanced, but because it started earliest, and because almost nobody thinks of it that way.

In 1982, Marquette Electronics shipped the 12SL algorithm inside its ECG machines. For the first time, the device didn't just record the electrical activity of the heart; it interpreted it. The machine printed a diagnostic header at the top of the tracing: "Normal Sinus Rhythm," "Left Bundle Branch Block," "Atrial Fibrillation." A computer was rendering a clinical opinion, decades before anyone used the phrase "artificial intelligence" in a hospital corridor.

I remember being amazed as a young medical student in 1994, watching old analog ECG machines spit out a printed diagnosis that was, sometimes, even accurate. It felt like a small miracle. It was also, in hindsight, the beginning of a bargain that medicine is still negotiating: the machine offers a first read, the physician is expected to verify it, and the liability falls entirely on the human regardless of what the machine said.

That bargain works only if the human maintains the skill to catch the machine's mistakes. And that's where the trouble starts.

When every ECG machine prints an interpretation, the incentive to develop your own reading skills quietly erodes. Students and residents spend less time puzzling through waveforms because the answer is already at the top of the page. Instead of working from the tracing to the diagnosis, the learner glances at the header and works backward. The deep pattern recognition that experienced cardiologists carry, the ability to spot a subtle ST elevation or a shortened PR interval at a glance, develops more slowly when a machine is always offering its opinion first.

This isn't unique to ECGs. It's the same dynamic that plays out with every assistive technology. Calculators weakened mental arithmetic. GPS navigation eroded our sense of direction. The tradeoff is always the same: the tool makes the task easier and the human less practiced at the underlying skill.

In medicine, the math is different. A wrong turn because your GPS failed is an inconvenience. A missed Wolff-Parkinson-White because you trusted the machine's "Normal Sinus Rhythm" is a patient who might not go home.

The honest answer is that this tension has no clean resolution. We aren't going to abandon automated ECG interpretation, nor should we. But the cardiologist who caught that WPW in 2002 did so because she had been trained to distrust the header. That instinct, the habit of looking past the algorithm to the raw data, is the real safety net. And it's the one most at risk of disappearing.

Every physician remembers their first stethoscope.

It arrives in the early weeks of medical school, usually in a white coat ceremony or handed out in a lecture hall, and it immediately becomes the most personal piece of equipment you own. You drape it around your neck and suddenly feel, for the first time, like you might actually become a doctor. It is the symbol of the profession in a way that no other tool is. Children draw it when they draw doctors. Patients expect to see it. It signals: this person listens, literally, to what is happening inside your body.

What makes the stethoscope remarkable is how little it changed. René Laennec invented it in 1816, and for two centuries the basic concept remained the same: a tube that conducts sound from the patient's chest to the physician's ear. The materials improved. The design got lighter. Orthopedic surgeons found creative alternative uses for testing reflexes. But the fundamental act, pressing a bell against the skin and listening, was essentially identical whether you were a physician in 1920 or 2020.

Listening to the heart through a stethoscope, a practice called auscultation, was one of the first clinical skills we learned. In the classroom, it seemed straightforward enough. You'd listen to recordings on tape: the normal lub-dub, the whoosh of a systolic murmur, the rumble of mitral stenosis. I could identify them reliably in that controlled setting. The sounds were clear, isolated, textbook.

Then you walked into a hospital room. The patient was breathing. The gown was rustling. Someone was talking in the hallway. The air conditioning was humming. And the subtle murmur that had been so obvious on tape became, for me at least, essentially inaudible. I'll be honest: using a standard stethoscope in a real clinical setting, I don't think I ever confidently heard a murmur on my own. I could hear the heart. I could count the rhythm. But the fine diagnostic distinctions that cardiologists seemed to make effortlessly? Those felt like a kind of magic I hadn't been granted access to.

I suspect most non-cardiologists would admit the same thing if they were being candid. Auscultation was medicine's most democratic skill in theory and one of its most specialist-dependent in practice. The gap between what the stethoscope could reveal to a trained ear and what it actually revealed to the rest of us was enormous.

Which is why what happened next matters so much.

In the mid-2010s, a company called [Eko Health](https://www.linkedin.com/company/eko-health/) did something that hadn't been done in two centuries: they meaningfully changed the stethoscope. Eko built a digital version that didn't just amplify sound but recorded it, visualized it as a waveform on a screen, and ran it through an AI trained to detect murmurs and arrhythmias. The device could identify abnormal heart sounds with a consistency that no human ear, no matter how experienced, could match.

But here's what matters more than the algorithm: it could do this in the hands of a primary care physician. In the hands of a nurse. In the hands of someone like me, who could never reliably hear a murmur with an analog scope in a noisy room. And for hearing-impaired physicians, who may have quietly stepped away from auscultation altogether, it reopens a diagnostic door that was closing on them.

This connects to a broader shift that has been quietly transforming cardiology. Identifying structural heart problems and rhythm abnormalities was, for most of medicine's history, a mystery reserved for specialists. You needed years of training to interpret the subtleties of a heart murmur or parse the complexities of a 12-lead ECG. Primary care physicians, internists, emergency doctors, we all learned the basics, but the advanced diagnostic work belonged to the cardiologists.

Digital stethoscopes and handheld ECG devices changed that equation. A primary care doctor can now place an Eko stethoscope on a patient's chest and get an immediate AI-assisted assessment of whether a murmur is present and how significant it might be. A nurse in a rural clinic can capture a diagnostic-quality ECG on a device the size of a credit card and have it interpreted in seconds.

And the ECG itself has turned out to hold far more information than anyone expected. Researchers at the Mayo Clinic discovered that AI algorithms trained on standard 12-lead ECGs could detect things that no human reader, no matter how experienced, could see. A routine ECG can now reveal that a patient has a weak heart pump, a condition called low ejection fraction, even when the patient has no symptoms and the tracing looks normal to the human eye. Other algorithms can detect signs of atrial fibrillation, the most common dangerous heart rhythm disorder, from a single ECG taken while the heart is beating normally, catching a condition that by definition comes and goes and has historically been maddeningly difficult to diagnose. New AI models can now identify the risk for structural diseases like hypertrophic cardiomyopathy and cardiac amyloidosis, conditions that once required expensive imaging or invasive biopsy to diagnose, from the same simple, inexpensive tracing available in any clinic on the planet.

For a physician, this changes the meaning of ordering an ECG. What used to be a rhythm check is becoming a screening tool for diseases that have nothing to do with electrical activity. For a patient, it means that a ten-second, painless test costing a few dollars might catch a life-threatening condition that would otherwise go undetected for years.

The monitoring revolution extends beyond the clinic walls entirely. The [Apple](https://www.linkedin.com/company/apple/) Watch and devices like [AliveCor](https://www.linkedin.com/company/alivecor/) KardiaMobile brought ECG capability to the consumer's wrist, and their algorithms can detect atrial fibrillation with surprising accuracy. For patients who need more sustained surveillance, wearable patches like the ZioPatch can continuously monitor heart rhythm for up to 14 days, capturing intermittent arrhythmias that a standard 24-hour monitor would miss. The physician's diagnostic reach now extends into the patient's daily life: sleeping, exercising, sitting in a meeting, walking the dog. A rhythm disturbance that would never have been caught in a ten-minute office visit can now be documented while the patient is brushing their teeth.

[Caption Health](https://www.linkedin.com/company/caption-health/) pushed the boundary further still. Their AI system guides non-expert clinicians through capturing a diagnostic-quality echocardiogram, an ultrasound of the heart. The AI watches the image in real time and tells the operator where to move the probe, when to hold still, and when the capture is good enough to interpret. The target user was never the cardiologist. It was everyone else.

The pattern across all of these innovations is the same: diagnostic capability that once required a specialist, a referral, and a wait is moving to the point of first contact. The primary care office. The rural clinic. The patient's own wrist. The question is no longer whether the technology can do it. The question is how medicine reorganizes itself around the fact that it can.

But the deskilling concern follows every one of these advances like a shadow. If the next generation of physicians learns cardiac assessment with AI doing half the diagnostic work, what happens when the AI isn't available? When the batteries die, when the network drops, when you're in a field hospital with nothing but a basic analog stethoscope and a patient who needs an answer? The technology is better than the unassisted human. The question is what becomes of the human without the technology.

Cardiology's story takes its sharpest turn when the algorithms leave the screen and enter the body.

For most of its history, interventional cardiology has been a feat of human dexterity and spatial imagination. A catheter is threaded through an artery, usually starting at the wrist or thigh, and guided into the heart or the vessels feeding it. The cardiologist navigates by watching a live X-ray called fluoroscopy, mentally reconstructing three-dimensional anatomy from a flat, shadow-like image. It demands extraordinary spatial reasoning, steady hands, and years of practice. It also bathes both patient and physician in radiation for the duration of the procedure.

In recent years, companies like [CathWorks](https://www.linkedin.com/company/cathworks/) began changing this equation. CathWorks developed a system that builds three-dimensional blood-flow simulations from the two-dimensional angiogram images already being captured during a procedure. The software can calculate whether a narrowed artery is actually restricting blood flow enough to warrant a stent, a measurement that previously required threading an additional pressure wire into the vessel. The cardiologist can now "test" the decision virtually before committing to it physically.

Cardiac CT is undergoing a similar transformation. AI can now automatically quantify coronary plaques, both the calcified kind visible on standard scans and the softer, more dangerous noncalcified plaques that have historically been difficult to assess. These tools measure the degree of artery narrowing, characterize plaque composition, and generate risk scores, turning what used to be a subjective visual assessment into a quantified, reproducible analysis. For the patient, this means a non-invasive CT scan can increasingly provide the kind of detailed coronary assessment that once required a catheter in the artery.

This was a meaningful shift. The AI moved from reading a signal after the fact to informing a decision during or even before a procedure. But the physician was still doing all the navigating.

By 2026, the next step is underway. New interventional systems are using reinforcement learning, AI that learns by trial and error in simulated environments, to assist with catheter navigation through complex vascular anatomy. The system helps guide the catheter through branching vessels, compensating for the heartbeat's pulsatile motion and each patient's unique anatomy. The physician remains in command of the strategic decisions: where to go, whether to intervene, what device to deploy. The AI handles the fine motor precision, the micro-adjustments that keep the catheter on course through vessels that twist and pulse.

The analogy that makes sense to most people is autopilot. Not self-driving. The pilot is still in the cockpit. The system handles the turbulence. The physician decides the destination; the AI assists with the navigation.

Cardiology isn't alone in this shift. In neurosurgery, AI-driven navigation systems are becoming what surgeons describe as "GPS for the brain," providing real-time, high-precision guidance through the most complex and unforgiving anatomy in the body. These systems assist at every stage, from pre-operative planning, where they map safe corridors through healthy tissue, to intraoperative guidance that tracks instruments against the patient's anatomy in real time. The principle is identical to catheter navigation: the AI enhances the surgeon's precision and spatial awareness without replacing their judgment. The destination is still the surgeon's call. The AI helps them get there without damaging what's along the way.

What changes the emotional register of this conversation is a simple fact: the AI is now physically inside the patient. In radiology, if an algorithm flags a false positive, the cost is a wasted minute of attention. In interventional cardiology, if a navigation system misjudges a turn, the cost could be a perforated vessel. Trust is no longer a philosophical debate about black boxes. It's a wire in someone's coronary artery, and the question of who's steering it is visceral.

The accountability framework for navigating this isn't as novel as people assume.

Go back to that cardiologist and the missed WPW in 2002. The legal reality was unambiguous: the machine generated an interpretation, and the physician bore the responsibility. That principle has governed algorithmic decision support in medicine for decades.

Automated blood count analyzers flag abnormal values; the physician signs the report. Robotic surgery platforms execute movements; the surgeon directs them. Smart ICU ventilators adjust breath-by-breath; the intensivist sets the parameters. And pacemakers, the original autonomous agents, have been making life-critical decisions inside human bodies since the 1960s. A modern implantable defibrillator detects a lethal rhythm and delivers a 700-volt shock on its own. No physician in the loop. No confirmation step. The device decides, and it acts.

These aren't future scenarios. They're Tuesday morning in any modern hospital. And they've never been 100% reliable.

Yet we've managed. Not because the machines are perfect, but because the system around them evolved. Training that teaches physicians to verify, override, and maintain independent judgment. Regulatory frameworks that define intended use and allocate liability. A culture that treats the algorithm as a tool, not an oracle.

The question for this generation of cardiac AI, the digital stethoscopes, the wearable monitors, the virtual simulations, the navigation systems, is whether that framework scales as the AI moves from interpreting signals on a screen to steering a wire through someone's artery. The foundation is not theoretical. It's been tested in practice for forty years. Whether it's sufficient for what comes next is the honest open question.

So what's the next version of "AI in cardiology is failing"?

It will center on autonomy. The critics will argue that systems physically guiding instruments inside the body represent an unacceptable risk, that one software error could be catastrophic, that we're moving too fast.

The objection will sound reasonable. It will also ignore the fact that we accepted machine autonomy inside the body decades ago. A pacemaker in 1965 fired on a fixed schedule, a simple rule-based system. A modern adaptive pacemaker senses activity, adjusts its rate, monitors for dangerous rhythms, and decides whether to intervene. The progression from fixed rules to sensing to autonomous decision-making happened inside a human chest, and we barely noticed because it happened gradually, device generation by device generation, each step making the patient a little safer than the last.

The risk calculus for catheter navigation, for digital twin simulations, for AI-guided intervention will follow the same logic. Not zero risk. Less risk than the alternative.

Meanwhile, somewhere right now, a primary care physician in a small clinic is pressing a digital stethoscope to a patient's chest. She's not a cardiologist. She never mastered the art of auscultation the way her professors insisted she should. But the device in her hand can hear what she cannot, and the algorithm behind it is telling her: this patient has a murmur. Refer.

A man in his fifties is glancing at his smartwatch during his morning run. He feels fine. The watch doesn't agree. It's flagged an irregular rhythm. He'll show the recording to his doctor next week, and the Holter monitor will confirm what the watch already knew: atrial fibrillation, caught months or years before it might have announced itself with a stroke.

Twenty years ago, that murmur would have gone undetected until the patient showed up in an emergency room with heart failure. The atrial fibrillation would have been discovered only after the clot had already traveled to the brain. Today, both were caught early, one by a physician with a better instrument, one by a patient who didn't even know he was being monitored.

The ear got sharper. It followed the patient home. And the people who benefit most are the ones who never had access to a specialist's ear in the first place.