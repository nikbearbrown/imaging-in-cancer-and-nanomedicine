# supplemental/

Optional ala carte chapters professors can swap in, reorder, or add
alongside the spine chapters.

## What this directory is for

The official AI+1 TOC is the canonical spine. Most domain-specific adoptions
will need 2–3 supplemental chapters that professors can incorporate based on
their course context, student background, or disciplinary emphasis.

Each supplemental chapter is:
- A standalone `.md` file
- Prefixed `supp-[slug].md`
- Self-contained: readable without the spine chapters, though it references them
- Annotated with an adoption note explaining where it fits in a course

See `catalog.md` for a one-paragraph description of each supplemental chapter
with course placement guidance.

## File format

Markdown. Filename: `supp-[slug].md`

Each file should begin with an adoption note block:

```
<!--
    ADOPTION NOTE
    Fits: [course context — e.g., "weeks 3–5 of a professional development course"]
    Pairs with or replaces: [spine chapter reference]
    What the instructor needs to know: [one sentence]
-->
```

## How it connects to Medhavy

Supplemental chapters can be imported into Medhavy as additional source
documents. They participate in the same Ask AI, Quiz Me, and Glimmer modes
as spine chapters when activated by the instructor.

## Authored by

Instructor-authored or AI-assisted. Each supplemental chapter should be
reviewed against the spine for conceptual consistency before distribution.
