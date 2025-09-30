# Ex.No.3 – Scenario-Based Report Development  
**Utilizing Diverse Prompting Techniques**

---

### DATE: 27-09-2025
### REGISTER NUMBER: 212222060103

---

## Aim
To design and evaluate prompts for **four major prompt-engineering types**—Straightforward, Tabular Format, Preceding Question, and Missing Word—by applying them to a selected Unit-5 use case and assessing one prompt using a defined rubric.

---

## Introduction
Prompt engineering is the art of structuring questions or instructions so that a language model produces **precise, context-aware responses**.  
This exercise explores four prompting styles and demonstrates their impact on clarity and output quality.

### Selected Use Case (from Unit-5)
**Explainable AI – Fraud Detection**  
*Goal:* Explain why a black-box classifier predicts that a specific bank transaction is **fraudulent**.

---

## Procedure

### 1️⃣ Straightforward Prompts
Straightforward prompts are direct questions or commands expecting concise answers.

**Examples**
- “Define photosynthesis in one sentence.”  
- “List three advantages of electric vehicles.”

**Applied to Use Case**  
Prompt:  
`Explain why the black-box classifier predicted “fraudulent” for this bank transaction.`  

Sample Output:  
*The model flagged the transaction because of a high transfer amount, an unfamiliar merchant category, and a location outside the customer’s usual geography.*

---

### 2️⃣ Tabular Format Prompting
This method requests outputs in **structured tables** for better readability and comparison.

**Examples**
- “Compare and contrast AC and DC current in a table.”  
- “Provide a table listing five programming languages, their paradigms, and one use case each.”

**Applied to Use Case**  
Prompt:  
`Provide a table of features, their contributions (+/–), and explanations for the fraud prediction.`  

| Feature            | Contribution | Explanation                                        |
|--------------------|-------------:|----------------------------------------------------|
| Transaction Amount | +0.35        | Amount far above user’s typical spend              |
| Merchant Category  | +0.20        | Category frequently associated with fraud          |
| Location Deviance  | +0.15        | Occurred in a different city                       |
| Time of Day        | +0.05        | Happened at 3 a.m., outside normal activity hours  |
| Prior Chargebacks  | +0.10        | History of disputed transactions                   |

---

### 3️⃣ Preceding Question Prompting
Here the model answers a **general question first**, then uses that context for a specific query.

**Examples**
- “Why is climate change a global concern? Explain how greenhouse gases contribute to global warming.”  
- “How do vaccines work? Describe the process of immunization in simple terms.”

**Applied to Use Case**  
Prompt:  
`What factors generally cause a classifier to label a transaction fraudulent? Based on those, explain this specific case.`  

*Output begins with common factors such as unusual amount, risky merchant type, and abnormal timing, then applies them to the sample transaction.*

---

### 4️⃣ Missing Word Prompting
Prompts are phrased with **blanks** to encourage the model to fill in key terms.

**Examples**
- “The capital of France is ____.”  
- “In photosynthesis, plants absorb sunlight to produce ____.”

**Applied to Use Case**  
Prompt:  
`The feature Transaction Amount contributed ___ because it was ___ the user’s typical spending.`  

Sample Output:  
`positive … well above`

---

## Evaluation Method

The **Tabular Format Prompt** was evaluated using a simple rubric:

| Criterion                | Max | Score | Notes                                   |
|--------------------------|----:|------:|------------------------------------------|
| Completeness            | 2   | 1     | Missed one or two minor features         |
| Accuracy of contribution| 2   | 2     | Signs and magnitudes are plausible       |
| Clarity & readability   | 2   | 2     | Table is easy to read                    |
| Explanation quality     | 2   | 1     | Explanations could be slightly richer    |

**Total: 6 / 8 → Good performance, room for added feature details.**

---

## Process Flow Diagram

flowchart TD
    A[Input transaction data] --> B[Prompt Creation]
    B --> C[Model Response]
    C --> D[Evaluation with Rubric]
    D --> E[Prompt Refinement]

## conclusion 

By crafting prompts across these four styles, we observed how prompt structure directly influences output.

Straightforward prompts give quick insights.

Tabular prompts enhance comparison and clarity.

Preceding question prompts improve reasoning by layering context.

Missing word prompts focus the model on key facts.





## Result
The experiment was carried out successfully.  
All four prompt-engineering techniques—**Straightforward**, **Tabular Format**, **Preceding Question**, and **Missing Word**—were designed, executed, and evaluated on the selected Explainable-AI (fraud detection) use case.  
The outputs confirmed that **prompt structure strongly influences response clarity, depth, and readability**, meeting the objectives of Ex.No.3.


