# Chapter 8 — Histology, IHC, and Multiplex Spatial Profiling
*Why a brown stain is not the same as a positive result — and how a treatment decision lives and dies on which bin a pathologist puts a continuous signal into.*

The biopsy comes in. The clinical question is sharp: does this breast cancer overexpress HER2? If yes, the patient gets trastuzumab and the family of HER2-targeted drugs that have transformed the prognosis of HER2-positive disease. If no, those drugs are not indicated.

The pathologist runs immunohistochemistry. An antibody specific to HER2 binds wherever the protein sits in the tissue, and a detection system deposits a brown precipitate at those sites. She looks at the slide. The tumor cell membranes show brown.

Now the harder part: the scoring system is **0, 1+, 2+, 3+**. A strong, complete, circumferential brown rim on the membranes of more than 10 percent of tumor cells is 3+ — HER2-positive, treat. Faint or incomplete staining is 0 or 1+ — negative, don't treat. This slide shows moderate staining that is somewhat patchy. That is 2+ — equivocal — the bin that means the IHC alone cannot decide, and the case has to go to a gene amplification test.

Here is the thing to hold onto. The brown precipitate is physically real — antibody bound to protein, enzyme turning a substrate into colored product. But turning "this shade of brown, this complete, in this fraction of cells" into "2+ versus 3+" is a judgment call on a continuous measurement forced into four discrete bins. Two pathologists can look at the same equivocal slide and give different scores. A patient's access to a targeted therapy can turn on which side of a threshold a single observer places a continuous stain. The slide measured a protein. The score is an interpretation. The interpretation — not the protein — is what determines the treatment.

---

### Before any stain: what happens to the tissue

A tissue sample does not arrive at a stain directly. Before the antibody binds anything, the tissue must be preserved, embedded, and sliced — and every step in that preparation shapes what the final stain can show.

The standard is **formalin-fixed, paraffin-embedded tissue**, universally abbreviated FFPE. Formalin — a solution of formaldehyde — cross-links proteins. It forms methylene bridges between nearby amino acids, locking the three-dimensional structure of the tissue in place, preventing enzymatic degradation, and preserving cellular morphology essentially indefinitely at room temperature. This is why FFPE archival blocks from decades-old surgeries can be retrieved and analyzed today. The preservation is excellent.

The cross-linking creates a problem. The same methylene bridges that lock the tissue's architecture also mask the very epitopes — the specific protein surface regions that antibodies bind — that immunohistochemistry needs to detect. The target protein is there, but it is buried under covalent cross-links, structurally inaccessible. Before any antibody can bind, the cross-links must be partially reversed. This is **antigen retrieval**, typically accomplished by heating the section in a buffer solution — the heat breaks the methylene bridges and refolds the protein enough to expose the epitope. Too little heat leaves the epitope still masked; too much denatures the protein further and can reduce or abolish signal. Antigen retrieval is where much of the variability in IHC intensity originates: labs with slightly different retrieval protocols, different buffers, different incubation times, produce different amounts of signal on identical tissue.

After retrieval, the section is deparaffinized (paraffin is hydrophobic, aqueous solutions cannot penetrate it without removing the wax first), rehydrated, and prepared for antibody application. Endogenous peroxidase — present in red blood cells and some tissue cells — is blocked to prevent it from reacting with the detection substrate and producing false positive background signal. Non-specific protein binding is blocked. Then the primary antibody is applied, incubated at the appropriate temperature and time to allow binding, washed away from unbound sites, and the signal is amplified through a secondary detection system — typically a polymer conjugated to horseradish peroxidase — and visualized with DAB substrate, which the enzyme converts to the brown precipitate. A hematoxylin counterstain colors nuclei blue-purple so the tissue architecture is visible alongside the antibody signal.

The physical signal IHC produces is colored enzymatic product at the sites of antibody binding. The spatial resolution is single-cell, and crucially the signal is *in tissue context* — you see not just that a protein is present but which cells express it, whether the staining is in the membrane or the cytoplasm or the nucleus, and how the expressing cells relate to non-expressing cells in the surrounding architecture. This spatial information is what IHC provides that protein measurements on cell homogenates or flow cytometry on dissociated cells cannot.

---

### H&E and IHC: two questions, two signals

**Hematoxylin and eosin** is not an immunohistochemical stain — it uses no antibodies. Hematoxylin is a basic dye that binds to negatively charged molecules, primarily the phosphate backbone of nucleic acids in the nucleus. Eosin is an acidic dye that binds to positively charged molecules, primarily cytoplasmic proteins and extracellular matrix. The result is that nuclei stain blue-purple and cytoplasm stains pink, with variation in shade and texture that reflects the tissue's cell types, architectural organization, and pathological state.

H&E answers an architectural question: what does this tissue look like, and is its organization consistent with malignancy? A pathologist reading H&E sees gland formation, nuclear atypia, mitotic figures, invasion into surrounding stroma, lymphovascular invasion. She can recognize that this is a carcinoma, grade it, and assess the margins. She cannot, from H&E alone, tell whether HER2 is overexpressed, whether PD-L1 is present, or whether the tumor is mismatch-repair deficient. Those are molecular questions about specific proteins, requiring molecular reagents.

IHC answers molecular questions in spatial context. The antibody is the molecular reagent; the tissue context is what distinguishes IHC from a protein blot or a flow cytometry readout. Both H&E and IHC are microscopy of fixed tissue sections. They differ in what they measure: H&E measures bulk dye binding that reflects tissue composition; IHC measures specific antibody binding that reports on a single target protein.

Scale-wise, both operate at the same physical resolution — single cells at a few micrometers — but they sit at a different rung of the information hierarchy. H&E reports morphology; IHC reports one molecular identity within that morphology.

<!-- → [DIAGRAM: tissue preparation and IHC workflow. Top row: five sequential steps in the FFPE preparation — tissue biopsy → formalin fixation (cross-links shown as bridges between proteins) → paraffin embedding (wax block) → microtome sectioning (3–5 µm slice) → glass slide mounted section. Bottom row: six sequential steps in IHC staining — deparaffinize/rehydrate → antigen retrieval (heat reversing cross-links) → block → primary antibody → secondary antibody/HRP polymer → DAB substrate (brown precipitate). Final image: microscopy view showing brown membrane staining on tumor cells. Annotate: where variability enters (retrieval conditions) and what the final signal represents (antibody-bound HER2 protein).] -->

---

### Scoring: where continuous biology meets discrete decisions

The brown stain does not come with a number. Converting the amount of brown into a clinical decision requires a scoring system — and that is where the biology's continuity collides with the decision's need for a discrete answer.

For HER2 in breast cancer, the scoring system is:

- **0**: No staining, or faint/incomplete membrane staining in ≤10% of tumor cells. HER2-negative.
- **1+**: Faint/barely perceptible incomplete membrane staining in >10% of tumor cells. HER2-negative.
- **2+**: Weak to moderate complete membrane staining in >10% of tumor cells, OR strong complete membrane staining in ≤10% of tumor cells. **Equivocal** — requires reflex in situ hybridization.
- **3+**: Strong, complete, circumferential membrane staining in >10% of tumor cells. HER2-positive — treat.

The criteria are as precise as words can make them. But "strong versus moderate," "complete versus incomplete," and "the fraction of cells that qualify" are all judgments applied to a gradient, not measurements on a scale. Where the line falls between 1+ (faint, negative) and 2+ (moderate, equivocal) for a given slide is a call that involves the observer's training, the lab's staining conditions, the specific antibody used, and the specific tumor's morphology. Inter-observer concordance for HER2 scoring is reasonable at the extremes — a 3+ is usually agreed to be 3+ — and deteriorates in the middle where most clinical difficulty lives.

The 2+ category is the system being honest about its own uncertainty. Moderate staining means the antibody signal is real and present, but its relationship to the biological question — does this tumor overexpress HER2 enough to respond to anti-HER2 therapy? — cannot be resolved by the stain alone. The algorithm routes 2+ to **reflex in situ hybridization**: a test that directly counts HER2 gene copies in the nucleus using fluorescent or chromogenic probes. Gene amplification (more HER2 gene copies per cell than the reference gene) resolves the ambiguity in one direction; no amplification resolves it in the other. The 2+ category exists so that borderline staining is confirmed rather than guessed.

PD-L1 scoring adds another layer of complexity. PD-L1 determines eligibility for checkpoint inhibitor therapy — pembrolizumab and related antibodies — in multiple cancer types. But PD-L1 scoring involves not just a single scale but a choice among scoring systems:

- **Tumor proportion score (TPS)**: the percentage of viable tumor cells showing any membrane staining above background.
- **Combined positive score (CPS)**: the ratio of all PD-L1-positive cells (tumor cells, lymphocytes, macrophages) to total viable tumor cells, expressed as a percentage, with the numerator sometimes capped at the denominator.
- **Immune cell score**: focuses on the proportion of tumor-infiltrating immune cells staining positive.

Different drugs were approved with different antibody clones on different platforms scored by different metrics. Pembrolizumab in non-small-cell lung cancer uses the 22C3 clone scored by TPS. Nivolumab uses the 28-8 clone. Atezolizumab in urothelial carcinoma uses the SP142 clone scored by immune cell score. These are not interchangeable. Studies comparing these assays directly have documented that they do not always agree on which tumors are "positive." A tumor that is TPS ≥ 50% by one assay can be TPS < 50% by another, not because the biology is different but because the antibody, the detection platform, and the scoring algorithm are different. The same tissue, different result, different treatment recommendation.

This is not a peripheral caveat to the field of IHC-based companion diagnostics. For PD-L1, it is a central, documented, incompletely resolved feature. Different drugs were developed in parallel using different assay systems, and the assays were not harmonized before approval. The practical consequence is that a clinician whose tumor returned "PD-L1 negative" on one assay may be uncertain whether the result reflects the tumor's biology or the choice of antibody.

---

### The scale ladder from single cells to whole-body

IHC sits at a specific position in the hierarchy of cancer measurements. Below it are molecular assays — Western blots, ELISAs, mass spectrometry, single-cell sequencing — that measure proteins or nucleic acids in cells or homogenates with greater molecular precision but no spatial context. Above it is whole-body imaging — CT, PET — that maps disease across the entire patient at centimeter-scale resolution but cannot see individual cells.

IHC's position is: single-cell resolution, in spatial context, for one protein at a time, in a tissue section a few micrometers thick. The spatial context is the key property. It is what allows the pathologist to say not just "HER2 protein is present in this tumor" but "HER2 protein is expressed in the membrane of these cells in this glandular structure adjacent to this stromal component." The architecture around the positive cells is part of the information.

Flow cytometry also detects proteins with antibodies, at single-cell resolution, for multiple markers simultaneously. What it cannot do is tell you where the positive cell was in the tissue. When a tumor is mechanically and enzymatically dissociated to produce the single-cell suspension that flow cytometry requires, the spatial relationships are destroyed. A cytotoxic T cell that was sitting against a tumor cell membrane is now an identical entry in the flow data to one that was excluded at the stroma. IHC preserves the location; flow cytometry sacrifices it for the ability to measure multiple markers simultaneously and quantify cell populations precisely.

---

### Multiplex spatial profiling: many markers, one section

Single-marker IHC answers one molecular question per slide. A slide stained for HER2 tells you about HER2. A slide stained for PD-L1 tells you about PD-L1. If you want to know both, and where each is relative to the other, you need either multiple sequential stains on serial sections — which introduces alignment problems and tissue consumption — or multiplex methods that read multiple markers in the same section simultaneously.

**Multiplex immunofluorescence** uses fluorescent secondary antibodies rather than enzymatic colorimetric detection, with each protein target labeled in a different fluorescent color. Commercial platforms like Vectra-Polaris image six to eight fluorescent channels simultaneously in a single section, with spectral unmixing algorithms separating the contributions of overlapping fluorophores. More aggressive protocols use iterative cycles — stain with antibodies, image, strip the antibodies off the section, stain again with a different panel — to reach larger numbers of markers at the cost of longer workflows.

**CODEX** uses antibodies conjugated to unique DNA barcodes rather than fluorophores. Each imaging cycle uses a small number of fluorescent reporters that hybridize to specific barcodes; after imaging, the reporters are stripped and a new set applied. The DNA-barcode scaffold separates the number of markers (which can be 40–50) from the number of fluorescent channels (which is physically limited), allowing very high marker counts from the same section.

**Imaging mass cytometry** and **multiplexed ion beam imaging** use metal-tagged antibodies instead of fluorescent labels. A laser or ion beam ablates tiny spots from the section; the ablated material is analyzed by mass spectrometry, which measures the metal content of each spot and maps it to a spatial position. Because mass spectrometry resolves distinct masses precisely, there is no spectral overlap — 40+ metals can be used simultaneously without crosstalk, at spatial resolution approaching single-cell.

These methods produce rich, multi-dimensional maps of the tumor microenvironment: which cell types are present, what they express, and how they are spatially organized relative to each other. The kind of question they enable — are cytotoxic T cells in direct contact with tumor cells, or physically excluded to the stromal compartment? — cannot be answered by any single-marker approach, or by methods that require tissue dissociation.

The gap between research capability and clinical deployment is wide. Multiplexed methods are not standardized across laboratories. Antibody panels, antigen retrieval conditions, image analysis algorithms, and cell-type classification schemes vary between groups. Turning a 40-marker spatial map into a reproducible, validated companion-diagnostic number that drives a treatment decision has not been accomplished for any indication. The methods are generating important biological insights about tumor microenvironment organization that will eventually shape treatment; they are not currently informing clinical decisions directly.

<!-- → [CHART: comparison of spatial profiling methods. Columns: method (single-marker IHC, mIF, CODEX, IMC/MIBI), number of simultaneous markers (1, 6–8, 40–50, 40+), spatial resolution (single cell for all), throughput (routine clinical to research-grade), standardization (clinical standard to not standardized), current clinical role (companion diagnostic standard to research tool). Each row annotated with one representative assay or platform.] -->

---

### What the score is and is not

The opening case's pathologist correctly scores the slide as 2+ equivocal and routes it to reflex ISH. The ISH comes back negative for gene amplification. The final report: HER2-negative. The patient does not receive trastuzumab.

This was the right sequence. The 2+ IHC was honest about its uncertainty; the ISH resolved it. The error that did not happen — and the one this chapter is trying to prevent — would have been to treat 2+ as positive because there was visible brown staining. Any visible brown on any membrane would mean "HER2 is here, treat with trastuzumab." That reasoning collapses the continuous stain into a binary, ignores the scoring criteria, and over-treats patients whose tumors will not respond.

The score is a thresholded interpretation of a continuous signal. The threshold is where biology becomes a decision. Between the biology and the threshold sits measurement variability — differences in antigen retrieval, antibody concentration, incubation time, observer judgment, and assay platform. Some of that variability is controlled by guidelines and quality assurance programs. Some of it is irreducible. The HER2 2+ equivocal bin is the honest acknowledgment of where the measurement variability is large enough that the test cannot decide alone, and the algorithm sends borderline cases to a more definitive measurement.

PD-L1 is the harder case because there is no single confirmatory test — different approved drugs came with different approved assays, and the assays are not always concordant. The clinical reality is that a pathologist using the 22C3 clone with TPS scoring for a pembrolizumab decision is not measuring the same thing as a pathologist using SP142 for an atezolizumab decision, even though both are called "PD-L1 testing." The biology being interrogated — does this tumor express PD-L1? — is the same; the measurements are not. This is a field with a documented assay concordance problem that has not been resolved by technical improvements, because the problem is structural: different drugs were developed with different companion diagnostics that were never harmonized.

A trainee who understands this is equipped for clinical practice. A companion-diagnostic IHC score is not a blood chemistry result with well-established reference ranges and small analytical imprecision. It is a scored interpretation of an immunochemical signal, with assay-specific and observer-specific variability, that has been validated to predict treatment response in specific drug-tumor combinations at specific thresholds. The validation is what makes it actionable. The variability is what makes the algorithm's equivocal bin and its reflex testing requirements necessary.

---

## Exercises

**Warm-up**

1. *(Recall — difficulty: low)* Explain why formalin fixation both preserves tissue morphology and necessitates an antigen retrieval step before IHC. What chemical event does formalin fixation create, and what does antigen retrieval physically reverse? *What this tests: the FFPE preparation steps and their mechanistic relationship.*

2. *(Recall — difficulty: low)* State the HER2 IHC scoring criteria for each bin (0, 1+, 2+, 3+) in terms of staining intensity, membrane completeness, and cell fraction. For each bin, state the clinical action it drives — and explain why the 2+ bin drives a different action than either 0/1+ or 3+. *What this tests: the scoring system before applying it to case-based scenarios.*

3. *(Recall — difficulty: low)* Name two approved PD-L1 antibody clones used in companion diagnostics for checkpoint inhibitor therapy, the scoring metric associated with each (TPS, CPS, or immune cell score), and one cancer type where each is used. *What this tests: the PD-L1 assay diversity before the concordance problem is analyzed.*

**Application**

4. *(Apply — difficulty: medium)* A lung tumor is scored PD-L1 TPS = 47% using the 22C3 antibody. The clinical threshold for first-line single-agent pembrolizumab in this indication is TPS ≥ 50%. Is the patient eligible by that threshold? Then name two specific sources of measurement variability — one from the laboratory preparation process and one from observer scoring — that could each independently move a true 47% result above or below the 50% threshold, and explain what clinical consequence each directional error would cause. *What this tests: threshold reasoning and the clinical consequences of variability near a decision boundary.*

5. *(Apply — difficulty: medium)* A HER2 IHC returns 2+ on a biopsy. Walk through the complete decision algorithm step by step: what test is performed next, what physical property of the tumor it measures, what result in each direction means for HER2 status, and what treatment decision each result drives. Then state one situation where a 2+ with negative reflex ISH might still raise concern about whether the final "HER2-negative" call accurately represents the whole tumor. *What this tests: the complete 2+ workflow with the reflex ISH, and the sampling-limitation problem.*

6. *(Apply — difficulty: medium)* A research group runs multiplex immunofluorescence on a cohort of non-small-cell lung cancer samples, staining simultaneously for PD-L1, CD8 (cytotoxic T cells), CD68 (macrophages), and cytokeratin (tumor cells). They find that patients with CD8-positive T cells in direct contact with cytokeratin-positive tumor cells have better responses to PD-1 checkpoint blockade than patients with equivalent PD-L1 TPS but T cells excluded to the stromal margin. Explain what spatial information this analysis captures that single-marker PD-L1 IHC cannot, and state one reason why this finding, however biologically compelling, cannot currently replace PD-L1 TPS as a clinical companion diagnostic. *What this tests: the spatial capability of multiplex profiling and the gap between research findings and clinical companion-diagnostic validation.*

**Synthesis**

7. *(Synthesize — difficulty: high)* Compare the HER2 IHC scoring system and the PD-L1 TPS scoring system as examples of continuous biology forced into clinical decision thresholds. For each: (a) describe what is being measured and how it is converted to a score; (b) identify where in the scoring process the greatest measurement variability arises; (c) state whether the algorithm handles that variability with a built-in resolution pathway (as HER2 2+ → reflex ISH does) or leaves it unresolved; and (d) evaluate whether digital pathology and automated scoring would reduce the variability that matters most. Conclude with a general statement about what it would take for an IHC companion diagnostic score to be considered a precise measurement rather than a thresholded interpretation. *What this tests: comparative analysis of two scoring systems with explicit variability attribution and an evaluation of the path toward precision.*

8. *(Synthesize — difficulty: high)* A hospital pathology department is considering adopting a multiplex spatial profiling platform to routinely characterize the tumor immune microenvironment alongside standard HER2 and PD-L1 IHC in all solid tumor biopsies. Evaluate this proposal: (a) what biological information would the multiplex platform add to current clinical assessment; (b) what specific clinical decision could it plausibly improve, and what evidence would be required to validate it as a companion diagnostic; (c) what standardization and reproducibility requirements must be met before the multiplex result could be used to change a treatment decision; and (d) what are the realistic timelines and barriers to clinical implementation given current regulatory and methodological constraints. *What this tests: translation of multiplex profiling capability into a clinical deployment decision, with explicit evidence requirements and barrier analysis.*

**Challenge**

9. *(Challenge — difficulty: high)* The PD-L1 companion diagnostic problem — four approved assays using different antibodies, different platforms, and different scoring metrics that do not always agree — has persisted despite documented clinical consequences and significant academic effort to harmonize them. Evaluate why the problem has not been solved: (a) identify the structural, regulatory, and economic factors that created it (different drugs developed by different companies with different companion diagnostics); (b) assess whether technical harmonization — using a single antibody and scoring method for all PD-L1 indications — is biologically valid, given that different scoring metrics (TPS vs. CPS) may actually be measuring different relevant biology; (c) evaluate whether the problem could be dissolved by replacing PD-L1 IHC with a different predictive biomarker (tumor mutational burden, gene expression profiling, microsatellite instability) that is more reproducible; and (d) state your own assessment of the most promising path forward and what evidence would validate it. Be explicit about what is established versus contested, and identify the single most important question whose answer would most change clinical practice for checkpoint inhibitor patient selection. *What this tests: structural analysis of a persistent clinical problem, mechanistic reasoning about whether harmonization is achievable or whether the different assays are measuring genuinely different things, and evaluation of alternative biomarker strategies.*
