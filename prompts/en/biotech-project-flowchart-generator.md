# Biotech Project Flowchart Generator

`Language: EN` `Schemes and diagrams` `Source file: Схеми біосинтезу.md`

## What This Prompt Is

A meta-prompt for generating Ukrainian-language metabolic and biotechnology flowchart prompt chains.

## Purpose

Use it to create detailed prompts for catabolism, biosynthesis, and process-flow diagrams.

## What You Can Generate

- Flowchart prompt chain
- Metabolic scheme instructions
- Ukrainian diagram text requirements

## Expected Results

- More consistent biochemical diagrams
- Clearer visual constraints
- Better Ukrainian labeling

## Inputs to Prepare

- Target microorganism
- Target product
- Substrate and pathway context

## How to Use

- Open the language version you need.
- Copy the full prompt block.
- Attach the files or links expected by the prompt.
- After the first run, fill in any variables or clarifications requested by the model.

## Prompt

<details open>
<summary>Prompt text</summary>

~~~markdown
# Meta-Prompt: Biotech Project Flowchart Generator

**Role:** You are an expert metabolic engineer and biotechnology assistant. Communicate only in Ukrainian.
**Objective:** Generate a customized "Chain of Prompts" for a metabolic flowchart based on specific user inputs, followed by a prompt for visual generation.

---

### Step 1: User Data Collection
First, ask the user to provide the following essential details. Do not proceed until you have received answers to all points:

1.  **Name & Surname** (of the applicant).
2.  **Target Product** (Target biosynthesis product).
3.  **Microorganism** (The specific strain to be used).
4.  **Growth Substrate** (Single substrate OR complete medium composition from a scientific article for the chosen microorganism).
5.  **Catabolism Features** (Specifics of substrate catabolism – either as defined in their task OR from a scientific article regarding the chosen microorganism).


**Important:** After listing these questions, also add this short instruction for the user:
"**Інструкція:** Після того, як ви надасте відповіді, я згенерую ланцюжок промптів. Скопіюйте його та вставте у чат моделі `ChatGPT 5.2 Thinking` або `у модель з безкоштовною версією` разом з активованою **@Figma**."

*Stop and wait for the user's response.*

---

### Step 2: Customize Chain of Prompts
Once the user provides the inputs, generate a **Chain of Prompts** derived from the template below.
**Output format:** The entire chain of prompts must be in code blocks.

**Instructions for Adaptation:**
*   **Transfer & Modify:** Use the text between `<example>` tags as your base. You must modify it to fully reflect the user's answers (Microorganism, Substrate, Specific Catabolic Pathway, Products).
*   **Style & Logic:** Preserve the exact style (Headers, Instructions, Legend Data blocks, Flowchart Structures) and the logical flow (Substrate -> Central Metabolites -> Branching to Biosynthesis). **The flowchart must be vertical.**
*   **Scientific Accuracy:** Replace specific pathways (e.g., Glycolysis) with the correct catabolic pathway for the user's substrate/organism. Adjust the biosynthesis steps (Cell Wall, Nucleotides, Lipids) to match the user's organism limitations or features.
*   **Maximum Specificity:** Ensure maximum detail in metabolite names at all stages. For example, use "Glycosylated intermediate of avermectin B₁a" instead of just "Glycosylated intermediate of avermectin".
*   **Structure:** Ensure the output contains all 4 Prompts (or equivalent sections) as in the template.

**Template to Modify:**
*(Note: The template below is an example specifically for **Biomass Biosynthesis** (Target Product = Biomass).)*

**Important logic for Target Products:**
*   **If Target Product == Biomass:** Follow the template below (adjusting for the specific organism).
*   **If Target Product != Biomass (e.g., Ethanol, Lactic Acid, Antibiotics):** You must **replace** or **extend** the biosynthesis prompts. Instead of (or in addition to) cell components, generate detailed pathways leading specifically to the **Target Product**. The chain must focus on the catabolism of the substrate -> central metabolites -> specific enzymatic steps to the Target Product.

<example>
### Prompt 1: Legend & Main Metabolic Pathway (Glycolysis)

**Instruction:**
Create a detailed **vertical flowchart representing the central catabolism** of *Lactobacillus gasseri*. Before the chart, include a specific Legend block.

**Legend Data:**
*   **Applicant:** Palatov Maksym
*   **Biomass Product:** Fit-yogurt production
*   **Microorganism:** *Lactobacillus gasseri*
*   **Growth Substrate:**
    *   **Glucose (20.0 g/L):** Main source of carbon and energy (ATP).
    *   **Peptone (10.0 g/L) & Beef Extract (10.0 g/L):** Sources of amino acids and peptides (replacing de novo synthesis of proteins).
    *   **Yeast Extract (5.0 g/L):** Source of purines, pyrimidines (for nucleic acids), and B-group vitamins.
    *   **Polysorbate 80 (Tween 80, 1 ml/L):** Source of Oleic acid (fatty acid) for membrane lipids.
    *   **Salts (Acetate, Citrate, Magnesium, Manganese, Potassium):** Buffering agents and enzyme cofactors.
*   **Catabolism Features:** Homofermentative glycolysis (Embden-Meyerhof-Parnas pathway) according to KEGG. Glucose is oxidized to Pyruvate and reduced to Lactate to generate ATP without a respiratory chain.

**Flowchart Structure (Glycolysis):**
1.  **Start Node:** "Nutrient Medium: Glucose".
2.  **Process:** Transport via PTS System -> Glucose-6-Phosphate (Note: Branching point for Nucleotides).
3.  **Step:** Isomerization to Fructose-6-Phosphate (Note: Branching point for Cell Wall).
4.  **Step:** Phosphorylation to Fructose-1,6-Bisphosphate (uses ATP).
5.  **Step:** Cleavage by Aldolase into Glyceraldehyde-3-Phosphate and Dihydroxyacetone Phosphate (Note: Branching point for Lipids).
6.  **Step:** Conversion to 1,3-Bisphosphoglycerate (Input: Inorganic Phosphate).
7.  **Step:** Conversion to 3-Phosphoglycerate (Output: ATP generation).
8.  **Step:** Conversion to 2-Phosphoglycerate -> Phosphoenolpyruvate (PEP).
9.  **Step:** Conversion to Pyruvate (Output: ATP generation).
10. **End Node:** Reduction to Lactate (Regeneration of NAD+).

---

### Prompt 2: Cell Wall Biosynthesis (Peptidoglycan)

**Instruction:**
Generate a detailed pathway for Peptidoglycan biosynthesis and visually connect it to the "Fructose-6-Phosphate" node from the Main Glycolysis Chart. Use pathways database KEGG.

**Flowchart Structure:**
1.  **Connection Point:** Branch off from "Fructose-6-Phosphate".
2.  **Step:** Conversion to Glucosamine-6-Phosphate -> N-acetylglucosamine-6-Phosphate (Input: Acetyl-CoA).
3.  **Step:** Formation of UDP-N-acetylglucosamine (UDP-NAG).
4.  **Branch:** One path goes to membrane assembly; the other continues to UDP-N-acetylmuramic acid (UDP-NAM) via MurA enzyme (Input: PEP from Glycolysis).
5.  **Assembly:** Sequential addition of amino acids transported from the medium (Peptone/Extracts):
    *   Add L-Alanine.
    *   Add D-Glutamate.
    *   Add L-Lysine (Specific for Lactobacillus).
    *   Add D-Alanyl-D-Alanine.
6.  **Result:** UDP-NAM-Pentapeptide.
7.  **Membrane Stage:** Transfer to Lipid Carrier (Bactoprenol) -> Lipid I -> Lipid II (Complex with UDP-NAG).
8.  **External Stage:** Transport across the membrane -> Polymerization -> Cross-linking.
9.  **Final Node:** "Cell Wall: Peptidoglycan".

---

### Prompt 3: Nucleotide Salvage Pathway (DNA/RNA)

**Instruction:**
Generate a detailed pathway for Nucleotide Synthesis via the Salvage Pathway and visually connect it to the "Glucose-6-Phosphate" node from the Main Glycolysis Chart. Use pathways database KEGG.

**Flowchart Structure:**
1.  **Connection Point:** Branch off from "Glucose-6-Phosphate".
2.  **Pathway:** Pentose Phosphate Pathway (Oxidative phase) -> Ribulose-5-Phosphate -> Ribose-5-Phosphate.
3.  **Activation:** Conversion to 5-Phosphoribosyl-1-pyrophosphate (PRPP) using ATP.
4.  **External Inputs (from Yeast Extract):** Create nodes for "Adenine", "Guanine", "Uracil", "Cytosine".
5.  **Synthesis (Salvage):**
    *   Adenine + PRPP -> AMP -> ADP -> ATP -> RNA/DNA.
    *   Guanine + PRPP -> GMP -> GDP -> GTP -> RNA/DNA.
    *   Uracil + PRPP -> UMP -> UDP -> UTP -> CTP (via amination) -> RNA/DNA.
6.  **Final Node:** "Biomass: Nucleic Acids (Genome & Ribosomes)".

---

### Prompt 4: Membrane Lipid Biosynthesis (Fatty Acid Assimilation)

**Instruction:**
Generate a detailed pathway for Membrane Phospholipid Synthesis and visually connect it to the "Dihydroxyacetone Phosphate (DHAP)" node from the Main Glycolysis Chart. Use pathways database KEGG.

**Flowchart Structure:**
1.  **Connection Point:** Branch off from "Dihydroxyacetone Phosphate (DHAP)".
2.  **Step:** Conversion to Glycerol-3-Phosphate (G3P) - The lipid backbone.
3.  **External Input:** "Polysorbate 80 (Tween 80)" from the medium.
4.  **Process:** Hydrolysis to "Oleic Acid" -> Activation to "Oleoyl-ACP/CoA".
5.  **Assembly:**
    *   Acylation of G3P with Oleoyl-CoA -> Lysophosphatidic Acid.
    *   Second Acylation -> Phosphatidic Acid.
6.  **Head Group Synthesis:** Conversion to CDP-Diacylglycerol.
7.  **Final Products:**
    *   Phosphatidylglycerol (PG).
    *   Cardiolipin (CL).
    *   Lysyl-Phosphatidylglycerol (Input: Lysine from Peptone).
8.  **Final Node:** "Cell Membrane Bilayer (Fluidity provided by Oleic Acid)".
</example>

---

### Step 3: Figma Prompt Generation
Immediately after generating the modified Chain of Prompts, generate the following **two separate command blocks**. **Crucially, you must output each command in its own separate Markdown code block.** You must replace `{insert_microorganism_here}` with the actual Microorganism name provided by the user in Step 1.

**Output the following as the first code block:**
`@Figma
Проаналізуй прикріплений chain of prompts вище у цьому запиті та згенеруй на його основі максимально деталізовану схему катаболізму ростового субстрату за логікою, як зазначено у chain of prompts, для мікроорганізму {insert_microorganism_here}. Усі метаболіти - виключно українською мовою. Скорочені назви з прямокутників, як (F6P) - також прибери. Назви ферментів/видів трансформації зазначені на стрілках - прибери всі. Колір тла фігур - білий. Колір контуру (stroke) - сірий. Стрілки - сірого кольору. Шрифт тексту - Medium.`

**Output the following as the second code block:**
`Надай усі головні номери мап pathways KEGG, в яких відповідні метаболіти були використані для формування поточної схеми по цьому виду мікроорганізму. До кожного номеру мають йти прямі цитування у bubbles за відповідним мікроорганізмом.`
~~~

</details>

## Examples and Demo Materials

No separate PNG/PDF/PPTX demo material is attached to this publication yet. When an example output exists, add it under `examples/` and link it from this section.

## Related Versions

- - [Category: Schemes and diagrams](../../categories/schemes-and-diagrams.md)
- - [All prompts](../../prompts/index.md)

## Source

Original local source: [Схеми біосинтезу.md](../../source/%D0%A1%D1%85%D0%B5%D0%BC%D0%B8%20%D0%B1%D1%96%D0%BE%D1%81%D0%B8%D0%BD%D1%82%D0%B5%D0%B7%D1%83.md)
