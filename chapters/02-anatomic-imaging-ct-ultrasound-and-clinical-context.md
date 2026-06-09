# Chapter 2 — Anatomic Imaging: CT, Ultrasound, and Clinical Context
*What a scan actually measures — and why "the CT shows cancer" is a sentence a radiologist cannot write.*

The junior trainee reads the CT report and writes in the chart: "lung cancer with liver metastasis." It is a reasonable inference. The chest CT showed a 3-centimeter mass in the right upper lobe, enlarged mediastinal lymph nodes, and a small lesion in the liver. The radiologist's report says "findings consistent with primary lung malignancy with possible hepatic metastasis." The trainee connected the dots.

The trainee connected the wrong dots. What the CT measured was X-ray attenuation — how much each tissue absorbs radiation from many angles around the patient, reconstructed computationally into density maps. Bone appears white because it absorbs X-rays strongly. Air appears black because it absorbs almost none. The 3-centimeter mass is a region of tissue dense enough to attenuate X-rays more than the surrounding lung parenchyma. Dense tissue and malignant tissue are not the same thing. The liver lesion might be a benign cyst. The enlarged nodes might be reactive to an old granulomatous infection. The CT has done exactly what it is built to do — located abnormalities, measured their sizes, and mapped their relationships to adjacent structures — and it cannot do the one thing the trainee assumed it did: distinguish malignant from benign.

Before anyone writes "cancer" in the chart, tissue must be obtained and a pathologist must look at cells. To get that tissue safely from a lesion deep in the liver, the team will use a different modality entirely — one that uses sound rather than radiation, that works in real time, and that can watch a needle travel to the exact spot as the biopsy is being taken. Two different physical principles, two different clinical jobs. The CT found the target; the ultrasound will navigate the needle to it.

This chapter is about what those two physical signals are, what each one can and cannot tell you, and how to choose between them when the clinical question changes.

---

### What anatomic imaging is actually for

Imaging is a step in a chain, not an endpoint. The chain runs: clinical suspicion → imaging → biopsy → pathology → diagnosis. Imaging occupies the middle of this chain and its job is specific: convert a vague clinical suspicion — "there might be a mass somewhere" — into a specific, located, measured target. It answers structural questions. Where is the abnormality? How large is it? Is it one lesion or several? What does it touch, and what does it push aside?

What anatomic imaging cannot do is answer biological questions about cells. It measures physical properties of tissue — density for CT, acoustic reflectivity for ultrasound, proton relaxation for MRI — and those physical properties correlate with, but do not identify, malignancy. The correlation is useful. A 3-centimeter spiculated mass in the right upper lobe of a former heavy smoker has a much higher prior probability of being cancer than a smooth round 5-millimeter nodule in the same location. That prior probability is what the radiologist is communicating with "findings consistent with." It is not a diagnosis. It is an indication for biopsy.

Functional imaging — PET and its variants — maps metabolic activity rather than anatomy, which is closer to biology, but even PET reads a proxy (glucose uptake, or receptor expression) rather than cellular identity. No imaging modality, anatomic or functional, replaces pathology. The error of confusing imaging findings with diagnosis shows up again and again in clinical practice, and it does consistent harm: patients are told they have cancer before the tissue is examined, or biopsy is delayed because the image "looked enough like cancer," or the wrong treatment is initiated based on the imaging stage before it is confirmed.

---

### CT: the physics of X-ray attenuation

A CT scanner is a rotating X-ray system. An X-ray tube and a detector array orbit the patient continuously, acquiring a large number of projections — each one measuring how much X-ray intensity is lost passing through the body along a specific path through the slice being imaged. The detector records this attenuation for hundreds of angular positions around the patient in a few seconds.

The mathematical problem being solved is an inverse problem: given many one-dimensional projections of a two-dimensional slice, reconstruct the two-dimensional density map that produced those projections. The algorithm — filtered back-projection and its computational descendants — was developed by Allan Cormack in the 1950s and implemented in the first clinical scanner by Godfrey Hounsfield at EMI in the early 1970s. They shared the 1979 Nobel Prize in Physiology or Medicine. Before their work, the interior of the body was visible only by exploratory surgery or by the crude silhouettes that conventional X-ray projections produced.

The output is a stack of cross-sectional slices, each a density map in Hounsfield units. Air is assigned −1000 HU. Water is 0. Soft tissue falls between roughly −100 and +100. Bone ranges from 400 to over 1000. Fat sits around −100. Blood and tumor both fall in the soft-tissue range, which is why contrast agents — iodine injected intravenously — are used to distinguish blood vessels from surrounding tissue and to highlight tumors whose vascularity differs from background.

The capabilities this produces are substantial. Modern multi-detector scanners reconstruct images at sub-millimeter resolution — often around 0.5 millimeters — and can image the entire chest, abdomen, and pelvis in a single acquisition lasting ten to fifteen seconds. This is the capability the opening case used: a survey of the whole torso that found abnormalities in the lung, the mediastinum, and the liver simultaneously, mapped their relationships to the vessels and airways, and measured their dimensions. No other modality provides this combination of spatial coverage, speed, and resolution.

The cost is ionizing radiation. A typical body CT delivers 8 to 15 millisieverts of absorbed dose. A single chest X-ray delivers roughly 0.1 millisieverts. Natural background radiation from cosmic rays, radon, and terrestrial sources contributes about 2.5 millisieverts per year to the average person. A body CT is therefore equivalent to roughly 80 to 150 chest X-rays or three to six years of natural background radiation exposure in a few seconds. This is not negligible, particularly for young patients who will have many decades in which a radiation-induced malignancy could develop, or for patients who will have many serial scans over the course of treatment.

The other cost is contrast. Iodinated contrast agents are generally safe but carry small risks of allergic reaction and contrast-induced nephropathy, particularly in patients with pre-existing renal insufficiency. A creatinine check and a risk assessment precede contrast administration in patients where impairment is possible.

CT's limitation as a signal is soft-tissue contrast. Because many soft tissues have similar densities, CT cannot distinguish tumors from muscle or identify intracranial structures in the detail that MRI provides. The brain, spinal cord, and liver parenchyma are generally better characterized by MRI when anatomic detail in soft tissue is the primary question.

<!-- → [DIAGRAM: CT signal formation and reconstruction. Left: cross-sectional view of patient inside scanner ring, with X-ray tube and detector array shown at one angular position and faint lines indicating multiple other angular projections radiating through the patient. Center: schematic of many one-dimensional projections of a single slice, labeled "angular projections." Right: the reconstructed density image with regions labeled (bone = bright white, air = black, soft tissue = gray, fat = darker gray). Caption: "CT acquires X-ray attenuation from hundreds of angles, then solves backward for the density at every point."] -->

---

### Ultrasound: the physics of reflected sound

Ultrasound uses mechanical waves — pressure waves in tissue — rather than electromagnetic radiation. The frequency is far above the range of human hearing: diagnostic imaging uses frequencies of 2 to 15 megahertz or higher. An ultrasound probe contains both a transmitter that generates brief pulses of sound and a receiver that detects echoes. The probe is held against the skin and acoustic coupling gel allows the sound to pass from the probe into tissue without losing energy at the air interface.

Sound reflects wherever it encounters a boundary between tissues with different acoustic impedances — roughly, different combinations of density and stiffness. The returning echo is detected by the probe, and the time delay between transmission and echo return tells the system how far away the reflecting surface is. Sound travels through soft tissue at roughly 1540 meters per second; a microsecond of delay corresponds to less than a millimeter of depth. The ultrasound system builds an image by firing pulses in many directions across the face of the probe and assembling the echoes into a real-time display.

This physics produces a set of capabilities and limitations that are essentially the mirror image of CT's.

**Real time.** Because ultrasound is acquired continuously as the probe sweeps, the display updates in real time — you watch motion happening, not a frozen snapshot. This is what makes ultrasound irreplaceable for biopsy guidance: the needle is visible as a bright echogenic line in the image as it moves toward the target, and the operator watches it in real time as the biopsy is performed.

**No ionizing radiation.** Ultrasound has no known harmful biological effects at diagnostic power levels. It can be used in pregnant patients, repeated without concern about cumulative dose, and performed in settings where radiation is contraindicated.

**Depth-resolution tradeoff.** Higher-frequency ultrasound gives better spatial resolution but penetrates less deeply into tissue. A 15 MHz probe resolves structures to fractions of a millimeter but cannot image beyond a centimeter or two of depth. A 3 MHz probe reaches deep abdominal organs but resolves them at only 1 to 2 millimeters. The operator selects frequency based on the depth of the target — the thyroid, a centimeter below the skin, uses a high-frequency probe; the pancreas, 8 to 10 centimeters deep, requires a lower frequency with correspondingly lower resolution.

**Operator dependence.** Unlike CT, where the reconstruction algorithm produces the image from raw detector data regardless of who performs the scan, ultrasound images depend on how the probe is positioned, angled, and moved. The operator makes real-time decisions about which planes to image, what frequency to use, and how to optimize image quality for this patient's body habitus. Image quality genuinely varies between operators with different training and experience. This is not a fixable limitation — it is intrinsic to the real-time, hand-guided nature of the signal.

**Gas and bone.** Sound does not penetrate air or bone well — it reflects almost entirely at those interfaces. Bowel gas, lung, and ribs create acoustic shadows that block visualization of structures behind them. This is why abdominal ultrasound is limited when the bowel is gas-distended and why the lungs cannot be imaged beyond their surface.

The clinical applications follow directly from these properties. Superficial structures — thyroid, salivary glands, breast, lymph nodes in the neck and axilla — are imaged with high-frequency probes at excellent resolution with no radiation dose. Cystic versus solid characterization of a nodule is one of ultrasound's signature capabilities: fluid-filled cysts transmit sound and show through-transmission enhancement behind them; solid lesions attenuate sound and show acoustic shadowing. Real-time guidance for biopsies, drains, and catheter placements uses ultrasound wherever a needle or tube must go to a specific location. **Endoscopic ultrasound** — an ultrasound transducer mounted on the tip of an endoscope passed into the esophagus or stomach — brings the probe directly adjacent to the pancreas and distal bile duct, achieving resolution that external ultrasound cannot reach through overlying bowel and fat. Endoscopic ultrasound is the most sensitive imaging tool for detecting small pancreatic tumors and for staging pancreatic cancer.

---

### The frequency-depth tradeoff is a fundamental constraint

It is worth pausing on the depth-resolution tradeoff because it recurs throughout imaging physics in different forms and it explains why no single modality solves all problems.

Higher frequencies carry more energy per cycle and can resolve finer structures because the wavelength of the sound wave sets the minimum feature size the system can distinguish — you cannot resolve structures smaller than a wavelength. But higher-frequency sound also attenuates more rapidly in tissue: the energy is absorbed over shorter distances. This is not a limitation of current technology; it is a physical consequence of how sound interacts with matter.

The same tradeoff appears in MRI in the relationship between magnetic field strength and resolution. It appears in optical imaging in the tradeoff between numerical aperture (the angle over which light is collected, which governs resolution) and working distance. It appears in every wave-based imaging system: to resolve finer features, you use shorter wavelengths; shorter wavelengths interact more strongly with matter; stronger interaction limits depth. This is why imaging in biology requires multiple modalities operating at different scales, rather than one ideal instrument. The clinical question — its depth, its required resolution, its need for real-time feedback — routes to the modality whose physics matches those requirements.

---

### How to choose: the decision depends on the question

The two modalities are not ranked from worse to better. They serve different clinical questions rooted in different physical constraints.

**Choose CT when:** the question is whole-body, the target may be anywhere in the chest, abdomen, or pelvis, the scale of structures of interest is centimeters, and the radiation dose is justified by the staging or diagnostic value. CT for staging a known cancer searches the whole torso for lymphadenopathy, hepatic lesions, pulmonary nodules, and skeletal involvement simultaneously. No other single test provides this overview at this resolution.

**Choose ultrasound when:** the target is superficial and localized, real-time guidance is needed, radiation is to be avoided (pregnant patient, young patient, serial monitoring), or the question is specifically cystic-versus-solid. Ultrasound to characterize a palpable thyroid nodule and guide a fine-needle aspiration achieves better resolution at the target than CT would, with no radiation.

There are cases where neither provides the best answer. The pancreas sits behind the stomach, behind loops of bowel, deep in the retroperitoneum — the bowel gas blocks external ultrasound and CT's soft-tissue contrast may not distinguish a small pancreatic tumor from surrounding tissue. This is where endoscopic ultrasound or MRI with specific protocols enter the decision.

The decision framework is: match the modality to the scale, depth, and type of the question. It is not "use the most powerful machine available." The most powerful machine for the wrong question provides no useful information and may cause harm — the radiation of a whole-body CT for a thyroid nodule, the iodine contrast in a patient with impaired renal function, the delay in biopsy while waiting for an MRI appointment when ultrasound guidance is available immediately.

---

### Measuring treatment response: when the number becomes the question

Anatomic imaging is how oncologists determine whether treatment is working. Before treatment, the CT establishes baseline dimensions of target lesions. After one or two treatment cycles, a repeat CT measures the same lesions. The percent change in the sum of longest diameters of measured target lesions is classified by **RECIST** — Response Evaluation Criteria in Solid Tumors — as complete response (disappearance of all lesions), partial response (at least 30% reduction), progressive disease (at least 20% increase or new lesion), or stable disease (between).

RECIST is a valuable tool for clinical trial endpoints because it standardizes the language of response and allows comparison across studies. The number it produces — millimeters of longest diameter — is genuinely informative. A tumor that has shrunk from 4 centimeters to 1.5 centimeters after two cycles of therapy has changed in a way that matters biologically.

Size is still a proxy. A tumor can undergo central necrosis — the cancer cells die but the fibrous framework remains and the total lesion size changes little — producing minimal RECIST change in a responding tumor. A tumor can swell with immune infiltrate after immunotherapy — "pseudoprogression" — appearing larger on CT despite effective therapy. A tumor can develop cystic change in response to some targeted therapies, appearing larger in cross-section while the solid viable tumor component is smaller. These are all cases where the CT measurement reports the proxy correctly — the dimension is what it is — while the proxy fails to reflect the underlying biology.

RECIST has known limitations and partial solutions (separate criteria for immune responses, modifications for specific tumor types), but the fundamental constraint is that size is a physical property of the lesion rather than a biological property of its cells. The gap between the physical measurement and the biological question — is this patient responding? will this patient live longer? — is the gap that quantitative imaging methods, discussed in subsequent chapters, are designed to narrow. Anatomic imaging establishes the target and measures its physical dimensions. What happens inside those dimensions, and whether the patient lives longer as a result of treatment, requires different measurements or different endpoints.

---

## Exercises

**Warm-up**

1. *(Recall — difficulty: low)* For CT and for ultrasound, state: (a) the physical signal the modality measures; (b) the approximate spatial resolution; (c) the typical field of view (whole-body survey versus local); and (d) the radiation dose for a typical body CT, expressed in millisieverts, in multiples of a chest X-ray, and in years of natural background exposure. *What this tests: the physical foundations of each modality before comparing them in clinical scenarios.*

2. *(Recall — difficulty: low)* What is the depth-resolution tradeoff in ultrasound? Explain why a high-frequency probe gives better resolution but cannot image deep structures, and state what physics principle makes this tradeoff unavoidable rather than fixable by better technology. *What this tests: the fundamental physical constraint of ultrasound before applying it to clinical probe selection.*

3. *(Recall — difficulty: low)* What is RECIST, and what does it measure? State one clinical scenario where a RECIST response (lesion shrinkage ≥30%) might not indicate that the patient is benefiting from treatment, and explain why size can be a misleading proxy in that scenario. *What this tests: the measurement-versus-biology proxy distinction applied to treatment response assessment.*

**Application**

4. *(Apply — difficulty: medium)* You have four patients arriving in clinic. For each, select CT or ultrasound as the first-line anatomic imaging modality, justify the choice by explicitly addressing the signal, depth, resolution, radiation, and real-time-guidance requirements of the question, and name one feature that disqualifies the modality you did not choose: (a) a 62-year-old man with biopsy-proven non-small-cell lung cancer, staging for surgical resectability; (b) a 32-year-old pregnant woman with right upper quadrant pain and a suspected gallbladder mass; (c) a 45-year-old woman with a palpable neck lymph node and a question of whether it is reactive or enlarged; (d) a 58-year-old man with elevated CA 19-9 and a suspected 1.5-centimeter pancreatic head lesion. *What this tests: modality selection based on clinical question requirements, with explicit disqualification reasoning.*

5. *(Apply — difficulty: medium)* A body CT delivers approximately 12 mSv. Natural background radiation is 2.5 mSv per year; a chest X-ray is 0.1 mSv. Express the body CT dose as a multiple of a chest X-ray and as years of background radiation. Then argue in two sentences each: (a) why this dose routinely justifies a staging CT in a patient with biopsy-proven colon cancer; and (b) why it does not justify routine annual CT screening of healthy 25-year-olds with no risk factors. *What this tests: quantitative reasoning about radiation dose and the dose-benefit tradeoff in different clinical contexts.*

6. *(Apply — difficulty: medium)* The trainee in the opening case wrote "lung cancer with liver metastasis" in the chart based on the CT report. Write a corrected chart entry of no more than three sentences that: (a) accurately states what the CT established; (b) states what it did not establish; and (c) specifies the next step needed to convert the hypothesis into a diagnosis, naming the modality that will guide tissue sampling and why it is the right choice for that specific lesion. *What this tests: precise communication of the scope and limits of anatomic imaging findings in a clinical context.*

**Synthesis**

7. *(Synthesize — difficulty: high)* The depth-resolution tradeoff in ultrasound appears in different forms in other wave-based imaging modalities. For CT (photons), MRI (radiofrequency waves), and optical microscopy (visible light), describe an analogous resolution-versus-penetration constraint in each modality — state what sets the resolution limit, what limits the penetration, and whether the tradeoff is fundamental or addressable with better technology. Conclude with a general statement about why clinical imaging requires multiple modalities rather than a single ideal instrument. *What this tests: generalization of a physical principle across modalities and the structural reason for modality diversity.*

8. *(Synthesize — difficulty: high)* A patient with metastatic renal cell carcinoma on a targeted therapy has two CTs at 8-week intervals. The first shows target lesions summing to 6.2 cm. The second shows 5.1 cm — a 17.7% reduction, classified as stable disease by RECIST (threshold for partial response is ≥30%). The treating oncologist notes that the lesions appear "more cystic" on the second CT and considers this a treatment effect. Evaluate this clinical reasoning: (a) what does the RECIST classification accurately capture; (b) what does cystic change in a targeted-therapy response suggest biologically; (c) why is size alone a potentially misleading proxy in this specific clinical scenario; and (d) what additional imaging or measurement would most helpfully supplement the RECIST assessment to better characterize whether the patient is responding. *What this tests: application of the proxy-versus-biology distinction to a specific, clinically realistic RECIST-stable-disease scenario.*

**Challenge**

9. *(Challenge — difficulty: high)* AI-assisted interpretation of CT and ultrasound images is increasingly claimed to match or exceed radiologist performance for specific tasks — nodule characterization, fracture detection, liver lesion classification. Some argue that if such algorithms can distinguish malignant from benign lesions with sensitivity and specificity comparable to biopsy, the "imaging cannot diagnose" principle in this chapter would be obsolete. Evaluate this argument: (a) what would a validated AI imaging tool need to demonstrate to replace biopsy for a specific indication; (b) what information comes from tissue pathology that no imaging signal — however well-analyzed — can currently provide; (c) what are the risks of narrowing the biopsy indication based on imaging-AI confidence in a population where the prior probability of cancer varies; and (d) whether you think AI-based imaging will ever be sufficient to replace biopsy as the diagnostic standard for common solid tumors, and on what timeline and with what evidence threshold. Be explicit about what is established versus speculative, and identify the single most important piece of evidence that would most change your assessment. *What this tests: critical evaluation of an emerging technology against fundamental principles, with explicit distinction between what imaging measures versus what pathology establishes, and honest appraisal of the gap between current performance and clinical standard.*
