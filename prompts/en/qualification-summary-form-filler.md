# Qualification Summary Form Filler

`Language: EN` `Qualification document forms` `Source file: Мета-промпт_резюме.md`

## What This Prompt Is

A Ukrainian prompt for filling the qualification-work summary/abstract form.

## Purpose

Use it to create a concise summary with exact product, organism, process, volume, and bibliographic details.

## What You Can Generate

- Abstract/resume text
- Keywords
- Work-volume details
- Right-aligned signature block guidance

## Expected Results

- More specific summaries
- Fewer generic claims
- Better match to institutional examples

## Inputs to Prepare

- Blank resume DOCX
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
Your task: fill out the resume form for the qualification work.

Input files:
1. Resume form DOCX.
2. Example filled file DOCX.
3. General data of the applicant in text format.

Output format: DOCX.
Output file name: Resume_{Surname}.docx

Before generation, check if all necessary data are present:
- exact topic of the qualification work;
- course;
- group;
- first name and SURNAME of the applicant;
- full name or initials of the supervisor in the required format;
- exact product / object of the work;
- biological agent or microorganism;
- key technological parameters of the work;
- volume of work in pages;
- number of tables;
- number of figures;
- number of sources;
- keywords or sufficient data to form them.

If at least one field is missing, do not create the DOCX. Clearly state which data are missing.

Filling rules:
- Fill out exactly the form, do not create a document from scratch.
- Preserve the structure, fields, spacing, fonts (Times New Roman), and layout from the form.
- Use the example file for the resume style: short annotation, concise introduction, practical/scientific value, volume of work, keywords.
- Do not copy from the example other people’s full names, topic, product, microorganism, production parameters, or number of pages.
- The topic title in the resume must be italicized.
- Names of microorganisms, for example Aspergillus niger, should be italicized throughout the document.
- Follow name formats:
  - first name and SURNAME of the applicant in italics;
  - “Supervisor…” — surname and initials of the supervisor in italics;
- The annotation must be specific, not general. Include exact data from the provided text: target product, microorganism/strain, cultivation method, product purpose, fermenter volume or other calculated parameters, volume of work, number of tables, figures, and sources.
- In the keywords line, highlight only the phrase “Keywords:” in bold italics. Write the keywords themselves in normal style, except microorganism names, which must be italicized.
- The block “Performed by: applicant…”, including the applicant’s full name and signature space, must be right-aligned as in the example.
- Bold formatting of field names does not carry over to inserted text.
~~~

</details>

## Examples and Demo Materials

Relevant PNG/PDF or PPTX materials are included below for personal review of what this prompt can generate or support.

### View PNG demo: `20.png`

![Demo asset: 20.png](../../examples/20.png)

## Related Versions

- [Українська версія](../uk/qualification-summary-form-filler.md)
- [Category: Qualification document forms](../../categories/qualification-document-forms.md)
- [All prompts](../../prompts/index.md)

## Source

Original local source: [Мета-промпт_резюме.md](../../source/%D0%9C%D0%B5%D1%82%D0%B0-%D0%BF%D1%80%D0%BE%D0%BC%D0%BF%D1%82_%D1%80%D0%B5%D0%B7%D1%8E%D0%BC%D0%B5.md)
