# Chapter 5 — Theranostic Imaging
*When imaging and therapy become the same act — and what it means to select a patient lesion by lesion rather than diagnosis by diagnosis.*

The PSMA PET scan maps the patient's disease across his entire skeleton and lymphatic system in a single acquisition. Most of his bone metastases glow. Most of his lymph node lesions glow. The radiologist's report notes intense PSMA expression at all but one site.

The one exception is a 2-centimeter mass in the liver, visible on the staging CT as clearly as the others. On the CT it looks like any other metastasis. On the PSMA PET it is nearly dark.

This discordance is not a technical error and not an ambiguity in the reporting. It is biological information about a specific lesion: this tumor cell population does not express significant PSMA. And it is information that matters, because the therapy the team is considering — lutetium-177-PSMA-617 — works by attaching a radioactive isotope to a molecule that binds PSMA. The drug finds its targets the same way the scan did. Where the scan lit up, the drug will go. Where the scan was dark, the drug will not.

The CT shows cancer. The PSMA PET shows where the drug can reach. These are two different measurements of the same body, and they disagree about one lesion. The board has to decide how to treat a patient who has both PSMA-positive disease that a radioligand will reach and PSMA-negative disease that it will not. The clinical problem only exists because imaging and therapy are now, in theranostics, the same molecular act.

---

### What makes an agent theranostic

Conventional oncology separates imaging and treatment into distinct tools with distinct molecules. You choose a CT protocol to localize the disease. You prescribe a drug to treat it. Information flows in one direction: the scan informs the treatment, and the treatment is administered independently of how the scan was obtained.

A **theranostic agent** collapses this separation. The molecule used to image the target is the same molecule — or a near-identical structural analog — used to deliver therapy to that target. The binding event that places the imaging signal in a lesion is the same binding event that later places the therapeutic payload there. Imaging and therapy are not two separate decisions connected by a clinical judgment call. They are two expressions of the same molecular recognition event, differing only in what is attached to the targeting molecule.

The logic of patient selection changes completely in this framework. A patient selected for a conventional chemotherapy on the basis of their diagnosis — they have metastatic prostate cancer — is selected because the drug broadly targets rapidly dividing cells, and their cancer has those cells. A patient selected for a PSMA radioligand therapy is selected because their specific tumors, in their specific body, express the molecular target the drug binds. The selection is not diagnosis-level; it is target-level. And target expression must be confirmed by the same molecular imaging that will guide the therapy — not assumed from the histological diagnosis.

---

### The PSMA system: one ligand, two isotopes, two jobs

**Prostate-specific membrane antigen** is a transmembrane protein expressed at high levels on prostate cancer cells, rising in concentration with disease aggressiveness. It is an enzyme — a carboxypeptidase — with an active site that small molecules can be designed to occupy with high affinity. That active site is the target: a molecule built to fit into it will bind to prostate cancer cells wherever they are in the body.

What happens next depends only on what you attach to the targeting molecule.

Attach a **positron-emitting isotope** — gallium-68, with a half-life of 68 minutes, or fluorine-18, with a half-life of 110 minutes — and the agent is a diagnostic. The isotope decays by emitting a positron that almost immediately annihilates with a nearby electron, producing two gamma-ray photons traveling in exactly opposite directions at 511 keV each. A PET scanner detects these coincident photons and uses the timing information to localize the source to a point along the line connecting the two detectors. Over a 20-minute acquisition the system accumulates enough events to reconstruct a three-dimensional map of where the targeting molecule has bound — a map of PSMA expression across the whole body. The resolution is roughly 4 to 6 millimeters in clinical scanners: coarse enough that individual cells are invisible, but fine enough to identify discrete lesions and compare their uptake to a reference organ. This is gallium-68-PSMA-11 or fluorine-18-DCFPyL — the diagnostic, the scan that lit up the patient's skeleton and nodes in the opening case.

Attach a **therapeutic isotope** — lutetium-177, with a half-life of 6.6 days — and the same targeting molecule becomes a therapy. Lutetium-177 decays by emitting a beta particle: an electron ejected from the nucleus at moderate energy that travels a few millimeters through tissue, ionizing DNA and other molecules along its path. The binding event that would have produced a PET voxel now deposits a radiation dose. Cells expressing PSMA receive a high local radiation dose from the lutetium-177 carried to them by the ligand. Cells not expressing PSMA are not targeted. This is lutetium-177-PSMA-617 — Pluvicto — approved by the FDA in 2022 for metastatic castration-resistant prostate cancer following the VISION trial.

The workflow is a loop: image with the diagnostic version to identify and measure PSMA expression, select the patient based on the imaging findings, treat with the therapeutic version targeting the same sites, then image again — either with a repeat diagnostic scan or by taking advantage of the fact that lutetium-177 also emits a low-energy gamma ray that allows post-therapy scintigraphy — to confirm where the therapeutic dose was delivered and assess response.

<!-- → [DIAGRAM: theranostic loop for PSMA therapy. Center: schematic of the PSMA ligand molecule. Left branch: gallium-68 or fluorine-18 attached, labeled "diagnostic isotope — PET imaging." Right branch: lutetium-177 or actinium-225 attached, labeled "therapeutic isotope — radioligand therapy." Below: circular workflow arrow labeled: (1) image — identify PSMA-expressing lesions; (2) select — confirm eligibility, identify discordant lesions; (3) treat — administer therapeutic version; (4) re-image — confirm dose delivery, assess response. Each workflow step annotated: physical signal (511 keV gamma for PET; beta emission for therapy; gamma for post-therapy scintigraphy), spatial scale (4–6 mm PET resolution; millimeter range beta particle; organ-level post-therapy scan), and biological question (where does PSMA expression exist? / does the drug reach these cells?).] -->

---

### What each step in the loop is actually measuring

Every step in the theranostic loop is a measurement. They measure different things at different scales, and understanding what each one measures — and what it does not — is the discipline the opening case demands.

**The diagnostic PET scan** measures the spatial distribution of PSMA expression across the whole body at the resolution of clinical PET — roughly 4 to 6 millimeters per voxel. The physical signal is positron annihilation gammas. The biological question is: which lesions, wherever they are, bind this targeting molecule at a concentration high enough to produce a signal above background? The scan answers a per-lesion yes/no question across an entire patient. "Yes" means the lesion will take up the therapeutic version of the same agent; "no" means it will not.

**The therapeutic delivery** is not itself an imaging step, but it is still a measurement of sorts — the drug is measuring the target expression of every cell it encounters by binding to those that express PSMA and sparing those that do not. The physical event is beta particle emission from lutetium-177. The scale is millimeters of tissue irradiated around each PSMA-expressing cell. The biological question is: can a lethal radiation dose be deposited in the targeted cells? This is the step the scan predicts but cannot guarantee.

**Post-therapy scintigraphy or SPECT/CT** uses the gamma emissions from lutetium-177 to confirm where the therapeutic dose went. The resolution is coarser than PET — 1 to 2 centimeters — but the image is direct evidence of where the drug actually delivered dose, not just a prediction from the pre-therapy scan.

The PET scan is the proxy. The therapy is the thing. The theranostic premise is that the proxy predicts the thing with enough reliability to select patients and guide decisions. The opening case is precisely the case where that premise is challenged: the liver lesion is bright on CT, dark on PET, and the question is whether the discordance is clinically meaningful or a noise artifact.

---

### Beta and alpha: the isotope choice reshapes the risk-benefit profile

The choice of therapeutic isotope is not incidental. It determines the range of tissue irradiated, the intensity of DNA damage per particle, and the clinical profile of both efficacy and toxicity.

**Beta emitters** release electrons at intermediate energies that travel a few millimeters through tissue — roughly 1 to 10 millimeters depending on the specific isotope and its energy spectrum. Lutetium-177 is the dominant clinical beta emitter in radioligand therapy. Yttrium-90 has higher energy and longer range. Iodine-131, the oldest radioligand therapeutic, treats thyroid cancer using the thyroid's natural iodine uptake as a targeting mechanism.

The millimeter range of beta particles creates **crossfire**: a PSMA-expressing cell irradiates neighboring cells within a few millimeters, including cells that might not themselves express the target. In a tumor with heterogeneous PSMA expression — some cells positive, some negative — the crossfire from the positive cells irradiates the negative cells nearby. This is a feature in heterogeneous tumors, not a flaw. The range of beta particles means "targeted" therapy still has a neighborhood effect.

The cost is that those same millimeters of range also irradiate normal tissue adjacent to the tumor. Beta radiation from lutetium-177 bound to PSMA-expressing salivary gland cells can damage the surrounding gland. Beta radiation from lutetium-177 bound to PSMA-expressing renal tubular cells can damage the kidney. The targeting reduces but does not eliminate off-tumor irradiation.

**Alpha emitters** release helium nuclei — two protons and two neutrons — at very high energies. The range in tissue is 50 to 100 micrometers: the width of roughly five to ten cells. Actinium-225 is the therapeutic alpha emitter in active clinical development for PSMA-targeted therapy. Radium-223, the approved alpha-emitting agent for prostate cancer bone metastases, targets bone-surface calcium rather than a receptor, but demonstrates the clinical proof of concept.

The 50-to-100-micrometer range means almost no crossfire: the alpha particles deposit their energy within the targeted cell and its immediate neighbors, sparing everything beyond that radius. The tradeoff is that a heterogeneous tumor with PSMA-negative cells cannot rely on the neighborhood effect to kill them — each cell needs to be directly targeted.

The very short range also means very high **linear energy transfer** — energy deposited per unit path length — roughly 20 times higher for alpha particles than beta particles at comparable energies. High LET produces more complex, clustered DNA damage that is harder for cells to repair and more likely to produce lethal double-strand breaks even in cells that are otherwise radioresistant. This makes alpha therapy potentially more effective against tumors that have developed resistance to beta-emitter therapy, where the cells may have upregulated DNA repair capacity.

The clinical evidence for actinium-225-PSMA is promising in small series and early trials but not yet established in randomized outcome data at the level of the VISION trial. The supply of actinium-225 is a genuine constraint — it is a cyclotron-produced isotope with limited global production capacity — and manufacturing complexity is higher than for lutetium-177. The claim that alpha emitters are "simply better" than beta emitters overstates the current evidence; they are better suited to specific biological situations and may be particularly valuable for beta-resistant disease, but the general clinical advantage is not yet proven.

<!-- → [CHART: beta versus alpha emitter comparison. Four columns: isotope class; representative isotope; range in tissue; linear energy transfer (qualitative: moderate vs. high); crossfire behavior (yes/no); clinical maturity. Rows: beta (lutetium-177: mm range, moderate LET, yes crossfire, approved); alpha (actinium-225: 50–100 µm range, high LET, minimal crossfire, investigational). Below chart: brief note on radium-223 as the approved alpha emitter for bone disease.] -->

---

### Beyond PSMA: the template and where it generalizes

The PSMA system succeeded as a theranostic because the target has properties that make the template work: PSMA is expressed at high and relatively uniform levels on nearly all metastatic prostate cancer, the small-molecule binding affinity is high enough to achieve good tumor-to-background ratios on imaging, and the same binding event that produces a clean scan also delivers a meaningful radiation dose.

**Lutetium-177-DOTATATE (Lutathera)**, approved in 2018, extends the template to gastroenteropancreatic neuroendocrine tumors. The targeting molecule is octreotate, which binds somatostatin receptor type 2 — expressed at high levels on well-differentiated neuroendocrine tumors. Gallium-68-DOTATATE PET is the companion diagnostic. The NETTER-1 trial established clinical benefit. Lutathera was the first modern FDA-approved radioligand theranostic and established the regulatory pathway that PSMA therapy followed.

The pipeline of new radioligand targets is active. Fibroblast activation protein, expressed on cancer-associated fibroblasts in the tumor stroma rather than on the cancer cells themselves, is being explored as a broadly applicable target across multiple solid tumors. Gastrin-releasing peptide receptor, CXCR4, glypican-3, and mesothelin are in various stages of development. Whether any of these will replicate the PSMA story — clean, high-level target expression, good imaging agent, tractable pharmacology — remains to be demonstrated. PSMA and SSTR2 may be unusually favorable targets rather than representative ones.

---

### What a positive scan does and does not guarantee

The opening case's liver lesion is the right object to keep in mind as a corrective to overconfidence about theranostic selection.

A positive PSMA PET scan means: this lesion expresses PSMA at a concentration high enough to produce a signal above background at the resolution of clinical PET (roughly 4 to 6 millimeters). It means the targeting molecule will bind there. It means the therapeutic isotope, if attached to that molecule, will be delivered to cells in that lesion.

It does not mean: the lesion will respond. It does not mean the cells in that lesion are radiosensitive. It does not mean the absorbed dose delivered will exceed the threshold for cell kill. It does not mean the cells are homogeneously PSMA-positive throughout the lesion — a lesion that is bright on PET can contain PSMA-negative subclones that will survive irradiation of their PSMA-positive neighbors, especially if the beta particle range is insufficient to create crossfire across the diameter of the negative cluster.

The relationship between PSMA PET signal intensity and therapeutic response is imperfect. Patients with very high PSMA expression on pre-therapy PET do not uniformly have the best outcomes. Some bright lesions respond poorly; some moderately bright lesions respond well. The correlation exists in aggregate but is not deterministic at the individual lesion level. A bright scan confirms delivery; it does not guarantee effect.

The opening case's discordant liver lesion is a harder version of the same problem. That lesion is PSMA-negative by PET — but "PSMA-negative" at PET resolution means the signal is below the detection threshold, not that no PSMA-expressing cells are present. A lesion that would have marginal therapeutic response may still have some subpopulations accessible to the drug. The clinical judgment call in the opening case requires integrating: the size and growth rate of the discordant lesion, the overall PSMA burden at responsive sites, the availability of alternative systemic or local therapies for the discordant site, and the patient's overall trajectory and goals.

The scan does not make that decision. It provides the measurement. The decision belongs to the clinical team interpreting what that measurement means for this patient's specific biology.

---

### Off-tumor PSMA: why the targeting creates predictable toxicity

PSMA is not expressed exclusively on prostate cancer. It is also expressed on the proximal tubular cells of the kidney, on normal salivary and lacrimal glands, on the small intestine, and at lower levels in several other normal tissues. The therapeutic ligand binds to PSMA wherever PSMA is expressed. The salivary glands are not safe because the therapy is "targeted to cancer" — they express the same target.

The salivary gland dose from lutetium-177-PSMA-617 produces **xerostomia** — dry mouth — as a significant toxicity in a meaningful fraction of treated patients. This is not an unexpected or unpredicted side effect; it is the mechanistic consequence of PSMA expression in salivary tissue receiving beta irradiation from a PSMA-targeted drug. Similarly, renal tubular PSMA expression creates kidney dose, contributing to nephrotoxicity and making renal function a monitoring priority during therapy.

This is, in a sense, the inverse of the therapeutic principle: the same molecular selectivity that concentrates the drug at the tumor concentrates it at every PSMA-expressing cell in the body. The therapeutic window exists not because normal tissues are completely spared — they are not — but because tumor cells typically express PSMA at substantially higher levels than normal tissues, producing a ratio of tumor dose to normal tissue dose that is, on average, favorable. The salivary gland and kidney are the tissues where that ratio is least favorable, which is why their dose becomes the practical constraint on how much therapy can be delivered.

Predicting and managing these toxicities requires knowing not just where the tumor is, but where PSMA expression in normal tissue will concentrate dose. Dosimetry — calculating the absorbed dose to specific organs from post-therapy imaging — is the tool that would make this prediction individualized. It is not yet routine, but the argument for it is exactly the argument for personalized dosing in any pharmacological system: the distribution of the drug matters as much as the quantity administered, and the distribution varies between patients.

---

## Exercises

**Warm-up**

1. *(Recall — difficulty: low)* In your own words, explain why a PSMA PET scan and a contrast CT can both detect the same liver metastasis but reach opposite conclusions about whether it should receive lutetium-177-PSMA-617. Name the physical signal each modality measures and state what biological property each measures. *What this tests: the modality-specific measurement distinction before applying it to theranostic decision-making.*

2. *(Recall — difficulty: low)* State three differences between beta-emitter and alpha-emitter radioligand therapy. For each difference, state whether it is an advantage or disadvantage and in what biological situation it becomes clinically important. *What this tests: the physical properties of each emitter type and their clinical implications.*

3. *(Recall — difficulty: low)* What is the theranostic loop, and what does each step measure? For the PSMA prostate cancer system, name the diagnostic isotope(s), the therapeutic isotope, the target protein, and the companion imaging agent used for patient selection. *What this tests: the structural logic of the theranostic approach and the specific PSMA system components.*

**Application**

4. *(Apply — difficulty: medium)* A patient with gastroenteropancreatic neuroendocrine tumor is being considered for lutetium-177-DOTATATE. What companion imaging agent is used for patient selection, what receptor is targeted, and what specific imaging finding would make you withhold the therapy? Then explain why "this patient has a neuroendocrine tumor" is not sufficient by itself to prescribe lutetium-177-DOTATATE. *What this tests: generalization of the PSMA theranostic logic to the DOTATATE system and the diagnosis-versus-target distinction.*

5. *(Apply — difficulty: medium)* A tumor shows heterogeneous PSMA expression on PET — some regions intensely bright, some moderately bright, some faint — within a single metastatic lymph node. Argue whether lutetium-177 (beta emitter, millimeter range) or actinium-225 (alpha emitter, 50–100 µm range) is the more mechanistically rational choice for this specific lesion, using the crossfire concept. State one piece of evidence that would reverse your choice. *What this tests: application of beta versus alpha emitter properties to a specific heterogeneity scenario.*

6. *(Apply — difficulty: medium)* A patient receives lutetium-177-PSMA-617 and develops grade 2 xerostomia (significant dry mouth affecting quality of life). Explain mechanistically why this toxicity occurred despite the therapy being "targeted to prostate cancer cells," using the concept of off-tumor PSMA expression. Then state what pre-treatment information, if available, might have predicted the severity of this toxicity. *What this tests: the off-tumor PSMA toxicity mechanism and the concept of individualized dosimetry.*

**Synthesis**

7. *(Synthesize — difficulty: high)* Draw or describe the complete theranostic loop for PSMA prostate cancer therapy. For each of the four steps (image, select, treat, re-image), state: (a) the physical signal; (b) the spatial scale and resolution; (c) the biological question the step answers; and (d) one specific failure mode — a situation where the step's measurement could be misleading or insufficient. Conclude with a statement about what the loop as a whole can and cannot establish about whether a patient will benefit from treatment. *What this tests: integration of the four-step loop with explicit failure-mode analysis at each step.*

8. *(Synthesize — difficulty: high)* Compare the clinical evidence base for lutetium-177-PSMA-617 and actinium-225-PSMA therapy at the time this chapter was written. For each, state the level of evidence (randomized trial, phase II, retrospective series), the patient population studied, and the primary outcome demonstrated. Then explain why the actinium-225 data, however promising, cannot yet support a claim of superiority over lutetium-177, and what specific trial design would be required to establish that claim. *What this tests: evidence-level reasoning applied to a live clinical controversy, with explicit specification of the evidentiary standard needed to change practice.*

**Challenge**

9. *(Challenge — difficulty: high)* The theranostic premise — that target expression on a pre-therapy scan predicts therapeutic response — is foundational to patient selection in radioligand therapy. Yet the relationship between PSMA PET signal intensity and clinical response to lutetium-177-PSMA-617 is imperfect: some high-expressing patients respond poorly; some moderate-expressing patients respond well. Evaluate whether this imperfection undermines the theranostic selection logic or is compatible with it. Specifically: (a) distinguish the claims "the scan predicts drug delivery" and "the scan predicts clinical response," and evaluate whether the imperfection challenges one or both; (b) identify at least three biological mechanisms that could produce poor response despite high PSMA expression; (c) propose what additional pre-treatment measurement — beyond PSMA PET signal intensity — would most improve response prediction; and (d) evaluate whether post-therapy dosimetry (measuring absorbed dose per organ and per lesion from post-therapy imaging) should become a routine component of radioligand therapy management, and what evidence would be required to demonstrate that dosimetry-guided treatment adaptation improves outcomes. Be explicit about what is established versus speculative, and identify the single most important unanswered question in theranostic patient selection. *What this tests: critical analysis of the proxy-versus-response distinction, mechanistic reasoning about response heterogeneity, and the evidence standards for practice change in an active clinical area.*
