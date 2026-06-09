# Histology, IHC, and Multiplex Spatial Profiling

## Learning Objectives

After working through this chapter you should be able to:

- **Describe** how a tissue sample becomes an FFPE slide and why every step (fixation, embedding, sectioning, antigen retrieval) shapes what the final stain can show.
- **Explain** the physical signal and biological question of H&E histology versus immunohistochemistry (IHC), and locate both on the scale ladder between flow cytometry and whole-body imaging.
- **Score** a HER2 IHC result on the 0/1+/2+/3+ scale and a PD-L1 result by tumor proportion score (TPS%), and state what threshold drives a treatment decision.
- **Compare** single-marker IHC with multiplex spatial profiling (mIF, CODEX, MIBI, imaging mass cytometry) by marker count, spatial information, and standardization.
- **Critique** the assumption that a companion-diagnostic IHC score is a precise, reproducible measurement of the underlying biology.

## Opening Case

A pathologist receives a breast cancer biopsy. The treatment decision turns on one protein: HER2, a growth-factor receptor that, when overexpressed, makes the tumor eligible for trastuzumab (Herceptin) and related HER2-targeted drugs. She runs immunohistochemistry — an antibody stain that deposits a brown precipitate wherever HER2 protein sits in the tissue — and looks down the microscope.

The membranes of the tumor cells show a brown rim. But how brown, and how complete? The HER2 scoring scale is **0, 1+, 2+, 3+**, and the entire clinical decision hinges on which bin this slide falls into. A crisp, complete, intense membrane stain in most cells is 3+ — HER2-positive, treat. Faint, incomplete staining is 0 or 1+ — negative, don't. This slide sits in between: moderate, somewhat patchy staining. That is **2+ — equivocal**, the category that means *the IHC cannot decide*, and the case must go to a separate test (in situ hybridization for HER2 gene amplification) to break the tie.

Here is the failure mode in plain view. The brown precipitate is a real, physical signal — antibody bound to protein, enzyme depositing dye. But turning "this much brown, this complete, in this fraction of cells" into "3+ versus 2+" is a human judgment on a continuous variable forced into discrete bins. Two pathologists can look at the same equivocal slide and score it differently. A patient's access to a targeted drug can ride on which side of a threshold one observer places a continuous stain. The slide measured HER2 protein. The *score* is an interpretation — and the interpretation, not the protein, is what determines the treatment.

## Core Concepts

### From tissue to slide

**Histology** is the study of tissue architecture under the microscope. Before any staining, the tissue must be preserved and sliced. The standard route is **formalin-fixed, paraffin-embedded (FFPE)** tissue:

1. **Fixation** in formalin cross-links proteins, freezing the tissue's structure and preventing decay — but those same cross-links *mask* the very antigens you later want to detect.
2. **Embedding** in paraffin wax supports the tissue so it can be cut.
3. **Sectioning** on a microtome produces slices 3–5 µm thick — roughly the thickness of one cell layer — mounted on glass slides.

The baseline stain is **hematoxylin and eosin (H&E)**: hematoxylin turns nuclei blue-purple, eosin turns cytoplasm and extracellular protein pink. H&E shows *architecture* — gland shapes, nuclear atypia, invasion — but says nothing about specific molecules. Its physical signal is bulk dye binding to nucleic acid and protein; its biological question is *what does this tissue look like, and is it malignant?*

### Immunohistochemistry: putting a molecule on the map

**Immunohistochemistry (IHC)** detects a *specific* protein in tissue using antibodies. The workflow:

1. **Deparaffinize** and rehydrate the section.
2. **Antigen retrieval** (heat or enzyme) reverses the formalin cross-links so the target epitope is accessible again — a step that, if under- or over-done, changes how much signal you get.
3. **Block** endogenous peroxidase and non-specific binding.
4. **Primary antibody** binds the target protein.
5. **Secondary antibody / detection system** (typically HRP-conjugated polymer) amplifies the signal.
6. **Substrate (DAB)** — the enzyme converts it to a **brown precipitate** wherever the antibody is bound.
7. **Counterstain** with hematoxylin to show nuclei; coverslip; image by light microscopy.

Physical signal: a colored enzymatic precipitate marking antibody-bound protein. Spatial resolution: single-cell, and crucially **in tissue context** — you see not just that HER2 is present, but *which* cells, in *what architecture*. That is the property the previous chapter's flow cytometry threw away when it dissociated the tumor.

<!-- → [DIAGRAM: scale ladder — flow cytometry (cells in suspension, no location) → IHC/H&E (single cells in tissue context) → multiplex spatial (many markers, mapped) → whole-body PET (organism, coarse); annotate signal and spatial scale at each rung] -->

### Scoring: continuous biology, discrete decisions

IHC outputs range from crude to quantitative:

- **Qualitative:** positive vs. negative.
- **Semi-quantitative:** the **0 / 1+ / 2+ / 3+** intensity scale, used for HER2.
- **Quantitative composites:** the **H-score** (intensity × percent positive cells, 0–300); the **Allred score** for breast hormone receptors (ER/PR); and for PD-L1, the **tumor proportion score (TPS%)** — the percentage of tumor cells with membrane staining — and the **combined positive score (CPS)** that also counts immune cells.

These scores are the hinge between measurement and decision. **HER2 3+** (or 2+ confirmed amplified by in situ hybridization) means treat with trastuzumab [verify]. **PD-L1 TPS ≥ 50%** (assayed, for the pembrolizumab indication, with the **22C3** antibody clone) has been used as a threshold for first-line checkpoint inhibitor eligibility in some lung cancers [verify]. The biology — protein abundance — is continuous. The decision is a bin. The threshold is where a number becomes a treatment.

### The reproducibility problem

Here the chapter's honesty obligation kicks in. These scores are *not* fully objective measurements.

- The **HER2 2+ "equivocal"** bin exists precisely because IHC alone cannot reliably resolve borderline cases, which is why a confirmatory in situ hybridization test is built into the algorithm [verify].
- **PD-L1 assays are genuinely discordant.** Different drugs were approved with different antibody clones (22C3, 28-8, SP142, SP263) on different platforms, scored by different metrics (TPS, CPS, IC%). Studies comparing these assays have found they do *not* always agree on which tumors are "positive," and inter-observer agreement on PD-L1 scoring is imperfect [contested — see pantry flag: PD-L1 assay and reader discordance is well documented]. A tumor can be "positive" by one approved assay and "negative" by another.

So the same tissue can yield different actionable calls depending on which antibody, platform, and reader produced the score. That is not a peripheral caveat; for PD-L1 it is a defining, unresolved feature of the field.

### Multiplex spatial profiling

Single-marker IHC answers one molecular question per slide. **Multiplex** methods answer dozens *at once, in situ*, mapping the tumor microenvironment:

- **Multiplex immunofluorescence (mIF)** uses several fluorophores (often with tyramide signal amplification and antibody stripping between rounds) to read 6–8+ proteins in one section.
- **CODEX** uses iterative cycles of DNA-barcoded antibodies to reach tens of markers.
- **Imaging mass cytometry (IMC) and MIBI** use metal-tagged antibodies read by mass spectrometry, pushing toward 40+ markers with no spectral overlap.
- **Vectra-Polaris** provides multispectral imaging and analysis.

These let you ask *spatial* questions single IHC cannot: are cytotoxic T cells touching tumor cells, or excluded to the stromal margin? Is PD-L1 on the tumor or on neighboring macrophages? The payoff is a marker-rich map of *who is next to whom*. The cost — and the current frontier of contention — is **standardization**: multiplex-IF workflows are not yet harmonized across labs, and turning a beautiful multiplexed image into a reproducible, decision-grade number remains an open methodological problem [contested — see pantry flag].

<!-- → [CHART: IHC scoring ladder — HER2 0/1+/2+/3+ membrane patterns and PD-L1 TPS% thresholds — beside a multiplex spatial map showing tumor/immune cell neighborhoods] -->

## Worked Example

**Situation.** The opening-case breast biopsy: moderate, somewhat patchy HER2 membrane staining. Is this patient HER2-positive and eligible for trastuzumab?

**Reasoning — first attempt (the dead end).** "There's clearly brown membrane stain, so HER2 is overexpressed — call it positive and treat." This treats *any* visible signal as a positive result. It fails because HER2 IHC is scored by **intensity and completeness of membrane staining in a fraction of tumor cells**, not by mere presence of brown. Faint or incomplete staining (0, 1+) is *not* eligibility; strong, complete, circumferential staining in >10% of cells (3+) is. Calling everything brown "positive" would over-treat patients whose tumors won't respond to a HER2-targeted drug — confusing a continuous signal with a binary truth.

**Reasoning — corrected.** She scores against the defined criteria. The staining is moderate and incomplete in many cells — neither the faint/absent pattern of 0–1+ nor the strong, complete rim of 3+. This is **2+ (equivocal)**. By the diagnostic algorithm, 2+ does *not* settle the question; it triggers a **reflex in situ hybridization (ISH)** test for HER2 gene amplification [verify]. The ISH counts HER2 gene copies directly, bypassing the subjective intensity judgment.

**Resolution.** The reflex ISH shows no HER2 gene amplification. The final call is **HER2-negative**: the patient is not a candidate for trastuzumab, and treating on the basis of the ambiguous 2+ stain alone would have been an error. The IHC didn't fail — it correctly flagged its own uncertainty by landing in the equivocal bin, and the algorithm sent the hard cases to a more definitive test.

**The lesson.** A companion-diagnostic IHC score is a *thresholded interpretation* of a continuous stain. The equivocal bin is not a defect; it is the system admitting where antibody staining alone cannot decide, and routing those cases to confirmation.

**The limit.** Even the ISH-confirmed call captures HER2 status in *this* sampled fragment at *this* moment. Tumors are heterogeneous: a different block might score differently, and HER2 status can shift under treatment. A single slide is a spatial and temporal sample, not the whole tumor.

## Common Misconceptions

**"If the IHC shows brown stain, the marker is positive."** Plausible — brown means antibody bound. But scoring depends on intensity, pattern (membrane vs. cytoplasmic), completeness, and the fraction of cells, against a defined threshold. Faint staining is "negative" by criteria even though brown is visible. This is exactly the trap the opening case sets: any-brown-is-positive over-treats.

**"A HER2 or PD-L1 score is an objective number."** It is a human (or algorithm) reading a continuous signal forced into bins, with real inter-observer variability — and for PD-L1, real disagreement *between approved assays*. The same tumor can be positive by one clone and negative by another. Treating the score as a precise constant ignores the documented discordance [contested — see pantry flag].

**"Multiplex imaging with 40 markers makes single-marker IHC obsolete."** Multiplex methods add spatial and combinatorial richness, but they are far less standardized, harder to reproduce across labs, and not yet validated as routine companion diagnostics. For a HER2 or ER decision, a well-validated single-marker IHC plus reflex testing remains the clinical standard; multiplex is, for now, mostly a research tool.

**"Flow cytometry and IHC measure the same thing, just differently."** Both detect proteins with antibodies, but flow cytometry reports *how many* cells in a suspension are positive, with no location, while IHC reports *which* cells are positive *and where they sit* in the tissue. The spatial context — tumor margin, immune infiltration pattern — is the entire reason IHC exists and is exactly what dissociation for flow cytometry destroys.

## Exercises

1. **(Comprehend)** Explain why formalin fixation both preserves tissue and necessitates an antigen-retrieval step before IHC. What does retrieval physically reverse?

2. **(Apply)** A lung tumor is scored PD-L1 TPS = 45% with the 22C3 antibody. The clinical threshold for first-line single-agent pembrolizumab in this scenario is TPS ≥ 50% [verify]. Is the patient eligible by that threshold? Then name two sources of uncertainty that could move a 45% across the 50% line.

3. **(Apply+)** A HER2 IHC reads 2+. Walk through the decision algorithm step by step, naming the confirmatory test, what it physically measures, and why the workflow does not simply treat all 2+ cases as positive. State the risk of treating versus not treating based on the 2+ stain alone.

4. **(Produce)** Create a one-page "scoring reference card" for a trainee pathologist covering HER2 (0/1+/2+/3+ membrane criteria) and PD-L1 (TPS vs. CPS, the relevant threshold, the antibody clone). For each marker, write one sentence stating the treatment decision the score drives. (Producing the card forces you to tie each bin to a consequence.)

5. **(Analyze)** Two labs report opposite PD-L1 results on the same tumor using two different approved assays. List the specific differences between assays that could cause this, and argue what a clinician should do when faced with discordant PD-L1 calls.

## What Would Change My Mind

The central claim is that an IHC companion-diagnostic score is a *thresholded interpretation* of a continuous signal — subjective enough that the same tissue can yield different actionable calls depending on antibody, platform, and reader — rather than a precise measurement of the underlying biology. What would revise that? A large, multi-lab study showing that a fully automated, digital-pathology scoring algorithm reads HER2 and PD-L1 with near-perfect agreement across labs *and* that those harmonized scores predict treatment response better than current human scoring — collapsing the inter-observer and inter-assay variability I'm emphasizing — would weaken the framing. If digital quantification turned these scores into reproducible, biology-tracking numbers, the "interpretation, not measurement" claim would lose force for those markers. The documented PD-L1 assay discordance and HER2 2+ inter-observer disagreement are what currently keep the framing honest [contested — see pantry flag]; convincing evidence that automation has closed those gaps would move me.

## Still Puzzling

- **Will digital pathology and AI scoring resolve the subjectivity, or relocate it?** Automated HER2/PD-L1 quantification is advancing fast. Does it remove reader variability, or just move the arbitrary choices into the algorithm's training and thresholds?
- **How should clinicians handle PD-L1 assay discordance?** When approved assays disagree, there is no clean rule for which to trust. Is harmonization across clones achievable, or are these fundamentally measuring slightly different things?
- **What is the right unit of "positivity" for a heterogeneous tumor?** A single 3–5 µm section samples a sliver of a spatially varied tumor. How many sections, from how many blocks, make a "tumor-level" HER2 or PD-L1 status trustworthy?
- **Can multiplex spatial profiling become decision-grade?** The maps are gorgeous and biologically rich, but standardization lags. What would it take to turn a CODEX or MIBI neighborhood analysis into a reproducible companion diagnostic?

## References

- NCI, "Research Areas: Cancer Diagnosis" (biomarkers, imaging, single-cell and spatial data). https://www.cancer.gov/research/areas/diagnosis
- NCI, "Tests and Procedures Used to Diagnose Cancer" (biopsy, IHC, tumor markers). https://www.cancer.gov/about-cancer/diagnosis-staging/diagnosis
- NCI Core Resources Guide (optical imaging, microscopy cores). https://ccr.cancer.gov/sites/default/files/nci_core_resources_guide_2020.pdf
- Source chapter: "Protein Analysis: Western Blot, ELISA, and Immunohistochemistry" (cba-77), Humanitarians AI cancer series.
- HER2 IHC scoring (0/1+/2+/3+) and reflex ISH algorithm; trastuzumab (Herceptin) companion diagnostic [verify against current ASCO/CAP HER2 guideline before publication].
- PD-L1 IHC assays and clones (22C3, 28-8, SP142, SP263); TPS and CPS scoring; pembrolizumab indication thresholds [verify and update against current labeling].

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
