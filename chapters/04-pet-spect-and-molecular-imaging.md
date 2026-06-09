# Chapter 4 — PET, SPECT, and Molecular Imaging

A 62-year-old man treated for lymphoma a year ago has a follow-up CT. There is a 2-centimeter mass where the tumor used to be. Is it residual cancer, or scar tissue left behind after successful treatment? CT cannot tell — both are masses of roughly the same density and shape. The man is told he may need another round of harsh chemotherapy.

A PET scan is ordered. Lymphoma cells are metabolically ravenous; scar tissue is metabolically quiet. PET, which images metabolic activity rather than structure, shows the mass is not taking up the radiotracer — it is metabolically dead. The tumor on CT is scar. No further chemotherapy is needed. A functional signal answered a question no anatomic image could: not *is there a mass?* but *is the mass alive?*

Now the failure mode. Three months later the man develops a fever and a new PET shows a bright, FDG-avid lymph node. The reflex is to call it relapsed lymphoma and restart chemotherapy. But FDG does not measure cancer. It measures glucose uptake — and inflammation and infection light up FDG just as brightly as tumor. The fever suggests infection. Treating the bright spot as cancer without confirming it could mean toxic chemotherapy for an infected node. PET's signal is powerful and dangerously easy to over-read.

This chapter is about what the radiotracer actually measures, and the gap between "it lights up" and "it is cancer."

---

## How PET forms an image

Tag a biological molecule with a radioactive atom, inject it, and let it accumulate wherever that molecule is used. The radioactivity announces its location by emitting paired signals that the scanner triangulates.

The physics is specific and worth understanding precisely. A radioactive isotope in the tracer decays by emitting a **positron** — a positive electron. The positron travels only a short distance before meeting an ordinary electron. The two annihilate each other, converting their combined mass into two gamma-ray photons that fly off in exactly opposite directions — 180 degrees apart, each carrying 511 keV of energy. A ring of detectors around the patient records pairs of photons arriving at the same instant. This is **coincidence detection**: when two detectors fire simultaneously, the annihilation event must have occurred somewhere along the line connecting them. Collect millions of such lines and a computer reconstructs a three-dimensional map of where the tracer concentrated.

<!-- → [DIAGRAM: PET signal chain — isotope decay emits a positron → positron annihilates with an electron → two 511 keV photons emitted back-to-back at 180° → detector ring records the coincident pair → many lines reconstruct the activity map. Include FDG half-life (~110 min) and the trapped-glucose mechanism inset.] -->

PET does not measure structure. It measures where a biological process is happening. The image is a map of activity. This is why PET is *functional* imaging — it is the complement, not the competitor, to the anatomic imaging of the previous chapters.

The coarseness follows from the physics: the positron travels a small but nonzero distance before annihilating, and that travel smears the apparent location of the event. Resolution is roughly **4 to 6 mm** — the coarsest of all clinical modalities. A PET image cannot distinguish structures separated by less than half a centimeter. A CT can resolve half a millimeter. An MRI is between them. The inverse relationship between functional richness and spatial precision that runs through this entire book appears here in its starkest form.

---

## FDG: tracing a tumor's metabolism

The most widely used tracer is **fluorodeoxyglucose (FDG)** — a glucose molecule with a radioactive fluorine-18 atom substituted at one position. Cells take up FDG through their normal glucose transporters and phosphorylate it, but the modified molecule cannot proceed further through glycolysis. It is **trapped** inside the cell. The more glucose a cell consumes, the more FDG it accumulates.

Cancer cells characteristically consume glucose at elevated rates — the Warburg effect described in earlier chapters. They take up more FDG than most normal tissue and appear as bright spots against a darker background. This makes FDG sensitive for many common cancers: lymphoma, lung, breast, colon, head and neck, and others.

Fluorine-18 has a half-life of about 110 minutes — long enough to synthesize the tracer, inject it, wait for it to distribute, and scan, short enough that the radioactivity largely clears within hours. The short half-life is also a logistical constraint: fluorine-18 is produced in a cyclotron and decays quickly, so it must be made at or near the facility where it will be used. PET cannot be practiced everywhere; it requires either an on-site cyclotron or proximity to a production facility that can deliver fresh tracer within hours.

---

## What FDG misses, and what falsely lights it up

Because FDG measures glucose uptake rather than malignancy, it misleads in two directions, and being clear about both is essential before ordering a scan.

**False positives.** Anything that consumes glucose heavily will accumulate FDG. Inflammation and infection are the most clinically important sources of false-positive PET signal. Active inflammatory sites — healing surgical wounds, granulomatous disease, recently irradiated tissue, infected nodes — take up FDG indistinguishably from tumor at the resolution the scanner provides. Brown adipose tissue, activated by cold, is intensely FDG-avid and can create confusing uptake in the neck and mediastinum. This is the opening case's trap: a feverish patient with an FDG-avid node is as likely to have an infected node as a relapsed lymphoma, and the PET signal alone cannot tell the difference.

**False negatives.** Not all cancers are metabolically hyperactive. Well-differentiated thyroid carcinoma, many prostate cancers, indolent lymphomas, and mucinous tumors often take up too little FDG to appear bright against background. A negative FDG-PET in a patient whose cancer type is known to be FDG-poor is not reassuring. It means only that the metabolic signal was not there — not that the cancer was not there.

A combined **PET/CT** delivers approximately 25 millisieverts of radiation — roughly double a body CT and a meaningful dose in absolute terms, though small compared with the dose of a therapeutic course. This is not negligible, particularly for younger patients and for surveillance studies that may be repeated. Every PET scan ordered should have a specific question that the scan can plausibly answer.

---

## Why PET must be fused with anatomy

PET's coarse resolution forces a design choice. A bright spot at 4 to 6 mm resolution says that metabolic activity is *here, approximately* — but it cannot say with sufficient precision which anatomical structure the activity occupies. Is the bright spot in a lymph node, or in adjacent bowel, or in overlying muscle? In the chest, is it in the lung or mediastinum?

This is why PET is fused with anatomic imaging. **PET/CT** combines the functional map with a high-resolution CT in a single examination, so the computer overlays the two images: the PET tells you what is active, the CT tells you exactly where. **PET/MRI** does the same with an MRI, providing better soft-tissue contrast at the cost of longer acquisition time.

Hybrid imaging is not a luxury added to make the scan look better. It is the direct consequence of PET's position on the resolution ladder. Without the anatomic overlay, PET is a map without streets — you can see that something is happening, but you cannot navigate to it.

---

## SPECT: PET's lower-resolution cousin

**Single-photon emission computed tomography (SPECT)** is the related nuclear-imaging technique. Instead of detecting paired annihilation photons, SPECT images isotopes that emit single gamma photons directly, using a rotating gamma camera. It is more widely available and cheaper than PET, but provides lower resolution and somewhat lower sensitivity.

The most familiar SPECT application in oncology is the **bone scan**: a technetium-99m-labeled phosphonate accumulates in areas of bone remodeling, flagging bone metastases. The bone scan is less specific than PET — fractures, arthritis, and healing injuries also remodel bone — but it is inexpensive, broadly available, and does not require a cyclotron. For bone metastases from prostate cancer and breast cancer, it remains a practical first tool in many settings.

SPECT's physics means it cannot achieve PET's sensitivity for detecting small lesions. Where PET uses coincidence detection to precisely locate each annihilation event, SPECT uses physical collimators to accept only photons arriving from specific directions, discarding the majority of emitted photons. The tradeoff between availability and performance is different for SPECT than for PET, and the choice between them is partly logistical.

---

## Target-specific tracers

FDG reads a general property — glucose hunger — that many cancers share with inflamed tissue. The frontier of molecular imaging is tracers aimed at a specific molecule that a particular cancer expresses, narrowing the signal to the cancer's distinctive biology rather than its generic metabolic intensity.

**PSMA PET** targets prostate-specific membrane antigen, a transmembrane protein expressed at high levels on prostate cancer cells. Gallium-68 and fluorine-18 PSMA tracers are FDA-approved for staging and restaging prostate cancer and are dramatically more sensitive than CT, bone scan, or FDG-PET for detecting metastatic and recurrent prostate disease — including the biochemically recurrent cases where PSA rises after surgery but all conventional imaging is negative. The reason: prostate cancer cells express PSMA regardless of their glucose metabolism, and small deposits that would not distort anatomy and are not FDG-avid still concentrate the PSMA tracer against a low background.

**DOTATATE PET** targets somatostatin receptors on neuroendocrine tumor cells. Gallium-68-DOTATATE is more sensitive than the older octreotide scintigraphy it replaced and more specific than FDG for these tumors.

The conceptual step that links molecular imaging to therapeutic oncology is this: **a molecule that identifies a cancer's cells on an imaging study can also be the docking site for a therapeutic agent aimed at those same cells.** The same PSMA that lights up on a diagnostic PET scan is the target for lutetium-177-PSMA-617, a radioligand therapy that delivers a lethal radiation dose to the same cells the scan found. Molecular imaging and targeted therapy become two expressions of the same molecular recognition. This is the logic of **theranostics**, the fusion of therapy and diagnostics around a shared target, covered in the next chapter.

---

## When the right answer is a different tracer

A patient with rising PSA after prostatectomy has, by definition, cancer somewhere — but CT and bone scan show nothing. The plan is to repeat CT with more contrast.

Repeating anatomic imaging is the wrong answer. The recurrence is small — below the threshold for anatomic distortion — and prostate cancer is frequently not FDG-avid, so even a standard FDG-PET may miss it. Pushing harder on signals that the biology evades cannot work. The problem is not image quality; it is signal choice.

The right move switches to a target-specific signal. PSMA PET images the antigen that recurrent prostate cancer cells express, regardless of their glucose metabolism or their size. Even a small deposit concentrates the tracer and produces signal against a dark background, across the whole body in a single study. PSMA PET routinely localizes recurrent prostate cancer that CT, bone scan, and FDG-PET all miss. The disease was always there; only a tracer matched to the cancer's specific molecule could find it.

The limit of this argument: PSMA PET's specificity is also its boundary. A PSMA-low variant of the cancer can hide, just as FDG misses low-glucose tumors. And at 4 to 6 mm resolution, PSMA PET reports that disease is in this region — it cannot resolve a microscopic deposit, count cells, or confirm malignancy without tissue. The tracer narrows the search to a location; it does not replace the biopsy that confirms what is there.

---

## What would change this picture

The central claim is that PET measures a biological proxy — metabolic or molecular activity — not malignancy itself, so a positive PET requires confirmation before treatment, and PET's coarse resolution forces fusion with anatomic imaging. The finding that would revise the first part: a tracer or combination validated to distinguish malignant from benign uptake prospectively, with specificity high enough to replace biopsy across tumor types. Total-body PET, dual-tracer approaches, and kinetic modeling are advancing toward better specificity, but none has yet crossed the threshold of replacing tissue confirmation as a clinical standard. For the resolution argument: if detector and reconstruction advances pushed PET resolution toward 1 mm, the dependence on fusion with CT or MRI for precise localization would weaken. Neither result is in hand.

---

## Still open

How specific a tracer can become before specificity becomes a liability is genuinely unsettled. A tracer perfectly specific to PSMA is blind to PSMA-low prostate cancer variants, just as FDG is blind to glucose-poor tumors. As cancers are increasingly imaged by single-molecule tracers, the false-negative risk from target heterogeneity grows. The optimal balance between generality and specificity depends on the cancer and the clinical question.

Whether earlier, more sensitive molecular detection actually saves lives is incompletely answered for several applications. PSMA PET finds recurrence sooner and more often than conventional imaging. Finding disease earlier is not the same as helping the patient live longer or better. Whether the added sensitivity translates into mortality benefit, rather than earlier knowledge with the same eventual outcome, is being studied but not settled.

Whether theranostics will blur the line between imaging and therapy is a question the next chapter addresses directly. If the same molecular target is imaged and then treated with a paired radioligand, the act of imaging is simultaneously the beginning of treatment planning, and evaluating the safety and benefit of the combined tool requires different frameworks than evaluating either component alone.

---

## LLM Exercises

1. **(Signal chain)** Walk through the PET signal chain in order: name what the isotope emits, what happens when it meets an electron, how many photons result and in what geometric relationship, how the detector ring uses them to locate the source, and why this makes PET a functional rather than anatomic modality. Then explain in one sentence why resolution is 4 to 6 mm rather than millimeter-scale like CT.

2. **(Half-life consequences)** FDG has a half-life of approximately 110 minutes. A dose is calibrated at 8:00 a.m. Compute roughly how much radioactivity remains at noon. Explain why this half-life means FDG must be produced near the scanner rather than shipped from a central facility, and describe one practical consequence this has for access to PET imaging.

3. **(Tracer selection)** For each scenario, choose between FDG-PET, PSMA PET, and DOTATATE PET, justify by the molecular target and the cancer's biology, and name one tracer that would be a poor choice and explain what its signal would miss: (a) staging an aggressive lymphoma; (b) localizing biochemically recurrent prostate cancer with a normal CT; (c) imaging metastatic neuroendocrine tumor.

4. **(Fusion logic)** PET resolution is 4 to 6 mm and MRI resolution is approximately 1 mm. Explain why this resolution gap is the reason PET and MRI are combined into PET/MRI rather than used as competitors. What does each modality contribute to the fused image, and what would be lost by using either alone?

5. **(Opening case dissent)** The team in the opening case is about to restart chemotherapy because of a new FDG-avid lymph node in a patient with fever. Write a one-paragraph dissent: state precisely what the FDG signal establishes and what it does not, name the two most likely benign explanations given the clinical context, specify the next step that would distinguish relapse from infection, and explain why treating the proxy (glucose uptake) as the thing (cancer) is the error to avoid.

---

## References

- Phelps, M. E. (2000). PET: the merging of biology and imaging into molecular imaging. *Journal of Nuclear Medicine*, 41(4), 661–681.
- Wahl, R. L., et al. (2009). From RECIST to PERCIST: evolving considerations for PET response criteria in solid tumors. *Journal of Nuclear Medicine*, 50(Suppl 1), 122S–150S.
- Hofman, M. S., et al. (2020). Prostate-specific membrane antigen PET-CT in patients with high-risk prostate cancer before curative-intent surgery or radiotherapy (proPSMA). *Lancet*, 395(10231), 1208–1216.
- Krenning, E. P., et al. (1993). Somatostatin receptor scintigraphy with [111In-DTPA-D-Phe1]- and [123I-Tyr3]-octreotide: the Rotterdam experience with more than 1000 patients. *European Journal of Nuclear Medicine*, 20(8), 716–731.
- NCI. *Theranostics and AI in Cancer Precision Medicine* (2023). https://www.cancer.gov/about-nci/organization/cbiit/news-events/blog/2023/theranostics-and-ai-next-advance-cancer-precision-medicine
- NCI. *Cancer Imaging Basics.* https://dctd.cancer.gov/research/research-areas/imaging/basics
