# Examination Commission Submission Form Filler

`Language: EN` `Qualification document forms` `Source file: Мета-промпт_подання голові ЕК.md`

## What This Prompt Is

A Ukrainian prompt for completing the submission to the head of the examination commission.

## Purpose

Use it to prepare the commission-facing administrative form from thesis data and examples.

## What You Can Generate

- Completed submission form
- Defense-related data fields
- Example-matched formatting

## Expected Results

- Cleaner defense-document package
- Reduced missing field risk
- More consistent administrative style

## Inputs to Prepare

- Blank submission DOCX
- Example DOCX
- Structured thesis data

## How to Use

- Open the language version you need.
- Copy the full prompt block.
- Attach the files or links expected by the prompt.
- After the first run, fill in any variables or clarifications requested by the model.

## Prompt

<details open>
<summary>Prompt text</summary>

~~~markdown
Your task: fill out the submission form to the head of the examination committee regarding the defense of the qualification work.

Input files:
1. Submission form to the head of the EC (examination committee) DOCX.
2. Example filled file DOCX.
3. General data of the candidate in text format.

Output format: DOCX.
Output file name: Submission_to_head_of_EC_{Surname}.docx

Before generation, check if all necessary data are present:
- candidate's first name and SURNAME;
- candidate's full name;
- exact topic of the qualification work;
- first name and SURNAME of the supervisor;
- distribution of grades according to the national scale in percentages;
- distribution of grades according to the ECTS scale in percentages;
- uniqueness percentage of the work, if this field is present in the form.

If at least one field is missing, do not create the DOCX. Clearly state which data are missing.

Filling rules:
- Fill out exactly the form, do not create a document from scratch.
- Preserve the structure, tables, fields, underlines, spacing, and fonts (Times New Roman) of the form.
- Use the example file only for the style of data placement and name format.
- Do not copy from the example other people's full names, topics, grades, percentages, uniqueness, or supervisors.
- Follow the name formats:
  - “Sent to…” — candidate's first name and SURNAME in italics;
  - “Certificate of achievement…” — candidate's first name and SURNAME in italics;
  - “Secretary of the institute (faculty)” — Alina PRYKHUDKO in italics;
  - “Supervisor's conclusion on the qualification work…” — candidate's first name and SURNAME in italics;
  - “Supervisor of the work…” — supervisor's first name and SURNAME in italics;
  - “Candidate's qualification work…” — candidate's first name and SURNAME in the required case in italics.
- Fill in the grade distributions only from the provided data, do not invent percentages.
- Names of microorganisms, for example Aspergillus niger, should be italicized in the topic and text.
- Bold formatting of field names does not transfer to the inserted text.
- The supervisor's conclusion on the qualification work is not filled out.
~~~

</details>

## Examples and Demo Materials

No separate PNG/PDF/PPTX demo material is attached to this publication yet. When an example output exists, add it under `examples/` and link it from this section.

## Related Versions

- - [Українська версія](../uk/examination-commission-submission-form-filler.md)
- - [Category: Qualification document forms](../../categories/qualification-document-forms.md)
- - [All prompts](../../prompts/index.md)

## Source

Original local source: [Мета-промпт_подання голові ЕК.md](../../source/%D0%9C%D0%B5%D1%82%D0%B0-%D0%BF%D1%80%D0%BE%D0%BC%D0%BF%D1%82_%D0%BF%D0%BE%D0%B4%D0%B0%D0%BD%D0%BD%D1%8F%20%D0%B3%D0%BE%D0%BB%D0%BE%D0%B2%D1%96%20%D0%95%D0%9A.md)
