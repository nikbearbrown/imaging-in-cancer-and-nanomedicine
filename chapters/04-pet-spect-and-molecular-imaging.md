# PET, SPECT, and Molecular Imaging

## Learning Objectives

By the end of this chapter you will be able to:

- **Explain** how PET forms an image from radioactive decay — positron emission, annihilation, and coincidence detection — and why this signal reports *function*, not anatomy.
- **Describe** how FDG, a glucose analog, traces the elevated metabolism of cancer cells, and **name** the false positives and false negatives that follow from what FDG actually measures.
- **Distinguish** PET from SPECT, and general metabolic tracers (FDG) from target-specific tracers (PSMA, DOTATATE), by the biological question each answers.
- **Justify** why functional imaging is fused with anatomic imaging (PET/CT, PET/MRI), reasoning from PET's coarse resolution.
- **Critique** the inference from "FDG-avid" to "malignant," weighing PET's radiation cost and specificity against its sensitivity.

## Opening Case

A 62-year-old man treated for lymphoma a year ago has a follow-up CT. There is a 2-centimeter mass where the tumor used to be. Is it residual cancer, or just scar tissue left behind after a successful treatment? CT cannot tell — both are masses of roughly the same density and shape (cba-29). The man is told he may need another round of harsh chemotherapy.

A **PET scan** is ordered. Lymphoma cells are metabolically ravenous; scar tissue is metabolically quiet. PET, which images metabolic *activity* rather than structure, shows the mass is **not** taking up the radiotracer — it is metabolically dead. The "tumor" on CT is scar. No further chemotherapy is needed (cba-29). Here a functional signal answered a question that no anatomic image could: not *is there a mass?* but *is the mass alive?*

Now the failure mode, which is the mirror image. Three months later the man develops a fever and a new PET shows a bright, FDG-avid lymph node. The reflex is to call it relapsed lymphoma and restart chemotherapy. But FDG does not measure cancer; it measures glucose uptake — and **inflammation and infection light up FDG just as brightly as tumor** (cba-29). The fever suggests infection. Treating the bright spot as cancer, without confirming, could mean toxic chemotherapy for what is actually an infected node. PET's signal is powerful and dangerously easy to over-read. This chapter is about what the radiotracer actually measures, and the gap between "it lights up" and "it is cancer."

## Core Concepts

### What PET measures: decay, annihilation, coincidence

Plain language: tag a biological molecule with a radioactive atom, inject it, and let it accumulate wherever that molecule is used; the radioactivity announces its location by emitting paired signals that the scanner triangulates.

Formally, **positron emission tomography (PET)** images the distribution of a **radiolabeled tracer** — a biological molecule carrying a radioactive isotope — that accumulates in tissue according to a biological process (cba-29). The physics is elegant. The isotope decays by emitting a **positron** (a positive electron). The positron travels a tiny distance, meets an ordinary electron, and the two **annihilate**, converting their mass into two gamma-ray photons that fly off in *exactly opposite directions* (180° apart). A ring of detectors around the patient records pairs of photons arriving at the same instant — **coincidence detection** — and the line connecting each pair must pass through the annihilation point. Collect millions of such lines and a computer reconstructs where the tracer concentrated (cba-29).

<!-- → [DIAGRAM: PET signal chain — isotope decay emits a positron → positron annihilates with an electron → two 511 keV photons emitted back-to-back at 180° → detector ring records the coincident pair → many lines reconstruct the activity map. Include FDG half-life (~110 min) and the trapped-glucose mechanism inset.] -->

Crucially, PET does not measure structure. It measures **where a biological process is happening**. The image is a map of activity. This is why PET is *functional* (or *molecular*) imaging, the complement to the anatomic imaging of the previous chapters (cba-29).

### FDG: tracing a tumor's hunger for glucose

The most widely used tracer is **fluorodeoxyglucose (FDG)** — a glucose molecule with a radioactive fluorine-18 atom substituted in. Cells take up FDG through their normal glucose transporters and phosphorylate it, but the modified molecule cannot proceed through metabolism, so it is **trapped** inside the cell (cba-29). The more glucose a cell consumes, the more FDG it accumulates. Cancer cells, which characteristically burn glucose at elevated rates (the Warburg effect), take up more FDG than most normal tissue and appear as bright spots (cba-29).

Fluorine-18 has a **half-life of about 110 minutes** — long enough to synthesize the tracer, inject it, and scan, short enough that the radioactivity clears in hours (cba-29). That short half-life is also a logistical constraint: the isotope is cyclotron-produced and decays fast, so it must be made near where it is used.

### Scale and signal: where PET sits on the ladder

- **Resolution:** roughly **4–6 mm** — the coarsest of all the clinical modalities, set partly by the small distance the positron travels before annihilating (cba-29).
- **Field of view:** whole-body, in a single study. PET's reach is its glory: it can find metabolically active disease *anywhere* in the body at once.
- **Biological question:** Where in the body is there active metabolism or expression of a specific molecular target — and is a known mass alive or dead?

That coarse resolution explains the field's defining design choice. A bright PET spot tells you activity is *here, roughly* — but 4–6 mm is too coarse to say exactly which anatomical structure it sits in. So PET is fused with an anatomic scan: **PET/CT** or **PET/MRI** overlays the functional map on a high-resolution structural image, marrying *what is active* (PET) to *exactly where* (CT/MRI) (cba-29). Hybrid imaging is the direct consequence of PET's place on the resolution ladder: pair a coarse, biologically rich signal with a sharp, structurally precise one.

### PET's limits: false positives and false negatives

Because FDG measures glucose uptake — not cancer — it misleads in two directions:

- **False positives:** inflammation, infection, brown fat, recent surgical sites, and granulomatous disease all consume glucose and light up FDG, mimicking tumor (cba-29). This is the opening case's trap.
- **False negatives:** some cancers are not FDG-avid — well-differentiated thyroid cancer, many prostate cancers, indolent and mucinous tumors take up little FDG and can hide (cba-29).

PET also carries real costs: a combined **PET/CT delivers about 25 mSv** of radiation — substantial, roughly double a body CT — and a scan costs several thousand dollars and depends on cyclotron-produced isotopes (cba-29). High sensitivity, imperfect specificity, real dose: PET is a strong but easily over-interpreted signal.

### SPECT: PET's lower-resolution cousin

**Single photon emission computed tomography (SPECT)** is the related nuclear-imaging technique. Instead of detecting paired annihilation photons, SPECT images isotopes that emit *single* gamma photons directly, using a rotating gamma camera. It is more widely available and cheaper than PET but provides somewhat **lower resolution** (cba-29). A familiar example is the **bone scan** (bone scintigraphy), in which a technetium-99m-labeled phosphonate accumulates in areas of bone turnover, flagging bone metastases — less specific than PET but inexpensive and broadly available (cba-29).

### Target-specific tracers: from metabolism to molecules

FDG reads a general property (glucose hunger). The frontier of molecular imaging is tracers aimed at a *specific molecule* that a particular cancer expresses:

- **PSMA PET** targets prostate-specific membrane antigen, a protein on prostate cancer cells. Ga-68 or F-18 PSMA tracers are highly sensitive for detecting and staging prostate cancer — including in the FDG-negative cases where FDG fails — and are FDA-approved for metastatic prostate cancer evaluation (cba-29).
- **DOTATATE PET** (Ga-68) targets somatostatin receptors on neuroendocrine tumors (cba-29).
- Amino-acid tracers (methionine, FET, FDOPA) for brain tumors; choline and fluciclovine for prostate cancer recurrence (cba-29).

The logic is profound and worth naming: **a molecule that drives a cancer's biology can be both an imaging target and a therapy target.** The same PSMA that lights up on a PET scan can be the docking site for a radioactive drug that kills the cell — the basis of **theranostics** (therapy + diagnostics), pairing a diagnostic tracer with a therapeutic one aimed at the identical target. Molecular imaging thus runs in parallel with the targeted-therapy revolution (cba-29; NCI Theranostics, 2023).

## Worked Example

**Situation.** A man with rising PSA (a prostate-cancer blood marker) after surgery has, by definition, cancer somewhere — but a conventional CT and bone scan show nothing. Where is the disease? The plan is to repeat the CT with more contrast and hope the recurrence becomes visible.

**Reasoning, including a dead end.** Repeating anatomic imaging is the dead end. The recurrence is small — too small to distort anatomy enough for CT to flag, and prostate cancer is often **not FDG-avid**, so even a standard FDG-PET may miss it (cba-29). Pushing harder on signals that the biology evades cannot work; the problem is not image quality but signal *choice*.

The right move switches to a **target-specific** signal. **PSMA PET** images the prostate-specific membrane antigen that the recurrent cells express, regardless of their glucose metabolism or their size. Even a tiny PSMA-expressing deposit concentrates the tracer and lights up against a dark background, whole-body, in one study (cba-29). PSMA PET routinely localizes recurrent prostate cancer that CT, bone scan, and FDG-PET all miss. The disease was always there; only a tracer matched to the cancer's specific molecule could find it.

**The lesson.** When the question is "where is this specific cancer," choose the tracer that targets a molecule the cancer actually expresses — not a generic metabolic tracer, and not a finer anatomic scan. Molecular specificity, not resolution, is the lever.

**The limit.** PSMA PET's specificity is also its boundary. It sees PSMA expression — so a PSMA-low variant of the cancer can hide, just as FDG misses low-glucose tumors. And at 4–6 mm resolution, PSMA PET reports that disease is *in this region*; it cannot resolve a microscopic deposit, count cells, or confirm malignancy without tissue. The tracer narrows the search to a place; it does not replace the biopsy that proves what is there (cba-29).

## Common Misconceptions

**"If it lights up on PET, it's cancer."** Plausible, because tumors are FDG-avid and a bright spot looks like a hit. It fails because FDG measures glucose uptake, not malignancy: inflammation, infection, brown fat, and healing surgical sites all light up identically (cba-29). This is precisely the opening case's trap — the FDG-avid node in a feverish patient was more likely infection than relapse. A positive PET is a lead to be confirmed, not a diagnosis. Treating the proxy (glucose uptake) as the thing (cancer) is the recurring error of this whole book.

**"A negative PET rules out cancer."** Plausible, because PET is highly sensitive for many tumors. It fails because some cancers — well-differentiated thyroid, many prostate, indolent and mucinous tumors — take up little FDG and stay dark despite being malignant (cba-29). A negative FDG-PET does not clear a patient whose tumor type is known to be FDG-poor; the right move there is a target-specific tracer or tissue, as the prostate worked example showed.

**"PET is the highest-tech scan, so it gives the sharpest, most detailed images."** Plausible, because PET is expensive and cutting-edge. It fails because PET has the *coarsest* resolution of all clinical modalities — 4–6 mm, far worse than CT or MRI (cba-29). Its power is not sharpness but the *kind* of signal: biological activity and molecular expression, whole-body. That is exactly why PET must be fused with CT or MRI to know precisely where the activity sits. High-tech does not mean high-resolution; it means a different question answered.

## Exercises

1. **(Recall/Understand.)** Walk through the PET signal chain in order: name what the isotope emits, what happens when it meets an electron, how many photons result and in what geometric relationship, and how the detector ring uses them to locate the source. Then state in one sentence why this makes PET a functional rather than an anatomic modality.

2. **(Apply.)** FDG has a half-life of about 110 minutes. A dose is calibrated at 8:00 a.m. (a) Roughly how much radioactivity remains at noon? (b) Explain, from the half-life, why FDG must be produced near the scanner rather than shipped overnight from a distant supplier, and why this constrains where PET can be offered.

3. **(Apply+/Produce.)** For each scenario, choose between FDG-PET, PSMA PET, and DOTATATE PET, and **justify by the molecular target and the cancer's biology**: (a) staging an aggressive lymphoma; (b) localizing biochemically recurrent prostate cancer with a normal CT; (c) imaging a metastatic neuroendocrine tumor. Produce a three-row table; for each, name one tracer that would be a poor choice and explain what its signal would miss.

4. **(Analyze.)** PET resolution is 4–6 mm and MRI resolution is ~1 mm. Explain why this resolution gap is the *reason* PET and MRI are physically combined into PET/MRI rather than used as competitors. What does each modality contribute to the fused image, and what would be lost by using either alone?

5. **(Evaluate/Produce.)** Return to the opening case's feverish patient with the FDG-avid node. The team is about to restart chemotherapy. Write a one-paragraph dissent: state precisely what the FDG signal does and does not establish, name the two most likely benign explanations given the clinical context, and specify the next step that would actually distinguish relapse from infection.

## What Would Change My Mind

The central claim is that PET measures a biological *proxy* (metabolic or molecular activity), not malignancy itself, so "FDG-avid" cannot be read as "cancer" without confirmation, and that PET's coarse resolution forces fusion with anatomic imaging. A specific finding would revise the first half: a tracer (or combination) prospectively validated to distinguish malignant from benign uptake — separating tumor from inflammation and infection — with specificity high enough to replace biopsy across tumor types. Total-body and long-axial-field-of-view PET, plus dual-tracer and kinetic-modeling approaches, are pushing toward better specificity, but as of now they remain research advances, not a clinical standard that lets a bright spot stand alone as a diagnosis (NCI Theranostics, 2023). For the resolution half: if detector and reconstruction advances pushed PET resolution toward 1 mm, the strict need to fuse with CT/MRI for localization would weaken. Neither result is in hand; either would move me.

## Still Puzzling

- **How specific can a tracer get before specificity becomes a liability?** A tracer perfectly specific to one molecular target (say PSMA) is blind to variants that lose that target. As cancers are increasingly imaged by single-molecule tracers, the false-negative risk from target heterogeneity grows. Where is the optimal balance between a general tracer and a hyper-specific one?

- **Does earlier, more sensitive molecular detection actually save lives?** PSMA PET finds recurrence sooner and more often — but finding disease earlier is not the same as helping the patient live longer or better. Whether the added sensitivity translates into mortality benefit, rather than just earlier knowledge, is genuinely unsettled for some uses [verify].

- **Will theranostics blur the line between imaging and therapy entirely?** If the same molecular target is imaged and then treated with a paired radioligand, "diagnosis" and "treatment" become one act. How should we evaluate the safety and benefit of a tool that is simultaneously a camera and a drug (NCI Theranostics, 2023)?

## References

- "Chapter 29 — Cancer Diagnosis: Imaging and the Tissue Sample" (cba-29), clinical-imaging source chapter, *Imaging in Cancer and Nanomedicine* pantry. (PET physics and FDG mechanism, false positives/negatives, dose, SPECT, bone scan, PSMA/DOTATATE tracers, hybrid imaging.)
- *Molecular probes for the in vivo imaging of cancer.* PMC3407672. https://pmc.ncbi.nlm.nih.gov/articles/PMC3407672/ (PET/SPECT, optical imaging, molecular-imaging strategy.)
- NCI, *Theranostics and AI in Cancer Precision Medicine* (2023). https://www.cancer.gov/about-nci/organization/cbiit/news-events/blog/2023/theranostics-and-ai-next-advance-cancer-precision-medicine
- NCI, *CT Scans and Cancer Fact Sheet* (PSMA imaging agents, radiopharmaceuticals). https://www.cancer.gov/about-cancer/diagnosis-staging/ct-scans-fact-sheet
- NCI, *Cancer Imaging Basics.* https://dctd.cancer.gov/research/research-areas/imaging/basics

## Prompts

<!-- This section is populated automatically by the Cowork enrichment pass. -->

*No figures have been generated for this chapter yet.*
