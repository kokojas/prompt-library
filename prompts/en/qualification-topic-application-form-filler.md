# Qualification Topic Application Form Filler

`Language: EN` `Qualification document forms` `Source file: Мета-промпт_заява.md`

## What This Prompt Is

A Ukrainian prompt for filling the application form for approval of a qualification-work topic.

## Purpose

Use it to transfer thesis metadata into the correct administrative form style.

## What You Can Generate

- Completed application form
- Topic and student data mapping
- Formatting alignment

## Expected Results

- Fewer manual form errors
- Consistent wording
- Closer match to the provided example

## Inputs to Prepare

- Blank application DOCX
- Example DOCX
- Thesis topic data

## How to Use

- Open the language version you need.
- Copy the full prompt block.
- Attach the files or links expected by the prompt.
- After the first run, fill in any variables or clarifications requested by the model.

## Prompt

<details open>
<summary>Prompt text</summary>

~~~markdown
Your task: fill out the application form for approval of the qualification work topic.

Input files:
1. Application form DOCX.
2. Example filled file DOCX.
3. General data of the applicant in text format.

Output format: DOCX.
Output file name: Application_for_topic_{Surname}.docx

Before generation, check if all necessary data are present:
- Full name of the applicant;
- Academic group;
- Exact topic of the qualification work;
- Scientific degree / position / surname and initials of the supervisor;
- Date of the application, if it differs from the standard.

If at least one field is missing, do not create the DOCX. Clearly state which data are missing.

Filling rules:
- Fill in the form itself, do not create a document from scratch.
- Preserve the structure, fields, underlines, spacing, font (Times New Roman), and formatting of the form.
- Use the example file only for the style of filling in the full name, topic, group, and supervisor.
- Do not copy others’ full names, topic, group, date, or supervisor from the example.
- Follow name formats:
  - SURNAME first name patronymic of the applicant in italics;
  - “appoint as supervisor of the work…” — surname and initials of the supervisor in italics;
- The title of the application topic must be in italics.
- Names of microorganisms, for example Aspergillus niger, should be italicized in the topic.
- Present the supervisor in the format: scientific degree / position + surname and initials.
- Bold formatting of field names does not carry over to the inserted text in the blanks.
~~~

</details>

## Examples and Demo Materials

No separate PNG/PDF/PPTX demo material is attached to this publication yet. When an example output exists, add it under `examples/` and link it from this section.

## Related Versions

- - [Українська версія](../uk/qualification-topic-application-form-filler.md)
- - [Category: Qualification document forms](../../categories/qualification-document-forms.md)
- - [All prompts](../../prompts/index.md)

## Source

Original local source: [Мета-промпт_заява.md](../../source/%D0%9C%D0%B5%D1%82%D0%B0-%D0%BF%D1%80%D0%BE%D0%BC%D0%BF%D1%82_%D0%B7%D0%B0%D1%8F%D0%B2%D0%B0.md)
