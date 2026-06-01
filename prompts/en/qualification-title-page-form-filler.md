# Qualification Title Page Form Filler

`Language: EN` `Qualification document forms` `Source file: Мета-промпт_титульна сторінка.md`

## What This Prompt Is

A Ukrainian prompt for filling the title page form for a qualification thesis.

## Purpose

Use it to transfer student, topic, supervisor, department, and year fields into the title-page template.

## What You Can Generate

- Completed title page
- Field mapping
- Example-matched formatting

## Expected Results

- Fewer title-page mistakes
- Consistent administrative style
- Faster document preparation

## Inputs to Prepare

- Blank title-page DOCX
- Example DOCX
- Thesis metadata

## How to Use

- Open the language version you need.
- Copy the full prompt block.
- Attach the files or links expected by the prompt.
- After the first run, fill in any variables or clarifications requested by the model.

## Prompt

<details open>
<summary>Prompt text</summary>

~~~markdown
Your task: fill in the qualification work title page template.

Input files:
1. Title page template DOCX.
2. Example filled-in file DOCX.
3. General applicant data in text format.

Output format: DOCX.
Output file name: Title_Page_{Surname}.docx

Before generation, check if all necessary data are present:
- exact topic of the qualification work;
- full name of the applicant;
- course;
- group;
- full name of the supervisor;
- surname and name of the reviewer.

If at least one field is missing, do not create the DOCX. Clearly specify which data are missing.

Filling rules:
- Fill in the template itself, do not create the document from scratch.
- Preserve style, layout, fonts (Times New Roman), underlining, tables, and spacing from the template.
- Use the example file only to understand how the filled title page looks.
- Do not copy others’ full names, topic, group, supervisor, or other factual data from the example.
- The title page fields to fill are: topic, course, group, applicant’s full name in italics, supervisor’s full name in italics, and reviewer’s surname and name in italics.
- Microorganism names in the topic, for example Aspergillus niger, must be italicized.
- Bold formatting from field labels/names is not transferred to the text inserted into the blanks.
~~~

</details>

## Examples and Demo Materials

No separate PNG/PDF/PPTX demo material is attached to this publication yet. When an example output exists, add it under `examples/` and link it from this section.

## Related Versions

- - [Українська версія](../uk/qualification-title-page-form-filler.md)
- - [Category: Qualification document forms](../../categories/qualification-document-forms.md)
- - [All prompts](../../prompts/index.md)

## Source

Original local source: [Мета-промпт_титульна сторінка.md](../../source/%D0%9C%D0%B5%D1%82%D0%B0-%D0%BF%D1%80%D0%BE%D0%BC%D0%BF%D1%82_%D1%82%D0%B8%D1%82%D1%83%D0%BB%D1%8C%D0%BD%D0%B0%20%D1%81%D1%82%D0%BE%D1%80%D1%96%D0%BD%D0%BA%D0%B0.md)
