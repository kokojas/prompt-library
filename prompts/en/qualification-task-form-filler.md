# Qualification Task Form Filler

`Language: EN` `Qualification document forms` `Source file: Мета-промпт_завдання.md`

## What This Prompt Is

A Ukrainian prompt for filling the qualification-work task form from a blank, example, and thesis data.

## Purpose

Use it to produce a completed DOCX-style task form while preserving institutional formatting.

## What You Can Generate

- Completed task form
- Field-by-field data mapping
- Formatting notes

## Expected Results

- Faster administrative document preparation
- Fewer field omissions
- Closer match to examples

## Inputs to Prepare

- Blank DOCX
- Filled example DOCX
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
Your task: fill out the qualification work assignment form.

Input files:
1. Assignment form DOCX.
2. Example filled file DOCX.
3. General data of the candidate in text format.

Output format: DOCX.
Output file name: Assignment_{Surname}.docx

Before generation, check if all necessary data are present:
- Full name of the candidate;
- Exact topic of the qualification work;
- Full name of the supervisor;
- Scientific degree / position / academic title of the supervisor;
- Initial data for the work;
- Content of the explanatory note;
- List of graphic materials (only the number of pages in A1 format for the apparatus scheme and technological scheme is required);
- Calendar plan or sufficient data to form it.

If at least one field is missing, do not create the DOCX. Clearly state which data are missing.

Filling rules:
- Fill in the form itself, do not create a document from scratch.
- Preserve the structure, tables, fields, spacing, font (Times New Roman), and formatting of the form.
- Use the example file for the style of wording in the following sections:
  - “Initial data for the work”;
  - “Content of the explanatory note”;
  - “List of graphic materials”;
  - “Calendar plan”.
- Do not copy from the example other people’s full names, topic, biological agent, product, dates, or graphic materials.
- The order number and date are fixed: order 199кс dated 30.03.2026.
- In the list of graphic materials, indicate only the technological scheme and apparatus scheme. Do not add the biotransformation scheme or other materials unless explicitly specified by the user.
- Do not fill in the table “Consultants of the work sections.”
- Follow name formats:
  - SURNAME first name patronymic of the candidate in italics;
  - “Supervisor…” — SURNAME first name and patronymic of the supervisor in italics;
- In the calendar plan, the text of the stages should be non-bold.
- At the end of the document, in the signature lines, indicate only the first name and SURNAME of the candidate and supervisor in italics.
- Names of microorganisms, for example Aspergillus niger, should be italicized throughout the document.
- Bold formatting of field names, as in the form, is not transferred to the inserted text in the blanks. If a field has a bold heading, the inserted content after it should be normal unless the example explicitly requires otherwise.
~~~

</details>

## Examples and Demo Materials

No separate PNG/PDF/PPTX demo material is attached to this publication yet. When an example output exists, add it under `examples/` and link it from this section.

## Related Versions

- - [Українська версія](../uk/qualification-task-form-filler.md)
- - [Category: Qualification document forms](../../categories/qualification-document-forms.md)
- - [All prompts](../../prompts/index.md)

## Source

Original local source: [Мета-промпт_завдання.md](../../source/%D0%9C%D0%B5%D1%82%D0%B0-%D0%BF%D1%80%D0%BE%D0%BC%D0%BF%D1%82_%D0%B7%D0%B0%D0%B2%D0%B4%D0%B0%D0%BD%D0%BD%D1%8F.md)
