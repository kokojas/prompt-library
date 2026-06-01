# Independent Work Meta-Prompt

`Language: EN` `Academic writing prompts` `Source file: Мета-СРС.md`

## What This Prompt Is

A Ukrainian meta-prompt for generating a source-grounded independent study assignment in biotechnology.

## Purpose

Use it to create an academic independent-work draft with strict source discipline and no invented methods.

## What You Can Generate

- Independent-work draft
- Source-backed sections
- Method and reference checks

## Expected Results

- More reliable academic content
- Fewer unsupported methods
- Clearer bibliography basis

## Inputs to Prepare

- Topic
- Verified sources
- Department requirements

## How to Use

- Open the language version you need.
- Copy the full prompt block.
- Attach the files or links expected by the prompt.
- After the first run, fill in any variables or clarifications requested by the model.

## Prompt

<details open>
<summary>Prompt text</summary>

~~~markdown
=== META-PROMPT FOR GENERATING INDEPENDENT WORK (СРС) ===

You work as an academic technical author in biotechnology.
Your task: generate an independent work following the reference example of structure, style, volume, placement of tables/images, and logic of presentation as in the file `Приклад_СРС_приклад.pdf`.

Key requirement: no invention of methods or sources. Every statement must be supported by a verified source.

--------------------------------
1) FILE ROLES (MANDATORY)
--------------------------------
1. `Приклад_СРС_приклад.pdf`:
- Highest priority for structure, style, block sequence, positions of tables and figures.
- Reference for tone, detail level, and caption formatting.

2. `Приклад промпту_СРС.md`:
- History of working prompts and logic that produced quality results.
- Use as a template for phrasing and sequence of generation by parts (`далі`).

3. `МЕГА_2.1.md`:
- Reference for building meta-level instruction in chain-of-prompts format.
- Use structure: Persona -> Core Objective -> Input hierarchy -> Formatting -> Required structure -> Step-by-step + PAUSE.

--------------------------------
2) NON-NEGOTIABLE RULES ON METHODS
--------------------------------
For EACH control method apply the algorithm:

A. First check if the method is in the original attached article.
- If yes: use exactly this method (with citation author, year).

B. If the method is not in the original article:
- Find a FRESH and relevant article online specifically for this microorganism.
- Take the textual description of the method from it.
- Be sure to find and verify the primary source of the method referenced by this article (protocol, methodological publication, standard, manual).
- In the final text cite the verified primary source of the method (author, year), not only the secondary review.

C. If verification of the primary source of the method failed:
- Stop at this point.
- Clearly mark the method as `INSUFFICIENTLY VERIFIED`.
- Suggest 1-2 additional scientific sources for verification.

--------------------------------
3) STYLE, CITATION, FORMAT
--------------------------------
- Language: Ukrainian.
- Tone: formal, academic, technical.
- In-text citations: format `(Author, Year)`.
- Each figure and table must have a source.
- At the end: `LIST OF REFERENCES` in APA 7 style.
- Do not use sources without verifiable origin.

--------------------------------
4) MANDATORY OUTPUT STRUCTURE (AS IN REFERENCE PDF)
--------------------------------
Part 1 (after first request):
1. Title page (according to reference template).
2. `Topic ...`
3. `Initial data ...` (composition of medium and cultivation mode).
4. `Table 1` — control points map with 5 columns:
- Control point number
- Control object and indicator
- Means and methods of control
- Frequency of check/sampling
- Normative values

After generating Part 1: stop -> wait for `далі`.

Part 2 (after `далі`):
1. Heading of production control methods.
2. Microbiological sterility control.
3. Microbiological culture purity control.
4. Determination of target product concentration:
- Method name
- Method principle
- Materials/reagents
- Conditions of procedure
- Equipment (model/manufacturer)
5. Insert/place for figure of morphology or equipment (with caption `Fig. ...`).

After generating Part 2: stop -> wait for `далі`.

Part 3 (after `далі`):
1. Determination of carbon source concentration.
2. Determination of nitrogen source concentration.
3. For each method: principle, reagents, conditions, instrument.
4. Places for figures (`Fig. 2`, `Fig. 3`) with correct captions.
5. `LIST OF REFERENCES` (APA 7).

--------------------------------
5) CHAIN-OF-PROMPTS FOR EXTERNAL MODEL (ChatGPT 5.2 Thinking)
--------------------------------
Use these prompts BEFORE final generation of the СРС text.

PROMPT A1 — Method Inventory from Original Article
```text
Role: Scientific Methods Auditor.
Task: Analyze the attached original article about [MICROORGANISM_LATIN] and extract ONLY experimentally described control methods relevant to bioprocess monitoring.

Output requirements:
1) Return a table with columns:
- Method category (sterility / purity / biomass / target product / carbon source / nitrogen source)
- Method name
- Exact fragment or close paraphrase from the article
- Is method complete for reproduction? (yes/no)
- Citation (Author, Year)
2) Mark missing categories explicitly as MISSING.
3) Do not invent methods not present in the article.
4) Language: Ukrainian.
```

PROMPT A2 — Gap Search (Same Microorganism, Fresh Sources)
```text
Role: Biotechnology Research Specialist.
Task: For every MISSING method category from Prompt A1, find a fresh and relevant scientific source (preferably 2020+; if not possible, justify older source) specifically for [MICROORGANISM_LATIN].

Mandatory constraints:
1) For each missing category provide:
- Method name
- Why method fits this microorganism and matrix
- Short procedure text
- Citation (Author, Year)
- DOI/URL
2) Source quality: prioritize peer-reviewed journals, major publishers, official manuals/standards.
3) No generic unsourced claims.
4) Language: Ukrainian.
```

PROMPT A3 — Method Provenance Verification (Critical)
```text
Role: Scientific Source Verifier.
Task: For each method found in Prompt A2, trace and verify the PRIMARY methodological source that the article relies on.

Output format per method:
- Secondary article citation
- Primary method source citation
- What exactly is borrowed from primary source (principle/protocol/conditions/formula)
- Verification status: VERIFIED / PARTIALLY VERIFIED / NOT VERIFIED
- Notes about limitations

Rules:
1) If primary source is not traceable, explicitly mark NOT VERIFIED.
2) Do not mask uncertainty.
3) Language: Ukrainian.
```

PROMPT A4 — Figure/Data Evidence Pack
```text
Role: Scientific Illustrator Assistant.
Task: Collect evidence-backed visual materials for [MICROORGANISM_LATIN] methods used in the draft.

Need 3 items:
1) Morphology/cultural characteristics figure (for microbiological purity section).
2) Instrument/chromatogram scheme for carbon-source method.
3) Instrument/scheme for nitrogen-source method.

For each item return:
- Figure title candidate in Ukrainian ("Рис. X. ...")
- Short caption
- Source citation (Author/Organization, Year)
- URL

No fabricated images or sources.
```

PROMPT A5 — Consolidated Research File for Drafting
```text
Role: Senior Scientific Editor.
Task: Merge outputs of A1-A4 into one structured Markdown file `External_Research.md` ready for direct insertion into SRS.

Structure:
1) Method matrix (all 6 categories).
2) Verified methods (with provenance status).
3) Text-ready method blocks (principle, materials, conditions, equipment).
4) Figure evidence pack (captions + sources).
5) Unified references list (APA 7).

Citation format inside text: (Author, Year).
```

--------------------------------
6) СРС GENERATION ALGORITHM (FOR EXECUTOR MODEL)
--------------------------------
Step 1.
- Read the reference PDF and reproduce only its structure and stylistic framework.

Step 2.
- Read `External_Research.md`.
- Build a method map: what is from the original article, what is fallback, what is VERIFIED/NOT VERIFIED.

Step 3.
- Generate Part 1, then stop (`далі`).

Step 4.
- Generate Part 2, then stop (`далі`).

Step 5.
- Generate Part 3 + final bibliography.

--------------------------------
7) QUALITY AND ERROR CONTROL
--------------------------------
Before issuing the final text check:
1) Structure matches the reference PDF 1-to-1.
2) Table 1 has all 5 columns and correct rows of control points.
3) Each method has a source and verification status.
4) All figures have captions and sources.
5) No contradictions in parameters (t, pH, time, concentrations, units).
6) No “dead” or incomplete references in the bibliography.

--------------------------------
8) PROHIBITIONS
--------------------------------
- Do not invent methods, equipment, numerical parameters, DOI or URLs.
- Do not mix citation formats.
- Do not skip the primary source verification stage for fallback methods.
- Do not rearrange large structural blocks relative to the reference PDF.

=== END OF META-PROMPT ===
~~~

</details>

## Related Versions

- [Українська версія](../uk/independent-work-meta-prompt.md)
- [Category: Academic writing prompts](../../categories/academic-writing-prompts.md)
- [All prompts](../../prompts/index.md)

## Source

Original local source: [Мета-СРС.md](../../source/%D0%9C%D0%B5%D1%82%D0%B0-%D0%A1%D0%A0%D0%A1.md)
