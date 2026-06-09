# Chapter 11 — Image-Guided Therapy
*Imaging as a coordinate system — how precision makes high doses possible, and why a smaller margin is the safety, not the risk.*

The lung tumor is 2 centimeters, stage I, in the lower lobe of a patient who cannot tolerate surgery. The plan is stereotactic body radiation therapy — five fractions of very high dose, sub-millimeter precision, steep dose gradients that fall off within millimeters of the target.

There is a problem the diagnostic images do not show directly. The tumor moves. Every breath cycle, the lower lobe slides more than a centimeter. The nodule does not occupy a fixed point in space; it traces a trajectory, a distribution of positions across the breathing cycle. A single planning CT, taken at one moment, captures one point in that distribution and calls it the target.

Aim the beam at that static point and two failures happen simultaneously. At the moments when the tumor has moved away from the plan's assumed position, the high-dose region misses it — the cancer is underdosed. At the same moments, healthy lung tissue that briefly occupies the beam's path receives the full ablative dose. The precision that makes SBRT effective — the steep dose gradients, the concentrated high-dose volume — becomes the liability. A conformal beam centered on the wrong coordinate is more dangerous than a broad beam, not less, because the dose that misses the tumor is going somewhere specific: the surrounding lung.

The solution is not a better picture of the tumor. It is imaging integrated into the delivery itself. A four-dimensional CT acquires the tumor's position at each phase of the breathing cycle, not just at one. Respiratory gating fires the beam only during the phase when the tumor is in the planned position. Cone-beam CT, taken in the treatment room in treatment position immediately before each fraction, verifies that the tumor is actually where the plan assumed.

These are not diagnostic images. They are intervention infrastructure — the coordinate system that makes the therapy geometrically possible. That shift in the role of imaging, from measurement to targeting frame, is the subject of this chapter.

---

### The margin: what image guidance is actually buying

Every radiation treatment plan draws a target volume around the visible tumor, then adds a **margin** — a rim of additional tissue around the tumor, irradiated because the tumor's true position on any given treatment day is uncertain. The margin absorbs that uncertainty. If the tumor might be 5 millimeters to the left of where it appeared on the planning scan, the plan includes an extra 5 millimeters of tissue on the left.

A larger margin means less chance of missing the tumor. It also means more normal tissue inside the high-dose region. The spinal cord, the salivary glands, the rectum, the contralateral lung — all of these sit some distance from the tumor, and all of them receive more dose as the margin around the tumor grows. Large margins are not conservative; they are a tradeoff between geometric security and normal-tissue damage. A margin that protects against a 1-centimeter setup error does so by irradiating 1 centimeter of healthy tissue in every direction. The "safe" large margin is safe for the tumor and dangerous for the organs around it.

Image guidance changes this arithmetic. If the tumor's position on each treatment day is verified by imaging in treatment position — not assumed from the planning scan — the uncertainty that the margin was absorbing is reduced. The margin can shrink. Smaller margin means less normal tissue in the high-dose field. Less normal tissue in the high-dose field means lower toxicity. And lower toxicity means the dose to the tumor can be escalated without the treatment becoming intolerable.

This is the mechanism by which image guidance translates into clinical benefit: not by making the image prettier, but by reducing the margin, which directly reduces normal-tissue dose, which creates room to escalate tumor dose. Margin reduction is the quantitative heart of image guidance.

For SBRT, the logic is not just about toxicity management — it is about whether the dose is safe to deliver at all. SBRT doses (7 to 25 Gy per fraction) are ablative. They are designed to sterilize the tumor completely in a small number of fractions. At that dose level, the steep dose gradient that falls off within millimeters means that any geometric miss delivers a high dose to a millimeter of normal tissue rather than a millimeter of tumor. The precision that makes SBRT effective is what makes accuracy non-negotiable. You cannot deliver ablative SBRT without image guidance. The dose level itself demands the targeting infrastructure.

---

### How IMRT sculpts the dose to the target's shape

Before image guidance enters, the dose must be shaped. The history of radiation therapy is largely the history of getting better at concentrating dose where the tumor is and withdrawing it from where it is not.

**Intensity-modulated radiation therapy** achieves this by varying the intensity of the beam across its profile. The instrument is the **multi-leaf collimator** — a bank of metal leaves, each a few millimeters wide, that can be positioned independently across the face of the beam. Each leaf blocks some of the beam. By setting different configurations at different angular positions of the treatment machine, and by varying the configuration continuously as the machine rotates in the newer volumetric modulated arc therapy, the planning system assembles a dose distribution inside the patient from the superposition of hundreds of modulated beams.

The crucial capability this adds is concave dose distributions. An older rectangular field arrangement cannot avoid overdosing a structure that sits inside the concavity of a tumor — if the spinal cord is behind and between two tumor volumes, rectangular fields must either underdose the tumor or overdose the cord. IMRT can produce a dose cloud that wraps around the cord, carving a low-dose notch precisely where the critical structure sits. The dose distribution can bend.

This concavity is what allows head and neck cancer treatment to spare the parotid glands: the plan wraps the high dose around the tumor volumes on both sides of the neck while pulling dose off the midline structures and the glands. Before IMRT, xerostomia — permanent dry mouth from parotid damage — was near-universal in head and neck radiation. It was not an acceptable toxicity that patients learned to live with; it was a severe, permanent impairment that substantially degraded quality of life. IMRT made it substantially less common by making parotid sparing geometrically achievable.

The plan is generated by **inverse planning**: the dosimetrist specifies what the dose distribution should be — tumoricidal dose in the target, dose constraints for the spinal cord, parotids, bladder, rectum — and optimization software finds the beam configuration that best achieves those specifications. The human designs the desired outcome and the algorithm designs the delivery. This is only possible because of the imaging that defined the targets and organs in the first place: the dose constraints make no sense if the target volumes are wrong.

---

### Verifying position before every fraction: IGRT

The plan may be perfect. The patient on treatment day two may not be positioned identically to treatment day one. The bladder may be more or less full. The tumor may have shifted relative to bony anatomy. The plan was optimized for a specific geometry, and any deviation from that geometry is an error.

**Image-guided radiation therapy** addresses this by imaging the patient in treatment position, in the treatment room, before each fraction. The most common tool is **cone-beam CT** — a low-dose CT scan taken by a detector mounted on the treatment machine itself, acquired while the patient lies on the treatment couch, immediately before the beam fires. The cone-beam CT is registered to the planning CT, and the difference in position is used to reposition the patient (by moving the treatment couch) or to apply a correction to the beam angles.

For bony structures — spine, pelvis — a simpler verification using two orthogonal kV X-ray images provides rapid confirmation of position without full three-dimensional CT. For soft-tissue targets, where the tumor may shift relative to bone (the prostate moves with bladder filling; the pancreatic tumor shifts with organ motion that bony landmarks don't capture), cone-beam CT is needed because it visualizes the tissue, not just the skeleton. **Fiducial markers** — small gold seeds implanted in or near the tumor before treatment — provide visible reference points for soft-tissue targets in settings where the tumor itself is hard to resolve on cone-beam CT.

The most significant advance in per-fraction guidance is the **MR-Linac**: a linear accelerator combined with an MRI scanner in the same treatment room. The patient is imaged by MRI while lying in treatment position, the current anatomy is compared to the planned anatomy, and the plan can be adapted to what is actually seen that day before delivery begins. MRI provides soft-tissue visualization that CT cannot match — it can image the prostate, the cervix, and abdominal tumors with contrast that cone-beam CT's limited imaging quality cannot achieve. The MR-Linac also enables real-time gating: the beam fires only when the anatomy matches the planned position, and stops automatically if the target moves out of range. This is the technical implementation of what the lung SBRT case required: the beam knows where the tumor is in real time and responds.

---

### 4D imaging and the moving target

For tumors that move with respiration — lung tumors, liver tumors, pancreatic tumors — a single CT taken at one point in the breathing cycle does not represent the target's position through the treatment. **Four-dimensional CT** acquires images at multiple phases of the breathing cycle simultaneously, using a respiratory monitor to sort the images by breathing phase. The result is a stack of CT volumes representing the tumor's position at each phase: end-inspiration, mid-inspiration, end-expiration, and everything in between. This is not just a better snapshot; it is a map of where the tumor is at every moment of the cycle.

From the 4D-CT, the planner can define an **internal target volume** that encompasses the tumor's motion across all phases — a larger volume that ensures the target is always inside the field regardless of breathing phase. Or the planner can choose **respiratory gating**: treat only during a specific phase (usually end-expiration, when the tumor position is most reproducible) and gate the beam so it fires only during that phase. The gated approach uses a smaller volume because the tumor's position range during the gating window is narrow, reducing the margin needed, reducing the normal tissue included, and allowing the ablative dose to be concentrated.

The motion management challenge for lung SBRT is also the reason surface-guided radiation therapy is valuable: cameras tracking reflective markers on the patient's chest surface provide continuous motion data that can correlate with internal tumor position and trigger the beam without requiring the patient to be imaged with X-rays every breath cycle.

---

### Adaptive radiotherapy: re-planning because the target changes

The plan is made before treatment begins. Treatment can last three to seven weeks. In that interval, anatomy changes. A head and neck tumor shrinks — the target volume that justified the original margins is no longer accurate. A patient loses weight — the patient's surface is different from the planning CT. The bladder that was modestly full on planning day is distended on treatment day fifteen.

**Adaptive radiotherapy** responds to these changes by re-imaging and re-planning during the course of treatment. The simplest version is *offline adaptation*: take a new CT partway through the course, assess whether the plan is still accurate, and replan if needed. More intensive is *online adaptation*: on the MR-Linac, take an MRI immediately before the fraction, adapt the plan to that day's specific anatomy, verify the adapted plan against dose constraints, and then deliver. The adaptation takes minutes. The plan for that fraction is the plan optimized to the anatomy that exists right now, not the anatomy that existed when planning was done.

Adaptive radiotherapy is the logical endpoint of the imaging-as-infrastructure principle: the plan is not a fixed artifact but a living document continuously re-anchored to the patient's current anatomy by real-time imaging. The tumor gets the planned dose; the organs at risk receive what they would receive if the plan were always drawn to the current geometry, not the baseline geometry.

---

### Proton therapy: precision in depth, with a physical constraint

Protons stop. This is the fact that distinguishes them from photons, which deposit dose along their entire path through tissue and continue beyond the target. A proton of a specific energy travels through tissue, depositing low dose along the path, then releasing a sharp burst — the **Bragg peak** — at the end of its range. Beyond the peak: essentially nothing. No exit dose.

This physics is genuinely different from photon physics and genuinely valuable in specific settings. A child with a posterior fossa brain tumor who receives proton therapy instead of photons accumulates less integral dose — less total energy deposited across the whole body — and therefore has a lower probability of radiation-induced secondary malignancy over the decades ahead. That probability difference compounds over fifty years of life, and it is real. For tumors sitting immediately adjacent to the optic chiasm or the brainstem, protons can treat the tumor while avoiding the dose that photons would deposit in those critical structures on the way out.

For prostate cancer and many lung cancers, the comparison with modern photon techniques — IMRT, SBRT — is less favorable. Modern photon planning already achieves low doses to the rectum and bladder. The margin for proton improvement in acute and late toxicity in these cancers has been narrow in comparative clinical data, and proton centers cost several hundred million dollars to build. The allocation question — whether the incremental clinical benefit justifies the cost — is unresolved for most common adult cancers treated in this era of conformal photon delivery.

The proton's precision also creates a specific vulnerability: **range uncertainty**. The exact stopping point of a proton beam depends on the density and composition of all the tissue it traverses. If the tissue is heterogeneous — air pockets, bone, varying soft tissue — the proton's range is predicted imprecisely. A proton plan that relies on precision in depth is sensitive to errors in where the proton stops, which means it is sensitive to tissue motion, to changes in patient anatomy between planning and treatment, and to uncertainties in the CT-based range calculation. The Bragg peak's advantage — stopping exactly at the target — becomes a liability if the stopping point is poorly predicted. Image guidance for proton therapy must address depth accuracy as well as lateral positioning.

<!-- → [DIAGRAM: dose-depth profiles. Two curves on shared axes, x-axis = depth in tissue, y-axis = relative dose deposited. Photon curve: moderate surface dose, gradual exponential decay, tail extending past the target (exit dose labeled). Proton curve: low dose along path, sharp Bragg peak at end of range, near-zero beyond. Target region shaded between two vertical depth lines. Annotate: "exit dose" on photon tail; "Bragg peak" at proton maximum; "range uncertainty" as a bracket around the Bragg peak showing where the proton might actually stop. Caption: proton precision requires accurate prediction of stopping depth, which is the clinical vulnerability of the technique.] -->

---

### Beyond radiation: fluorescence-guided surgery and image-guided ablation

The infrastructure principle extends beyond radiation.

A surgeon resecting a brain tumor aims to remove all the tumor while preserving normal brain. The problem is that at surgical margins — the interface between tumor and normal tissue — the distinction is not always visible to the naked eye. **5-aminolevulinic acid** is a precursor that the body converts to protoporphyrin IX, a compound that accumulates preferentially in glioma cells and fluoresces pink-red under a specific wavelength of blue light. The surgeon switches to the fluorescent imaging mode and sees where the tumor is still present. The fluorescence is not a diagnosis (it requires pathologic confirmation); it is a real-time targeting signal during the operation, allowing more complete resection at the margins where the critical question — is this tumor or normal brain? — is hardest to answer by appearance alone.

**Indocyanine green** serves a similar role in other surgical settings: injected and taken up by the hepatobiliary system, it helps surgeons identify anatomical structures and vascular territories during liver surgery; injected and tracked to sentinel lymph nodes, it guides the lymph node mapping procedure with real-time fluorescence rather than requiring gamma-probe detection of a radiotracer.

**Image-guided ablation** uses CT or ultrasound to position a probe inside or immediately adjacent to a tumor, then delivers thermal energy that heats the tumor to lethal temperatures. **Radiofrequency ablation** and **microwave ablation** are the dominant modalities for liver tumors, lung tumors, and renal cell carcinoma. **Cryoablation** freezes tumors rather than heating them. The imaging is not the treatment; the needle and the energy are. But without imaging to navigate the needle to the target and confirm its position before energy delivery, the ablation is blind and either misses the target or injures adjacent structures.

In each case — fluorescence-guided surgery, image-guided ablation — the principle is the same one the chapter opened with: imaging is the coordinate system that lets a physical intervention hit a target it cannot see directly.

---

### What post-treatment imaging cannot tell you

After treatment ends, imaging assesses what happened. A follow-up CT shows the lung tumor smaller, or absent, or unchanged. A PET scan shows the previously FDG-avid lesion no longer taking up tracer. These findings are reported as evidence of treatment response, and they are meaningful.

They are also proxies. A tumor that appears smaller on CT may have undergone central necrosis with a preserved fibrous shell — smaller radiographic appearance, incompletely sterilized cells at the viable periphery. Radiation induces local inflammation; inflammatory tissue can appear hypermetabolic on PET, mimicking residual disease ("pseudoprogression") or producing false positives. A post-treatment scar cannot be distinguished radiographically from a small residual tumor at the lower limit of imaging resolution.

The imaging response is not the cure. Local control — the tumor does not regrow at the treated site — is itself a proxy for survival if micrometastatic disease outside the treated field is present. A patient whose primary tumor is sterilized by perfectly aimed SBRT but who has occult circulating tumor cells seeding the liver is not cured by the local control. The imaging that aimed the therapy beautifully cannot see the cells it did not treat.

This returns to the consistent theme of the imaging chapters: every signal is a measurement of something, and that something is a proxy for what clinicians and patients care about. Imaging guides the therapy to the visible target with remarkable precision. It cannot address the disease beyond the visible target, and it cannot, after the fact, prove that the disease at the visible target is completely gone.

---

## Exercises

**Warm-up**

1. *(Recall — difficulty: low)* Define these five terms in one sentence each, and for each state whether it primarily concerns defining the target, verifying its position, or delivering dose: IMRT, IGRT, CBCT, SBRT, and the Bragg peak. *What this tests: the vocabulary of image-guided therapy before it is applied to clinical scenarios.*

2. *(Recall — difficulty: low)* Explain the relationship between image guidance, margin size, and normal-tissue dose in radiation therapy. Specifically: what uncertainty does the margin absorb, how does per-fraction imaging reduce that uncertainty, and what happens to normal-tissue dose when the margin shrinks? *What this tests: the margin-reduction mechanism before it is applied to specific cases.*

3. *(Recall — difficulty: low)* What is a 4D-CT and why is it used instead of a standard CT for lung SBRT planning? State two options for managing respiratory motion that 4D-CT data enables, and explain one tradeoff between them. *What this tests: the 4D-CT concept and the internal-target-volume versus gating choice.*

**Application**

4. *(Apply — difficulty: medium)* A lung SBRT target moves 1.5 centimeters with respiration. Explain mechanistically why a single static planning CT is inadequate for this case. Name two specific image-guidance techniques from the chapter that address the motion, state what each one measures or controls, and explain why their combination achieves better targeting than either alone. *What this tests: the moving-target problem applied to SBRT with explicit mechanism reasoning.*

5. *(Apply — difficulty: medium)* A head and neck cancer treatment plan must achieve tumoricidal dose to bilateral neck targets while keeping the spinal cord below its tolerance dose and sparing both parotid glands. Explain why a simple opposed-lateral field arrangement fails each of these goals, and describe how IMRT inverse planning addresses each failure — specifically using the concept of concave dose distributions. *What this tests: the geometric case for IMRT over simple field arrangements, with organ-specific reasoning.*

6. *(Apply — difficulty: medium)* A proton therapy center argues that their Bragg peak technology will produce fewer late rectal and urinary complications in intermediate-risk prostate cancer compared with IMRT. Evaluate this argument using: (a) what the Bragg peak physically achieves in terms of dose distribution; (b) what modern IMRT already achieves in terms of rectal and bladder dose constraints; (c) range uncertainty as a proton-specific vulnerability; and (d) the current state of comparative clinical evidence. Conclude with a calibrated statement of what clinical evidence would change your assessment. *What this tests: the proton-versus-photon comparison applied to a specific cancer type with explicit evidence reasoning.*

**Synthesis**

7. *(Synthesize — difficulty: high)* Construct a complete image-guided treatment plan for a prostate SBRT course of five fractions. For each element of the plan, state: (a) which imaging modality is used; (b) what it specifically measures or verifies; (c) why that measurement is necessary at that stage; and (d) one failure mode if that imaging step is omitted or inaccurate. Cover at minimum: planning target definition, per-fraction position verification, motion management, and post-treatment response assessment. Conclude by explaining what the post-treatment imaging can and cannot establish about whether the patient was cured. *What this tests: end-to-end integration of the imaging infrastructure for a complete SBRT course, with explicit failure-mode analysis.*

8. *(Synthesize — difficulty: high)* Compare the clinical applications of cone-beam CT, MR-Linac, and 4D-CT as image-guidance tools. For each, state: (a) the physical signal it uses; (b) what source of geometric uncertainty it addresses; (c) what clinical situations it is best suited for; and (d) one situation where it is insufficient and a different approach is required. Then construct a general principle for selecting image-guidance technology, based on the relationship between the motion being corrected and the information each modality provides. *What this tests: comparative analysis of three guidance modalities with a generalizable selection principle.*

**Challenge**

9. *(Challenge — difficulty: high)* Adaptive radiotherapy — re-planning to account for anatomic changes during the treatment course — is technologically possible with MR-Linac systems but adds substantial time, cost, and complexity per fraction. Some argue that adaptive RT should become standard of care for all moving targets; others argue that the marginal benefit over well-guided conventional CBCT-based treatment is small for most patients, and that the resources should go to making basic image guidance available to more patients worldwide. Evaluate both positions: (a) what evidence exists that online adaptive RT improves clinical outcomes (local control, toxicity) beyond CBCT-guided treatment without online adaptation; (b) what patient populations and anatomic sites have the strongest biological and geometric rationale for online adaptation; (c) what the opportunity cost is of prioritizing sophisticated adaptive technologies in high-income settings when basic IGRT is not universally available; and (d) propose a framework for allocating image-guidance technology investment that accounts for both clinical benefit and global access. Be explicit about what is established versus what you are inferring from mechanism, and identify the single most important trial whose results would most change the field's approach to adaptive RT. *What this tests: evidence-level reasoning about a live clinical controversy, global health perspective on technology allocation, and the relationship between biological rationale and clinical evidence.*
