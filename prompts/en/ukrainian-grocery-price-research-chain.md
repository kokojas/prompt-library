# Ukrainian Grocery Price Research Chain

`Language: EN` `Research and web workflows` `Source file: промпт_продукти.md`

## What This Prompt Is

A chain of prompts for researching grocery prices across Ukrainian stores and producing Ukrainian output.

## Purpose

Use it to compare ATB, SILPO, and NOVUS prices with citations and a structured final list.

## What You Can Generate

- Store-by-store price research
- Cited price table
- Ukrainian final recommendations

## Expected Results

- More complete price coverage
- Traceable sources
- Cleaner shopping comparison

## Inputs to Prepare

- Product list
- Target stores
- Current web access

## How to Use

- Open the language version you need.
- Copy the full prompt block.
- Attach the files or links expected by the prompt.
- After the first run, fill in any variables or clarifications requested by the model.

## Prompt

<details open>
<summary>Prompt text</summary>

~~~markdown
# Chain of Prompts for ChatGPT 5.2 Thinking (Web Price Research)

Use these prompts in order (1 -> 7).  
Language of prompts: English. **Output: Ukrainian.**  
Target stores: `ATB`, `SILPO`, `NOVUS`.

---

## Prompt 1 - Initial Setup & ATB Baseline Collection

You are ChatGPT 5.4 Thinking acting as a grocery price intelligence analyst.

**Global Rules (Apply to all steps):**
1. **Scope:** Compare exact product keys across ATB, SILPO, NOVUS.
2. **Normalization:** Meat/deli -> UAH/1kg. Keep pack price/size + add normalized unit price. Keep 2 decimals.
3. **Output Format:** Output a table with columns: `Product key | Store | Exact product name | Brand | Pack size | Current price (UAH) | Promo (%) | Normalized price (UAH/unit) | Unit | Product URL | Last checked datetime (Kyiv)`. Add short "Matching decisions" and "Data quality flags" sections.

**Master Basket (Memorize for all steps):**
- **Meat/Deli:** Chicken (1.5kg), pork (1.5kg).
- **Dairy/Eggs:** Eggs (20pcs), milk (1L), sour cream (200ml), butter (1 pack 180-200g), processed cheese (3 packs), hard cheese (300g).
- **Pantry:** Mayonnaise (1 pack 500ml), tomato paste (1 pack), ketchup (4 packs).
- **Beverages:** Sweet soda (2L).

**Goal for Prompt 1:** Collect ATB prices for each item in the Master Basket using official online sources. Output the results using the standard format.

---

## Prompt 2 - ATB Deep Search

Continue ATB research.

**Global Priority Groups (Memorize for all deep searches):**
1) Dairy specifics: Sour cream, butter, processed cheese, hard cheese
2) Pantry specifics: Mayonnaise, tomato paste, ketchup
3) Beverages: Sweet soda
**Deep Search Rules (Apply to all deep searches):** 
Keep top 3 candidates by normalized price per item, pick 1 winner. Capture promo mechanics. Ensure meat/deli is normalized (UAH/kg).

**Task:** Perform deep search for the groups above and return the lowest valid ATB options. 
**Output:** Section A (Winners table), Section B (Alternatives table), Section C (Confidence notes).

---

## Prompt 3 - NOVUS Baseline Collection

Continue analyst role.

**Task:** Collect **NOVUS** prices for the exact same **Master Basket** established in Prompt 1.
**Rules:** Apply all **Global Rules**.
**Output:** Standard table format, plus "Differences vs ATB mapping" (Columns: Product key | ATB match status | NOVUS match status | Notes) and "Data quality flags".

---

## Prompt 4 - NOVUS Deep Search

**Task:** Run deep search for **NOVUS** using the same **Global Priority Groups** and **Deep Search Rules** from Prompt 2. If no clean match exists, mark "No direct match" and explain.
**Output:** Winner table, Alternatives table, and Match rationale section for NOVUS.

---

## Prompt 5 - SILPO Baseline Collection

**Task:** Collect **SILPO** prices using the established **Master Basket** (Prompt 1).
**Rules:** Apply all **Global Rules**.
**Output:** Standard table format, plus "Differences vs ATB mapping" (Columns: Product key | ATB match status | SILPO match status | Notes) and "Data quality flags".

---

## Prompt 6 - SILPO Deep Search

**Task:** Run deep search for **SILPO** using the **Global Priority Groups** and **Deep Search Rules** (Prompt 2).
**Output:** Winner table, Alternatives table, and Match rationale section for SILPO.

---

## Prompt 7 - Build Final DOCX (Same Structure as `lowest_groceries_winners_table_weekly_check.docx`)


You are ChatGPT 5.4 Thinking acting as a report compiler.

Input:
- Use the collected outputs from Prompts 1-6 (ATB, SILPO, NOVUS).

Task:
Create a DOCX report with the same structure and content logic as the reference file `Аналіз цін {дата}.docx`. **Output language: Ukrainian.**

Formatting and structure requirements (must match template logic):
1) Title section:
   "Порівняльна таблиця найнижчих цін на продукти харчування (АТБ / NOVUS / SILPO)"

2) Table 1: Winners by item (lowest price across stores)
   Columns:
   Позиція | Продукт | Ціна | Акція | Магазин

3) Note under Table 1:
   Поясніть будь-які відсутні значення та як були обрані переможці, коли дані були неповними.

4) Section:
   "Розрахунки тижневої перевірки (загалом)"
   Subsection:
   "Примітки до розрахунку"
   Include notes on:
   - proportional recalculation for weighted items
   - practical rounding to full packs where needed

5) Table 2: Line-item weekly calculations (proportional)
   Columns:
   No. | Категорія | Продукт | Необхідна кількість | Ціна з таблиці переможців | Мінімальна сума, грн | Максимальна сума, грн | Примітка

6) Table 3: Category totals
   Columns:
   Категорія | Розрахована мінімальна сума, грн | Розрахована максимальна сума, грн | Практична мінімальна сума, грн | Практична максимальна сума, грн

7) Table 4: Final weekly check amount
   Columns:
   Сценарій | Мінімальна сума, грн | Максимальна сума, грн | Коментар
   Include scenarios:
   - Розрахований базовий
   - Практичний базовий

8) Final conclusion paragraph:
   Дайте остаточний діапазон перевірки тижня та чітко вкажіть припущення.

Output requirements:
- Return the report content ready for DOCX export.
- Keep all monetary values in UAH with 2 decimals.
- Keep product/store names consistent with collected data.
- Keep transparency: include brief assumptions for substitutions.
~~~

</details>

## Examples and Demo Materials

No separate PNG/PDF/PPTX demo material is attached to this publication yet. When an example output exists, add it under `examples/` and link it from this section.

## Related Versions

- - [Category: Research and web workflows](../../categories/research-and-web-workflows.md)
- - [All prompts](../../prompts/index.md)

## Source

Original local source: [промпт_продукти.md](../../source/%D0%BF%D1%80%D0%BE%D0%BC%D0%BF%D1%82_%D0%BF%D1%80%D0%BE%D0%B4%D1%83%D0%BA%D1%82%D0%B8.md)
