# Pre-Diploma Practice Gap Analysis

`Language: EN` `Practice reports` `Source file: Звіт з переддипломної практики.md`

## What This Prompt Is

A Ukrainian prompt for identifying missing exact data, parameters, and source evidence in pre-diploma practice materials.

## Purpose

Use it to find critical gaps before writing or finalizing a pre-diploma practice report.

## What You Can Generate

- Gap list
- Missing parameter checklist
- Questions for data collection

## Expected Results

- Fewer unsupported claims
- Clearer data-collection plan
- Better report readiness

## Inputs to Prepare

- Attached practice files
- Target product/process
- Available source data

## How to Use

- Open the language version you need.
- Copy the full prompt block.
- Attach the files or links expected by the prompt.
- After the first run, fill in any variables or clarifications requested by the model.

## Prompt

<details open>
<summary>Prompt text</summary>

~~~markdown
Analyze the attached files.
Your task is to identify critical data gaps (exact indicators, technological parameters, numbers up to percentages) that will be missing when generating the pre-diploma practice report and generate the corresponding search chain of prompts to fully disclose the report. Do not consider replacing exact critical data from your own database – use the generation of chain of prompts queries for another AI model. Every technological indicator must be disclosed.
Input data for generation – attached files:
- `Курсова_робота_Клименко_М_А_БТ_3_1_1 (2).pdf` – for section 2.
- `Звіт з практики Фармак_Клименко М.А._БТ-4-1.pdf` – for section 3.

Perform the task in two steps: (1) planning and searching for critical data, (2) generating search chain of prompts for another AI model (6 prompts); when generating answers by another model, source citations must be in the style (author, year). The maximum number of sources per one prompt in the chain of prompts is 4.

===

Analyze the attached file of results of all 5 prompt queries.
Your task is to generate the pre-diploma practice report according to the structure below, using the input data from the attached files above `Курсова_робота_Клименко_М_А_БТ_3_1_1 (2).pdf` and `Звіт з практики Фармак_Клименко М.А._БТ-4-1.pdf`:
"""To complete the pre-diploma practice report, the student during the practice must work through the following sections:
INTRODUCTION
Section length – at least 2 pages
SECTION 1. Characteristics of the finished product according to the enterprise profile.
Section length – 1-2 pages
SECTION 2. Characteristics of the target product
Section length – 3-5 pages
SECTION 3. Main stages of isolation and purification of the target product
Section length – at least 5 pages
SECTION 4. Corrections to the course project on the discipline
"Design of Biotechnological Productions" (do not fill this section, leave just the template)
CONCLUSIONS"""

For each section, there should be two separate requests from me "next". Maximize the detail of technological and production parameters if the context requires it. Cite used sources in the text as (author, year).
No bullet points and no unnecessary "greetings" or "task completion reports".

===

next

===

Highlight in the original state the sources used for writing the pre-diploma practice report.

===

Analyze the attached files.
Your task is to identify critical data gaps (exact indicators, technological parameters, numbers up to percentages) that will be missing when generating the pre-diploma practice report and generate the corresponding search chain of prompts to fully disclose the report. Do not consider replacing exact critical data from your own database – use the generation of chain of prompts queries for another AI model. Every technological indicator must be disclosed.
Input data for generation – attached files:
- `Курсова_робота_Клименко_М_А_БТ_3_1_1 (2).pdf` – for section 2.
- `Звіт з практики Фармак_Клименко М.А._БТ-4-1.pdf` – for section 3.

Perform the task in two steps: (1) planning and searching for critical data, (2) generating search chain of prompts for another AI model (6 prompts); when generating answers by another model, source citations must be in the style (author, year). The following must be found: some articles on 2-KGK itself, articles on isolation and purification of 2-KGK from the culture fluid of the selected microorganism in the attached work. The maximum number of sources per one prompt in the chain of prompts is 4.
~~~

</details>

## Related Versions

- [Українська версія](../uk/pre-diploma-practice-gap-analysis.md)
- [Category: Practice reports](../../categories/practice-reports.md)
- [All prompts](../../prompts/index.md)

## Source

Original local source: [Звіт з переддипломної практики.md](../../source/%D0%97%D0%B2%D1%96%D1%82%20%D0%B7%20%D0%BF%D0%B5%D1%80%D0%B5%D0%B4%D0%B4%D0%B8%D0%BF%D0%BB%D0%BE%D0%BC%D0%BD%D0%BE%D1%97%20%D0%BF%D1%80%D0%B0%D0%BA%D1%82%D0%B8%D0%BA%D0%B8.md)
