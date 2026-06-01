# Production Practice Report and Scheme Generator

`Language: EN` `Practice reports` `Source file: Промпти_звіт з виробничої практики.md`

## What This Prompt Is

A Ukrainian chain for generating a production-practice report plus technology and equipment schemes.

## Purpose

Use it to plan and generate a complete practice-report package with source-grounded technical parameters.

## What You Can Generate

- Practice report
- Technology scheme
- Equipment scheme
- Parameter research prompts

## Expected Results

- More complete production workflow
- Better exact-data discipline
- Reusable report-generation chain

## Inputs to Prepare

- Product name
- Manufacturing context
- Available sources and requirements

## How to Use

- Open the language version you need.
- Copy the full prompt block.
- Attach the files or links expected by the prompt.
- After the first run, fill in any variables or clarifications requested by the model.

## Prompt

<details open>
<summary>Prompt text</summary>

~~~markdown
---
Report generator + technological scheme + apparatus scheme for production practice (4th year, 8th semester, NUHT).
Version: 0.0.1.

Context: there are two AI models: Gemini 3 Pro ("G") and ChatGPT 5.2 Thinking ("C", or another T version of the next generations). "C" works better with Internet information search - the main task, highlight in markdown format via Chrome extension "ChatGPT Exporter", and "G" works better with text and scheme generation (through the "Google AI Studio" platform).
---

===

<prompt 1>
Analyze the attached file.
Generate with pinpoint replacements a chain of prompts for another AI model to research the drug [drug_name/or_product] from [enterprise_name].
Add more information on searching exclusively for exact data/parameters/indicators/numbers/fresh and current sources:

- appropriate apparatus for manufacturing this drug stage-by-stage (start from reactor apparatus to packaging machines).
- full assortment of the enterprise according to the Anatomical Therapeutic Chemical classification ATC (if it corresponds to a medicinal product).
- a prompt that would cover the technological parameters of preparation of [product_name]: only exact parameters, exact data, and sources from which the information was taken should be provided.
- a prompt that would cover all quality control methods of [product_name] according to the European Pharmacopoeia (Ph. Eur.) (if it is a medicinal product. AI model "G").
- separate prompts for searching appropriate images (factory, drug, active components, etc., which must be indicated in the new report according to the attached example). Maximum 3 images per one query. Images must be placed in an "HTML" file and under each found image must be mandatory: (1) caption, (2) link to the source from which the image was taken, (3) full citation in APA 7 style.

Maximum number of used found sources: 4-6.
Statements must be cited in the style (author, year).
Below after each response from the query: full citation in APA 7 style. Numbering is preserved for responses of subsequent queries.

Number of prompts: 6.
Perform the task in [number] separate queries from me "next".
</prompt 1>

===

<prompt 2>

If the enterprise and product are not medicinal, then this query should be skipped.

Provide the full assortment of [enterprise_name] according to the Anatomical Therapeutic Chemical classification ATC, where for each letter group (A, B, C, etc.) a list of trade names of drugs belonging to the corresponding therapeutic area is given. Example: attached image.

</prompt 2>

===

<prompt 3>

If the enterprise and product are not medicinal, then this query should be skipped.

- AI model "G".

What methods from the European Pharmacopoeia are needed for the analytical-normative document for the medicinal product [drug_name] from [enterprise_name]?

</prompt 3>

===

<prompt 4>

Analyze the attached European Pharmacopoeia file.
Extract into a separate PDF file the following methods from the file: {Ph. Eur. 0520 "Parenteral preparations"; Ph. Eur. 1648 "Thioctic acid"; 2.2.1. "Clarity and degree of opalescence of liquids"; 2.2.2. "Degree of coloration of liquids"; 2.2.3. "Potentiometric determination of pH"; 2.2.35. "Osmolality"; 2.9.17. "Test for extractable volume of parenteral preparations"; 2.9.20. "Particulate contamination: visible particles"; 2.9.19. "Particulate contamination: sub-visible particles"; 2.2.29. "Liquid chromatography"; 2.2.25. "Absorption spectrophotometry, ultraviolet and visible"; 2.6.1. "Sterility"; 2.6.14. "Bacterial endotoxins"; 3.2.1. "Glass containers for pharmaceutical use"; 3.2.9. "Rubber closures..."} (methods must be listed as in this prompt ["Method code" - "its name"]).

</prompt 4>

===

<prompt 5>

# Analyze three attached files. Context: I need to generate a full production practice report at [enterprise_name] with identical structure and writing style as in the file `Звіт з практики Фармак_Клименко М.А._БТ-4-1.pdf`. The drug to be described is [drug_name].

## Your task based on the analysis of the files is to generate a full detailed production practice report at [enterprise_name] describing the selected drug [drug_name]. Use an academic style of responses, with appropriate source citations in (author, year) and a separate list of used sources as a final generation, formatted fully in APA 7 style.

### Role of each attached file:

- `Звіт з практики Фармак_Клименко М.А._БТ-4-1.pdf` - ideal example of the structure and style of writing a production practice report for JSC "Farmak". Use it to generate a report with identical structure for [enterprise_name] for the drug I selected [drug_name].
- `База даних.md` - detailed information (input data) from the enterprise [enterprise_name] both on manufacturing the finished drug [drug_name] and general rules, settings, and information about the enterprise [enterprise_name] that must be used when generating the report.
- `EP7_Vol1_selected_methods.pdf` - European Pharmacopoeia methods for the section "Specification and methods" for the drug [drug_name].

If there is a lack of relevant data/gaps/no necessary images - mark as [gap, fill X]. Must have - type of factory [enterprise_name]; logo [enterprise_name], photo of the drug [drug_photo]; photo of raw materials from which the drug is made; photo of active substance, etc.

### Perform the task in [number] separate queries from me "next". Prompt details:
1. Maximize detail. Use bullets only if really necessary.
2. Write out subsection "4.5. Description of the technological process of production of the target product" for the drug [drug_name], as done in the file `Звіт з практики Фармак_Клименко М.А._БТ-4-1.pdf`, using input data from the file `База даних.md`. Without bullets.
Perform this in two separate queries "next".
3. Write out subsection "4.6. Production control", as done in the file `Звіт з практики Фармак_Клименко М.А._БТ-4-1.pdf`, using input data from the file `База даних.md`. Without bullets. All relevant tables must be present.
Perform this in three separate queries "next".
4. Write out each method as done in `Звіт з практики Фармак_Клименко М.А._БТ-4-1.pdf`. The table "Specification for the finished medicinal product [drug_name]" must be filled as clearly as possible for all indicators.
5. After completion, we will proceed to further report generation "to move to Section 5 (Engineering systems) and Section 6 (Environmental protection)." For each section, 3 separate queries "next".
6. Generate in a separate response the entire list of used sources in APA 7 style from the files attached above, without paraphrasing/shortening or other modifications.
7. After generating the entire work, generate by a separate query "next" an "Abstract" in the style and structure as in `Звіт з практики Фармак_Клименко М.А._БТ-4-1.pdf`.

### Perform the task in [number] separate queries from me "next". Prompt details:

1. Generate section 1 from start to finish in two separate "next" requests.
2. Generate section 2 in two separate "next" requests.
3. Generate section 3 in two separate "next" requests.
4. Generate section 4 in three separate "next" requests from me. Maximize detail.
5. For the Technological Equipment Specification Table - use identical equipment as in `Звіт з практики Фармак_Клименко М.А._БТ-4-1.pdf`. (one "next" request).
6. Maximize detail of the production control points for the drug [drug_name]. (one "next" request).
7. Quality control of finished products - identical in structure and description volume as in `Звіт з практики Фармак_Клименко М.А._БТ-4-1.pdf`. (four "next" requests).
8. [If this is a medicinal product. If not - skip this step]. Generate a description of microorganisms according to ДФУ 2.6.12 and ДФУ 2.6.13, as done in the file `Звіт з практики Фармак_Клименко М.А._БТ-4-1.pdf`. Combine the last answer with the new one through a paraphrased excerpt: "In the production of sterile medicinal products, any presence of microorganisms is considered contamination, so it is important to pay attention to the most common microbial contaminants in pharmaceutical processes. Among such potential contaminants are *Escherichia coli*, *Pseudomonas aeruginosa*, *Candida albicans*, *Aspergillus brasiliensis* (formerly A. niger), *Salmonella enterica*, and others, for example *Staphylococcus aureus* - all of which can negatively affect the microbiological purity of the product and are criteria for rejection of finished products."
9. Generate section 5 in two separate "next" requests.
10. Generate section 6 in two separate "next" requests.
11. Generate in a separate response the entire list of used sources in the original APA 7 style from the attached files above, without paraphrasing/shortening or other modifications.
12. Generate the "Abstract" in the style and structure as in `Звіт з практики Фармак_Клименко М.А._БТ-4-1.pdf`.

</prompt 5>

===

<prompt 6>

You are an expert in generating a technological scheme for the production of medicinal products in ASCII format. Your task, following the example of the technological scheme attached as the file `Технологічна_схема_Пектолван Плющ_Клименко М.А._А3.pdf`, with identical style, construction logic, and using input data from the production practice report `Звіт_з_виробничої_практики_Фармекс Груп.pdf`, is to generate a technological scheme in SVG format for the selected "Gipromeloza-Farmex" drug. Decompose stages that can be decomposed.

Maximize detail for each substage.
Perform the task in four separate "next" requests.

</prompt 6>

===

<prompt 7>

Your task is to generate for each apparatus from the `Technological Equipment Specification` table (of the currently generated report) a separate vector schematic image in a professional scheme without rounded corners, following the style, structure, and volume as in the example "<example>".
Format: SVG in the code window.

<example>
<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 600 400">
  <defs>
    <style>
      .main-lines { fill: none; stroke: black; stroke-width: 3; stroke-linecap: square; stroke-linejoin: miter; }
      .thin-lines { fill: none; stroke: black; stroke-width: 2; }
      .dashed-lines { fill: none; stroke: black; stroke-width: 2; stroke-dasharray: 5,5; }
      .hatch { stroke: black; stroke-width: 1; }
      .text { font-family: 'Arial', sans-serif; font-size: 24px; fill: black; }
      .label-text { font-family: 'Arial', sans-serif; font-size: 32px; font-weight: bold; fill: black; }
    </style>
  </defs>

  <!-- Floor level -->
  <line x1="50" y1="350" x2="550" y2="350" class="main-lines" />
  <!-- Floor hatching -->
  <line x1="50" y1="350" x2="30" y2="370" class="hatch" />
  <line x1="90" y1="350" x2="70" y2="370" class="hatch" />
  <line x1="130" y1="350" x2="110" y2="370" class="hatch" />
  <line x1="170" y1="350" x2="150" y2="370" class="hatch" />
  <line x1="210" y1="350" x2="190" y2="370" class="hatch" />
  <line x1="250" y1="350" x2="230" y2="370" class="hatch" />
  <line x1="290" y1="350" x2="270" y2="370" class="hatch" />
  <line x1="330" y1="350" x2="310" y2="370" class="hatch" />
  <line x1="370" y1="350" x2="350" y2="370" class="hatch" />
  <line x1="410" y1="350" x2="390" y2="370" class="hatch" />
  <line x1="450" y1="350" x2="430" y2="370" class="hatch" />
  <line x1="490" y1="350" x2="470" y2="370" class="hatch" />
  <line x1="530" y1="350" x2="510" y2="370" class="hatch" />

  <!-- Conveyor -->
  <line x1="50" y1="250" x2="550" y2="250" class="main-lines" />
  <line x1="50" y1="260" x2="550" y2="260" class="main-lines" />
  
  <!-- Conveyor supports -->
  <line x1="100" y1="260" x2="100" y2="350" class="thin-lines" />
  <line x1="500" y1="260" x2="500" y2="350" class="thin-lines" />

  <!-- Label applicator (Sleeve) -->
  <rect x="150" y="100" width="100" height="150" class="main-lines" />
  
  <!-- Label roll -->
  <circle cx="200" cy="130" r="20" class="thin-lines" />
  <line x1="200" y1="150" x2="200" y2="200" class="thin-lines" /> <!-- Sleeve feed -->
  
  <!-- Cutter/Cutting mechanism -->
  <rect x="180" y="200" width="40" height="20" class="main-lines" />

  <!-- Steam tunnel (Heat shrink) -->
  <rect x="300" y="180" width="150" height="80" class="main-lines" />
  <line x1="300" y1="180" x2="450" y2="180" class="dashed-lines" /> <!-- In/Out -->
  
  <!-- Steam supply pipe -->
  <line x1="375" y1="180" x2="375" y2="150" class="thin-lines" />
  <line x1="375" y1="150" x2="400" y2="150" class="thin-lines" />
  <polygon points="390,145 400,150 390,155" fill="black" />

  <!-- Bottles on conveyor -->
  <!-- Before labeling -->
  <rect x="80" y="210" width="30" height="40" class="thin-lines" />
  <rect x="85" y="200" width="20" height="10" class="thin-lines" /> <!-- Neck -->
  
  <!-- Under applicator (with label) -->
  <rect x="200" y="210" width="30" height="40" class="thin-lines" />
  <rect x="200" y="220" width="30" height="20" class="hatch" /> <!-- Label -->
  
  <!-- In tunnel -->
  <rect x="360" y="210" width="30" height="40" class="dashed-lines" />
  
  <!-- Finished bottle -->
  <rect x="500" y="210" width="30" height="40" class="thin-lines" />
  <rect x="500" y="220" width="30" height="20" class="main-lines" fill="black" /> <!-- Shrunk label -->

  <!-- Leader and caption -->
  <line x1="200" y1="100" x2="200" y2="50" class="thin-lines" />
  <line x1="200" y1="50" x2="250" y2="50" class="thin-lines" />
  <text x="260" y="60" class="label-text">ЕТ-7</text>

  <!-- Text explanations -->
  <text x="120" y="120" class="text" text-anchor="end">Roll</text>
  <text x="400" y="140" class="text" text-anchor="start">Steam</text>
</svg>
</example>

</prompt 7>

===

<prompt 8>
`Analyze the attached apparatus scheme file.
Mark for me exactly what needs to be changed according to the description of the technological scheme so that the concept matches.`
</prompt 8>

===

<prompt 9>
`Analyze the attached files of the finished production practice report, technological and apparatus schemes.
Conduct an audit of the work for all existing inconsistencies and errors/mistakes that need correction.
Perform the task in two separate "next" requests from me.`
</prompt 9>

===
~~~

</details>

## Examples and Demo Materials

No separate PNG/PDF/PPTX demo material is attached to this publication yet. When an example output exists, add it under `examples/` and link it from this section.

## Related Versions

- - [Українська версія](../uk/production-practice-report-scheme-generator.md)
- - [Category: Practice reports](../../categories/practice-reports.md)
- - [All prompts](../../prompts/index.md)

## Source

Original local source: [Промпти_звіт з виробничої практики.md](../../source/%D0%9F%D1%80%D0%BE%D0%BC%D0%BF%D1%82%D0%B8_%D0%B7%D0%B2%D1%96%D1%82%20%D0%B7%20%D0%B2%D0%B8%D1%80%D0%BE%D0%B1%D0%BD%D0%B8%D1%87%D0%BE%D1%97%20%D0%BF%D1%80%D0%B0%D0%BA%D1%82%D0%B8%D0%BA%D0%B8.md)
