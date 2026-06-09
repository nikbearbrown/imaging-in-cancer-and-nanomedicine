# Theranostic Imaging

## Learning Objectives

After working through this chapter you should be able to:

- **Explain** how a theranostic agent uses the *same* molecular targeting event for both imaging and therapy, and why that coupling changes the logic of patient selection.
- **Distinguish** the physical signal, resolution, and biological question answered by a diagnostic PET scan versus a therapeutic radioligand, even when the two share a targeting molecule.
- **Compare** beta-emitter and alpha-emitter radioisotopes in terms of particle energy, range, linear energy transfer, and the clinical situations each suits.
- **Evaluate** a patient-selection decision using a PSMA PET scan, including the thresholds and uncertainties that make "PSMA-positive" a contestable category.
- **Critique** the claim that target expression on a scan guarantees therapeutic response.

## Opening Case

A 71-year-old man has metastatic castration-resistant prostate cancer. He has already progressed through androgen-receptor pathway inhibition and taxane chemotherapy. His oncologist wants to offer him lutetium-177-PSMA-617 (Pluvicto), a radioligand therapy approved by the FDA in 2022. But first the patient gets a gallium-68-PSMA-11 PET scan.

The scan lights up brightly at most of his bone and lymph-node metastases. But one liver lesion, clearly visible on his recent CT, shows almost no PSMA signal. The tumor board pauses. Here is the problem in miniature: the therapy will be delivered *only* to cells that express PSMA, because the drug finds its targets the same way the scan did. The CT sees a 2-centimeter mass. The PSMA PET sees whether that mass will take up the drug. These are two different measurements of the same lump, and they disagree.

If the team treats based on the CT — "there's cancer, treat the cancer" — they may irradiate the PSMA-positive sites while the PSMA-negative liver lesion grows unchecked. If they treat based on the PET — "treat what the scan can reach" — they accept that one visible tumor will get no therapeutic dose at all. The scan has not just diagnosed disease. It has predicted, lesion by lesion, where the drug will and will not go. The decision the board faces only exists because imaging and therapy are now the same act.

## Core Concepts

### What "theranostic" actually means

Conventional cancer care keeps diagnosis and treatment in separate boxes. You image the tumor with one tool, then treat it with an unrelated drug. Information flows one direction: the scan informs the treatment choice, but the treatment never feeds back through the scan.

A **theranostic agent** ("therapy" + "diagnostic") collapses that separation. The molecule used to *image* the target is the same molecule — or a near-identical sister molecule — used to *deliver therapy* to that target. The single molecular event of target binding drives both the diagnostic signal and the therapeutic payload [NCI, Theranostics and AI in Cancer Precision Medicine].

The cleanest examples are **radioligand theranostics**, and the cleanest of those is PSMA-targeted therapy for prostate cancer.

### The PSMA story, step by step

**Prostate-specific membrane antigen (PSMA)** is a protein that sits in the outer membrane of prostate cancer cells, expressed at high levels on nearly all metastatic prostate cancer and rising with disease aggressiveness [verify]. Crucially, a small molecule can be designed to lock into PSMA's active site. That small molecule is the targeting ligand. What you attach to it decides whether it images or treats.

- Attach a **PET-emitting isotope** — gallium-68 (as gallium-68-PSMA-11, marketed as Locametz/Illuccix) or fluorine-18 (as fluorine-18-DCFPyL/piflufolastat, marketed as Pylarify) — and the ligand becomes a **diagnostic**. The isotope emits positrons; the PET scanner detects the resulting annihilation photons and maps where PSMA is expressed across the whole body [NCI, CT Scans and Cancer Fact Sheet].
- Attach a **therapeutic isotope** — lutetium-177 (as lutetium-177-PSMA-617, Pluvicto) — and the *same ligand* becomes a **therapy**. Lutetium-177 emits beta particles that deposit ionizing radiation into the cells the ligand binds [verify].

So the workflow is: **image to find the target, treat through the same target, image again to confirm delivery and response.** The pivotal VISION trial showed improved overall survival from lutetium-177-PSMA-617 plus standard care versus standard care alone in heavily pretreated patients [verify], and that result drove the 2022 approval.

<!-- → [DIAGRAM: theranostic image-then-treat loop — PSMA ligand core, with gallium-68/fluorine-18 swapped in for PET imaging and lutetium-177 swapped in for therapy; arrows showing image → select → treat → re-image] -->

### Scale and signal: what each step measures

This is the through-line of the whole book. Each step in the theranostic loop is a *different measurement at a different scale*.

- **The diagnostic PET scan.** Physical signal: positron annihilation photons (511 keV each, emitted back-to-back). Resolution: roughly 4–6 mm in clinical PET — coarse by microscope standards, but whole-body. Biological question: *which lesions, anywhere in the body, express enough PSMA to be reached?* It answers a yes/no-per-lesion question across an entire person.
- **The therapy.** Physical signal: none you read out directly — the beta particles do their work over a few millimeters of tissue. Biological question: *can a lethal radiation dose be delivered to the targeted cells?* The same binding event that gave you a bright PET voxel now delivers a dose.

The PET scan is the proxy. The therapy is the thing. The entire theranostic premise is that the proxy predicts the thing — that a bright scan means a treatable lesion. The opening case is exactly where that premise gets tested.

### Beta versus alpha emitters

The therapeutic isotope choice reshapes the whole risk-benefit profile.

**Beta-emitters** release electrons of intermediate energy that travel **millimeters** through tissue. Lutetium-177 is the dominant clinical example; yttrium-90 (higher energy, longer range) and iodine-131 (the classic thyroid-cancer agent) are others. The millimeter range is a feature: a labeled cell irradiates its neighbors too, so **crossfire** can kill nearby tumor cells that don't themselves express the target — helpful when expression is patchy. The cost: lower **linear energy transfer (LET)** — the energy deposited per unit path — means each particle does less lethal DNA damage, and the longer range can spill dose into adjacent normal tissue.

**Alpha-emitters** release helium nuclei (2 protons + 2 neutrons) of very high energy but very short range — **50–100 micrometers**, roughly the width of a few cells. Actinium-225 is the leading clinical candidate; radium-223 (Xofigo, approved 2013) is already used for prostate-cancer bone metastases [verify]. The very high LET means far more lethal DNA damage per particle, which may overcome resistance to beta therapy, and the short range spares tissue just beyond the target. The costs: actinium-225 is hard and expensive to produce, and clinical experience is still limited [contested — see pantry flag: alpha-emitter clinical benefit vs. beta is still being established].

<!-- → [CHART: beta vs. alpha emitter comparison — particle, energy, range in tissue (mm vs. µm), LET, crossfire behavior, with Lu-177 and Ac-225 as exemplars] -->

### Beyond PSMA

The same template has spread. **Lutetium-177-DOTATATE (Lutathera)**, approved 2018 for gastroenteropancreatic neuroendocrine tumors, targets somatostatin receptor type 2 (SSTR2) using an octreotate ligand, with gallium-68-DOTATATE PET as its companion diagnostic [verify]. It was the first modern FDA-approved radioligand theranostic and established the regulatory pathway. Active pipelines target FAP (fibroblast activation protein, on tumor stroma), GRPR, CXCR4, glypican-3, mesothelin, and HER2 [verify].

## Worked Example

**Situation.** Return to the opening case: metastatic castration-resistant prostate cancer, prior taxane and AR-pathway inhibitor, multiple bone and node metastases bright on gallium-68-PSMA-11 PET, and one PSMA-faint liver lesion visible on CT. Should this patient receive lutetium-177-PSMA-617?

**Reasoning — first attempt (the dead end).** The intuitive move is: he has metastatic prostate cancer, Pluvicto treats metastatic prostate cancer, so treat. This reasons from the *diagnosis of disease* to the *use of the drug*. It fails because radioligand therapy is not a disease-level treatment — it is a target-level treatment. The drug deposits its dose only where the ligand binds PSMA. The PSMA-negative liver lesion is, to this drug, invisible and untreatable. Reasoning from "there is cancer" instead of "the target is present here" sets the patient up to progress in the one site the therapy cannot touch, while everyone believes he is being treated.

**Reasoning — corrected.** The actual selection question is set by the labeling and the VISION-style criteria: is there *sufficient PSMA expression* to justify therapy, typically judged on the PSMA PET against reference organs such as the liver [verify]? In the SPLASH/VISION framing, eligibility hinges on PSMA-positive disease with no dominant PSMA-negative lesions, because a discordant lesion — bright on CT, dark on PET — flags disease biology the drug won't reach. The presence of one substantial PSMA-negative lesion is precisely the discordance that should give the board pause.

**Resolution.** The team treats with lutetium-177-PSMA-617 *and* plans separate management for the liver lesion (for example, local therapy or a systemic agent that does not depend on PSMA), and follows with post-therapy imaging to confirm where dose was delivered. They also counsel the patient on expected toxicities driven by *off-tumor* PSMA expression: xerostomia (dry mouth) from PSMA on salivary glands, kidney toxicity from PSMA on renal tubules, and marrow suppression [verify]. The same targeting that makes the drug selective also makes the salivary glands a predictable casualty.

**The lesson.** In theranostics, the scan does not just say "cancer is here." It says "the drug can reach *here*, and not *there*." Patient selection is lesion-level, target-level reasoning — not disease-level reasoning.

**The limit.** PSMA expression on a scan predicts *delivery*, not *response*. A bright lesion still may not shrink — radiation resistance, low absorbed dose, or tumor heterogeneity within the "positive" lesion can all break the chain from binding to benefit. Imaging confirms the drug arrives; it does not guarantee the cancer dies.

## Common Misconceptions

**"If the tumor is on the CT, the radioligand will treat it."** Plausible, because we are trained to think a treatment for a cancer treats all of that cancer. It fails because radioligand therapy is delivered through the targeting ligand, not through bulk uptake. A CT-visible, PSMA-negative lesion receives essentially no therapeutic dose. This is the exact trap in the opening case — treating the *diagnosis* (prostate cancer) rather than the *target* (PSMA-positive cells).

**"A theranostic agent is one drug that both diagnoses and treats at the same time."** Almost — but the imaging and therapeutic versions usually carry *different isotopes* on the same ligand scaffold (gallium-68 or fluorine-18 for PET; lutetium-177 or actinium-225 for therapy). The shared element is the targeting molecule, not a single all-in-one isotope. Conflating them obscures why dosimetry and isotope choice matter so much.

**"Alpha-emitters are simply better than beta-emitters because they hit harder."** They do deposit more lethal damage per particle. But their 50–100 µm range means no crossfire to reach target-negative cells inside a heterogeneous tumor, they are far harder to manufacture (especially actinium-225), and clinical evidence is thinner [contested — see pantry flag]. "Harder hit" is not the same as "better outcome" across all tumors.

**"A bright PSMA PET means the patient will respond."** Expression predicts that the drug can *bind and deliver dose* — a necessary condition, not a sufficient one. Response also depends on absorbed dose, radiosensitivity, and intra-lesional heterogeneity. Confusing target expression with clinical response is the recurring proxy-for-truth error this book keeps flagging.

## Exercises

1. **(Comprehend)** In your own words, explain why a PSMA PET scan and a contrast CT can "see" the same liver metastasis but disagree about whether it should be treated with lutetium-177-PSMA-617. Name the physical signal each modality measures.

2. **(Apply)** A patient has neuroendocrine tumor metastases. The team is considering lutetium-177-DOTATATE. What companion imaging agent confirms the target, what receptor is being targeted, and what single imaging finding would make you *withhold* the therapy? Justify each answer in one sentence.

3. **(Apply+)** A tumor shows strikingly *heterogeneous* PSMA expression on PET — some regions bright, some dark, within the same mass. Argue whether a beta-emitter (lutetium-177) or an alpha-emitter (actinium-225) is the more rational choice for that lesion, and state the specific physical property (range, LET, crossfire) driving your decision. Then name one piece of evidence that would reverse your choice.

4. **(Produce)** Draw the theranostic loop for PSMA prostate cancer as a labeled diagram: the shared ligand scaffold in the center, the imaging isotopes and therapeutic isotopes branching off, and the four workflow steps (image → select → treat → re-image). For each step, annotate the **physical signal**, the **spatial scale**, and the **biological question** it answers. (This forces you to make the scale-dependence explicit.)

5. **(Analyze)** List three off-tumor sites where PSMA is expressed, and predict the toxicity each produces during lutetium-177-PSMA-617 therapy. Explain why the *same* selectivity that makes the drug useful also makes these toxicities unavoidable.

## What Would Change My Mind

The central claim here is that imaging and therapy in a theranostic agent are coupled measurements at different scales — and that target expression on a scan predicts *delivery* but not *response*. What would revise that? A large, well-controlled study showing that response to lutetium-177-PSMA-617 is essentially **independent** of baseline PSMA PET intensity — that low-expressing and high-expressing lesions respond at indistinguishable rates — would force a rethink. It would imply either that the imaging signal is not actually tracking the therapeutic delivery (the scan measures something other than what the drug binds), or that delivered dose is so dominated by factors downstream of binding that pre-treatment imaging adds little selection value. Some real-world series already hint that PSMA PET thresholds for patient selection are imperfect predictors [contested — see pantry flag]; a definitive negative result on the expression-response link would not kill theranostics, but it would dethrone the scan from its role as gatekeeper.

## Still Puzzling

- **How "positive" is positive enough?** The threshold for "PSMA-positive disease" on PET — what intensity, relative to which reference organ, over what fraction of lesions — is not settled, and different trials used different criteria. Where exactly is the line, and does it depend on the isotope you plan to treat with?
- **Can we predict response, not just delivery?** Dosimetry (measuring absorbed radiation dose per lesion from post-therapy imaging) might close the gap between "the drug arrived" and "the tumor died." It is not yet routine. Will personalized dosimetry become standard, and would it actually improve outcomes?
- **Will alpha-emitters earn their promise?** Actinium-225-PSMA looks compelling for beta-resistant disease, but supply is scarce and the evidence is early. Does the higher LET translate into better survival, or mainly into different toxicities?
- **Does the model generalize?** PSMA and SSTR2 are unusually clean targets — high, near-uniform expression. Will the FAP, CXCR4, and GRPR programs reach the same clarity, or are these the lucky exceptions?

## References

- NCI, "Theranostics and AI: The Next Advance in Cancer Precision Medicine." https://www.cancer.gov/about-nci/organization/cbiit/news-events/blog/2023/theranostics-and-ai-next-advance-cancer-precision-medicine
- NCI, "CT Scans and Cancer Fact Sheet" (CT, PET/CT, radiopharmaceuticals, PSMA imaging agents). https://www.cancer.gov/about-cancer/diagnosis-staging/ct-scans-fact-sheet
- NCI, "Molecular probes for the in vivo imaging of cancer." https://pmc.ncbi.nlm.nih.gov/articles/PMC3407672/
- NCI, "Cancer and Nanotechnology." https://www.cancer.gov/sites/ocnr/cancer-nanotechnology
- Source chapter: "Theranostics and Emerging Cancer Nanotechnology" (cba-48), Humanitarians AI cancer series.
- VISION trial of lutetium-177-PSMA-617 in metastatic castration-resistant prostate cancer [verify primary citation against NEJM Sartor et al. 2021 before publication].

---

## Prompts

<!-- This section is populated automatically by the Cowork enrichment
     pass. Each D3 figure generated in this chapter gets an entry here:
     the figure number, a short title, and a ready-to-paste prompt
     that produces a close approximation of that figure.

     Prerequisites: paste CLAUDE.md and DESIGN.md from the brutalist/
     folder before each prompt, or load them into your Claude project
     context once and reference them by name.
-->

*No figures have been generated for this chapter yet.*
*Run the Cowork enrichment pass to populate this section.*
