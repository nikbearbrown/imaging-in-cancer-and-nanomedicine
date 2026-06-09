# Chapter 7 — Flow Cytometry and FACS

A postdoc is profiling tumor-infiltrating lymphocytes from a melanoma biopsy. She wants to know what fraction of the T cells are exhausted — expressing the inhibitory receptor PD-1, a question that matters because exhausted T cells may be reawakened by checkpoint immunotherapy. She digests the tumor into a single-cell suspension, stains with anti-CD3 on one fluorophore and anti-PD-1 on another, and runs it on the flow cytometer.

The software reports that 38% of cells are PD-1-positive. She is about to write down "38% of T cells are exhausted."

Did she exclude dead cells, which bind antibody non-specifically and inflate the positive fraction? Did she exclude doublets — two cells stuck together and counted as one — which scramble the relationship between CD3 and PD-1? Where, exactly, did she draw the line between PD-1-negative and PD-1-positive, and is that line an artifact of fluorescence from the CD3 channel spilling into the PD-1 detector?

The cytometer measured photons and voltages faithfully, for tens of thousands of cells. But "38% exhausted T cells" is not a measurement. It is an interpretation layered on gating and compensation decisions — and any one of them, done wrong, moves the number.

---

## What the machine actually measures

**Flow cytometry** analyzes individual cells in suspension, one at a time, at high speed. The machine has four functional parts.

**Fluidics.** A narrow nozzle uses hydrodynamic focusing — a fast outer sheath fluid squeezing the sample stream — to line cells up single file so they cross the laser one at a time, thousands per second. Without this, cells would arrive in clumps and the machine would measure overlapping signals.

**Lasers.** One or more fixed-wavelength excitation sources. Common lines are 405, 488, 561, and 633 nm. Modern instruments carry three to six lasers. The laser excites fluorescent molecules on and in the cell, causing them to emit light.

**Optics.** Filters and dichroic mirrors split the emitted light by wavelength and route each wavelength band to its own detector.

**Detectors.** Photomultiplier tubes or avalanche photodiodes convert incoming photons to voltage pulses, recorded as a number for each cell and each channel.

As each cell crosses the beam, the machine reads three kinds of signal. **Forward scatter (FSC)** is light scattered slightly forward in the direction of the beam — a rough proxy for cell size. **Side scatter (SSC)** is light scattered at 90 degrees — a proxy for internal granularity and complexity; a granular neutrophil scatters more sideways than a small lymphocyte. **Fluorescence channels** each read one wavelength band, reporting the emission from a specific fluorophore-tagged antibody or dye bound to the cell. A modern instrument records fifteen to thirty parameters per cell, across hundreds of thousands of cells in minutes.

Flow cytometry sits on the scale ladder at an interesting position. Fluorescence microscopy sees where a protein sits inside one cell but images few cells and is slow. Bulk assays like ELISA report an average signal across millions of cells and say nothing about individual variation. Flow cytometry makes the trade in the middle: it sees individual cells at high throughput, measuring how much signal each carries, with no spatial information about where in the cell the signal came from. The biological question it answers well — what fraction of a population carries marker X, and how do multiple markers co-vary across cells — is one neither microscopy nor bulk assay can answer at scale.

<!-- → [DIAGRAM: flow cytometer schematic — fluidics/hydrodynamic focusing, laser interrogation point, optics splitting emission to detectors, then FSC vs SSC plot feeding into a sequential gating tree] -->

---

## Gating: the decisions that build the number

The standard workflow: prepare a single-cell suspension, stain, wash, acquire, gate, analyze. Gating is the step where measurement becomes interpretation.

**Gating** is the sequential selection of the cells you actually want to analyze. You draw boundaries — gates — on scatter and fluorescence plots, and only events inside the gate proceed to the next step. A gating strategy runs as a tree:

The first gate is drawn on **FSC versus SSC**, selecting intact cells of expected size and complexity and excluding debris. Debris is small, scatter-low, and would dilute your population with uninformative events.

The second gate addresses **doublets** — two cells that stuck together during preparation and passed through the nozzle as one event. Doublets have summed fluorescence signals and summed scatter. Because they carry signal from two cells, a doublet containing one CD3-positive and one CD3-negative cell looks like a weakly positive cell, not a positive and a negative. Doublet exclusion plots FSC-area against FSC-height: singlets have a tight linear relationship between the two; doublets fall off that line because their elongated shape produces a higher area-to-height ratio. This gate is frequently skipped and frequently matters.

The third gate uses a **viability dye**. Dead cells have compromised membranes and bind antibodies non-specifically, regardless of whether they express the target. A dead T cell that does not express PD-1 will nonetheless stain positively with anti-PD-1 if the cell is dead and sticky. Viability dyes like DAPI and 7-AAD enter only cells with permeable membranes and can be used to mark and exclude them. Skip this and dead cells inflate every positive fraction.

The final gates call cells **positive or negative** for the markers of interest. Where you draw the positive threshold determines the percentage. Move the line by a small amount and the percentage moves with it.

---

## Compensation: the correction for spectral overlap

Real fluorophores have broad emission spectra. A fluorophore excited at 488 nm and meant to emit into one detector also emits some light into neighboring detectors. This is **spectral overlap** or spillover, and it means that cells stained only with fluorophore A can appear to have signal in the detector for fluorophore B.

**Compensation** corrects for this. The correction is computed from **single-stain controls** — samples stained with one fluorophore each — that measure exactly how much each fluorophore bleeds into each other detector. The compensation algorithm subtracts the appropriate fraction of each channel's signal from every other channel.

Get compensation wrong in one direction and a population that is truly negative appears positive in the affected channel — a false positive created by the analysis, not the biology. In the opening case, CD3 on one fluorophore bleeds into the PD-1 detector. Without correct compensation, CD3-bright T cells appear PD-1-positive even when they are not.

The **fluorescence-minus-one (FMO) control** solves a related problem. An FMO is a sample stained with the complete panel *except* one fluorophore. The FMO shows you where the negative population actually falls after all the spectral contributions from the rest of the panel are present. Without it, drawing the positive gate is guesswork: you do not know where the background from all the other channels pushes the true-negative population. The FMO tells you honestly where negative ends and where positive should begin.

These controls — single-stains for compensation, FMOs for gating — are not optional refinements for a publication-quality analysis. They are the minimum for knowing that your number means what you think it means.

---

## Multi-color panels and their tradeoffs

Modern flow cytometry panels stack many fluorophores simultaneously. On a 488 nm laser: FITC, PE, PE-Cy7. On a 633 nm laser: APC, Alexa Fluor 647. On a 405 nm laser: Brilliant Violet dyes that dramatically expanded high-parameter immune phenotyping. A well-designed panel can identify T-cell subsets (CD4 helper, CD8 cytotoxic, regulatory T cells defined by CD25 and FoxP3), exhaustion markers (PD-1, TIM-3, LAG-3), cancer stem-cell surface markers (CD44, CD24, CD133), apoptosis (Annexin V combined with a viability dye), and cell cycle status (DNA content by propidium iodide or Ki-67 by intracellular staining).

Panel design is a craft requiring constraint. Every added fluorophore adds spectral overlap and one more compensation correction to get wrong. Bright fluorophores like PE spread heavily into neighboring channels; pairing PE with a dim marker of a rare population is a common mistake that produces false positives in exactly the cells you most care about. The rule: match the brightest fluorophores to the lowest-abundance markers, because the signal-to-noise is worst there. A poorly designed eight-color panel is less trustworthy than a clean four-color one. Parameter count is not rigor; controls are.

---

## FACS sorting and mass cytometry

**Fluorescence-activated cell sorting (FACS)** extends flow cytometry from measuring cells to physically separating them. Cells meeting defined fluorescence criteria are given an electric charge and deflected by electric plates into collection tubes; the rest flow to waste. This lets you isolate a live, specific population for downstream experiments — sequencing, functional assays, injection into an animal. Leonard Herzenberg developed the fluorescence-activated cell sorter at Stanford, establishing the technology that made modern immunology and cancer-cell biology possible.

FACS is slow relative to analytical cytometry, stresses cells, and requires expensive sorters. For bulk separation of a single marker, **magnetic-bead sorting (MACS)** is faster and gentler — cells bound to magnetic beads are held by a magnet while the rest wash through — but it cannot resolve fine, multi-marker populations where you need two or three simultaneous gates.

**Mass cytometry (CyTOF)** replaces fluorophores with metal-isotope-tagged antibodies. Stained cells are vaporized and ionized, and a time-of-flight mass spectrometer counts each metal per cell. Because metal isotopes have discrete masses, there is essentially no spectral overlap. Forty or more parameters can be measured simultaneously with minimal compensation. The tradeoffs are real: acquisition is slower, the cells are destroyed by the ionization process and cannot be recovered, and the reagents are more expensive. CyTOF answers the question "what is the high-dimensional molecular phenotype of each cell?" well; it cannot answer "can you give me those cells alive?" at all.

<!-- → [CHART: flow cytometry vs FACS vs CyTOF — parameters per cell, throughput (cells/sec), cells survive? (sort yes / analyze no / CyTOF no), with the question each best answers] -->

---

## The 38% revisited

Return to the opening case. "38% of T cells are PD-1-positive, therefore 38% are exhausted."

The postdoc rebuilds the analysis as a gating tree. First, FSC versus SSC to keep intact lymphocytes and exclude debris. Second, FSC-area versus FSC-height to exclude doublets. Third, viability dye to exclude dead cells. Fourth, a CD3 gate to restrict the denominator to genuine T cells — so the percentage is *T cells that are PD-1-positive*, not *all events that are PD-1-positive*. She runs single-stain controls and recomputes compensation to remove CD3-channel spillover into the PD-1 detector. She runs an FMO — everything except the PD-1 fluorophore — to see where the true-negative T cells fall and draws the positive gate there.

After dead-cell exclusion, doublet exclusion, proper compensation, and FMO-based gating, the PD-1-positive fraction drops from 38% to 22%. The original 38% was inflated by non-specifically stained dead cells and an over-generous positive gate set without an FMO.

And 22% is still not "22% exhausted." PD-1 alone marks both recently activated T cells — which upregulate PD-1 as part of normal activation — and genuinely exhausted ones. Distinguishing activation from exhaustion requires co-expression of additional inhibitory receptors, typically TIM-3 and LAG-3. PD-1-single-positive cells are a lead; PD-1/TIM-3/LAG-3-triple-positive cells are the subset with the phenotype most consistent with exhaustion.

The lesson runs both directions. A flow cytometry percentage is the product of two decisions: what cells to count (the denominator, set by the gating tree) and where to call positive (the threshold, set by the gate position and validated by the FMO). Neither is read directly from the data; both are constructed. The biology lives in the gating logic, not in the raw number.

And even a correct percentage is a phenotypic description, not a functional one. Whether a PD-1/TIM-3/LAG-3-triple-positive T cell is functionally exhausted — unable to proliferate and kill tumor cells, revivable by checkpoint blockade — cannot be read from its surface markers. That requires a functional assay. The suspension also discarded all spatial information: whether these T cells contact tumor cells, where they sit in the tissue architecture, and whether they are clustered near other immune cells is unknowable from the suspension. The instrument measured what it could measure; the biology it cannot measure requires a different method.

---

## What would change this picture

The central claim is that a flow cytometry result is a constructed number whose value is set by gating and compensation decisions, not read directly off the cells. What would revise this: a rigorous reproducibility study in which many independent analysts given the same raw data files and a fully automated, decision-free gating pipeline converge on statistically indistinguishable population percentages, and in which those percentages match an independent ground truth — single-cell sequencing of the same sample, for example. If gating could be made objectively reproducible and validated against independent measurement, the argument that the number depends on who drew the gate would weaken. Automated clustering and dimensionality reduction methods are advancing toward this, but they introduce their own parameter choices rather than eliminating decisions. The persistence of analyst-to-analyst variability in published immune-monitoring studies keeps the framing alive.

---

## Still open

Whether gating can ever be fully objective is genuinely unsettled. Automated gating algorithms and unsupervised clustering methods remove human gate-drawing but substitute algorithm choices — distance metrics, cluster numbers, dimensionality-reduction parameters — that are their own form of decision. Is objective gating achievable, or just relocated from the analyst to the algorithm?

How many markers are required to pin down a functional cell state is not established for most states. PD-1 marks activation and exhaustion; CD133 marks stem-like and non-stem-like cells depending on context. Whether any panel of surface markers fully resolves the functional state of a cell, or whether functional assays will always be required to complement phenotypic data, is a question with direct consequences for how flow cytometry data is interpreted in clinical and translational studies.

Whether dissociating a tissue into a suspension changes the cells being measured is underappreciated. Enzymatic digestion can preferentially destroy fragile populations, alter surface-marker expression through proteolytic cleavage, and introduce artifacts from the mechanical and thermal stress of processing. The measurement reports the cells that survived the preparation, which may not represent the full population in situ.

---

## LLM Exercises

1. **(Physical signals)** Name the physical signal behind forward scatter, side scatter, and a fluorescence channel. State the biological property each is used as a proxy for and give one example of a cell type that would be distinctive in each measure.

2. **(Spectral overlap)** You stain cells with PE-anti-CD8 and APC-anti-PD-1. In the PD-1/APC channel, CD8-high cells all appear weakly positive even in a sample not stained for PD-1. Name the most likely artifact, name the control that diagnoses it, explain the correction, and describe the result you would expect after correct compensation.

3. **(Gating tree design)** Design a minimal gating strategy to identify exhausted CD8 T cells in a tumor suspension. Present it as an ordered tree with axis variables labeled at each step. State the purpose of each gate, the artifact it excludes, and the single most important control for setting the final positive threshold.

4. **(Regulatory T-cell claim)** A colleague reports that a drug increased the regulatory T-cell fraction from 5% to 9%. Before accepting this doubling, list the gating and control steps that must have been done correctly for the change to be real. For each step, name the artifact that could otherwise produce a spurious increase.

5. **(Technology choice)** Your experiment requires: (a) measuring 25 surface and intracellular markers per cell to characterize tumor-infiltrating immune subsets comprehensively, and (b) recovering the rare double-positive population alive for single-cell RNA sequencing. Can one instrument or one run do both? Identify which technology best serves each requirement, explain why no single run satisfies both simultaneously, and propose the minimum experimental design that accomplishes both goals.

---

## References

- Herzenberg, L. A., et al. (2006). The history and future of the fluorescence activated cell sorter and flow cytometry: a view from Stanford. *Clinical Chemistry*, 48(10), 1819–1827.
- Perfetto, S. P., Chattopadhyay, P. K., & Roederer, M. (2004). Seventeen-colour flow cytometry: unravelling the immune system. *Nature Reviews Immunology*, 4(8), 648–655.
- Maecker, H. T., McCoy, J. P., & Nussenblatt, R. (2012). Standardizing immunophenotyping for the Human Immunology Project. *Nature Reviews Immunology*, 12(3), 191–200.
- Bendall, S. C., et al. (2011). Single-cell mass cytometry of differential immune and drug responses across a human hematopoietic continuum. *Science*, 332(6030), 687–696.
- Gattinoni, L., et al. (2011). A human memory T cell subset with stem cell–like properties. *Nature Medicine*, 17(10), 1290–1297.
- NCI. *Research Areas: Cancer Diagnosis.* https://www.cancer.gov/research/areas/diagnosis
