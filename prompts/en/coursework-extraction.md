# Coursework Extraction Prompt

`Language: EN` `Extraction prompts` `Source file: Курсова робота_для витягу.md`

## What This Prompt Is

A Ukrainian prompt for extracting required sections from a coursework file verbatim.

## Purpose

Use it to preserve original coursework sections for later synthesis or citation mapping.

## What You Can Generate

- Verbatim section extracts
- Original formatting preservation
- Clean extraction boundaries

## Expected Results

- Less source drift
- Easier reuse in larger workflows
- More reliable assembly

## Inputs to Prepare

- Coursework file
- Section list

## How to Use

- Open the language version you need.
- Copy the full prompt block.
- Attach the files or links expected by the prompt.
- After the first run, fill in any variables or clarifications requested by the model.

## Prompt

<details open>
<summary>Prompt text</summary>

~~~markdown
You are working with the file "Курсова робота...".
Your task is to extract the sections of the text specified below without changes, preserving the original formatting, in PDF format.

Extract the following parts:
1. "SECTION 1. CHARACTERISTICS OF THE TARGET BIOSYNTHESIS PRODUCT" (in full). This will go into SECTION 1 of the final work.
2. "SECTION 2. JUSTIFICATION OF THE CHOICE OF BIOLOGICAL AGENT" (in full). This will go into SECTION 2 (items 2.1, 2.2) of the final work.
3. From "SECTION 3" extract only the subsections "3.1. Selection of conditions and method of biosynthesis..." and "3.2. Selection of fermenter type". This will go into SECTION 5 (item 5.1) of the final work.

IMPORTANT CONDITION: In the text of these sections there are references to literature in square brackets (for example, [2], [6]). You must keep these numbers in the text without any changes. After the extracted text, create a heading "LIST OF SOURCES USED FOR THIS BLOCK" and list there from the original bibliography list (which is at the end of the document) ONLY those sources whose numbers appear in the text you extracted. Leave the bibliographic descriptions of the sources in their original form without changes.
~~~

</details>

## Examples and Demo Materials

No separate PNG/PDF/PPTX demo material is attached to this publication yet. When an example output exists, add it under `examples/` and link it from this section.

## Related Versions

- - [Українська версія](../uk/coursework-extraction.md)
- - [Category: Extraction prompts](../../categories/extraction-prompts.md)
- - [All prompts](../../prompts/index.md)

## Source

Original local source: [Курсова робота_для витягу.md](../../source/%D0%9A%D1%83%D1%80%D1%81%D0%BE%D0%B2%D0%B0%20%D1%80%D0%BE%D0%B1%D0%BE%D1%82%D0%B0_%D0%B4%D0%BB%D1%8F%20%D0%B2%D0%B8%D1%82%D1%8F%D0%B3%D1%83.md)
