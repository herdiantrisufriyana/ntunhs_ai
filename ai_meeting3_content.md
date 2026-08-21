# Prompt Engineering for Healthcare

**Herdiantri Sufriyana**
Graduate Institute of Artificial Intelligence and Big Data in Healthcare
National Taiwan University of Nursing and Health Sciences

---

## Subtopics

- Principles of effective prompting
- Zero-shot, few-shot, chain-of-thought
- Healthcare-specific prompting strategies
- Hands-on: Designing prompts for clinical scenarios

---

## Session 1: Lecture — Principles of Effective Prompting (25 mins)

---

## What is Prompt Engineering?

**Prompt engineering** is the practice of designing input instructions to get the best possible output from an AI model. The same AI can give vastly different answers depending on how you ask.

**Why it matters in healthcare:**
- A vague prompt can produce a generic or dangerously incomplete response
- A well-structured prompt can produce a clinically useful, evidence-based answer
- The difference is not the AI's capability — it is how you communicate with it

---

## Five Principles of Effective Prompts

| Principle | Description | Example |
|-----------|------------|---------|
| **1. Be specific** | State exactly what you need | "List 5 differential diagnoses for acute chest pain in a 55-year-old male smoker" instead of "What causes chest pain?" |
| **2. Provide context** | Give relevant background information | "The patient has a history of DVT and recent long-haul flight" |
| **3. Define the format** | Tell the AI how to structure the output | "Present as a table with columns: diagnosis, likelihood, key distinguishing feature" |
| **4. Assign a role** | Tell the AI to act as a specific expert | "Act as an emergency medicine physician" |
| **5. Set constraints** | Specify what to include or exclude | "Use only evidence from guidelines published after 2020" |

**Bad prompt vs. good prompt:**

| Bad prompt | Good prompt |
|-----------|------------|
| "Tell me about diabetes treatment" | "Act as an endocrinologist. Summarize the 2024 ADA Standards of Care recommendations for first-line pharmacotherapy in newly diagnosed type 2 diabetes for a patient with BMI 32, eGFR 60, and no cardiovascular disease. Present as a numbered list with drug name, mechanism, and key consideration." |

> **Can you guess:**
>
> - Why does assigning a "role" to the AI change the quality of the response?
> - *(Hint: the role primes the model to draw from the subset of its training data relevant to that expertise)*

---

## Session 2: Lecture — Prompting Techniques (20 mins)

---

## Zero-Shot, Few-Shot, and Chain-of-Thought

**Zero-shot prompting:** Ask the question directly without examples.

> "Classify the following chief complaint as urgent or non-urgent: 'I have had a headache for 3 weeks.'"

**Few-shot prompting:** Provide examples before asking the question.

> "Classify the following chief complaints as urgent or non-urgent:
>
> - 'Crushing chest pain radiating to left arm' → Urgent
> - 'Mild knee pain for 2 months' → Non-urgent
> - 'Sudden vision loss in right eye' → Urgent
>
> Now classify: 'I have had a headache for 3 weeks.'"

**Chain-of-thought (CoT) prompting:** Ask the AI to reason step by step.

> "A 70-year-old patient presents with sudden onset aphasia and right-sided weakness. Think step by step: What is the most likely diagnosis? What are the immediate priorities? What imaging should be ordered first and why?"

**Comparison:**

| Technique | When to use | Strength |
|-----------|------------|----------|
| **Zero-shot** | Simple, well-defined questions | Fast and easy |
| **Few-shot** | Classification or formatting tasks | Teaches the pattern you want |
| **Chain-of-thought** | Complex reasoning or multi-step problems | Reduces errors in logic |

> **Can you guess:**
>
> - For a task like extracting medication names from clinical notes, would zero-shot or few-shot work better?
> - *(Hint: few-shot — showing examples of what to extract and what format to use dramatically improves accuracy)*

---

## Session 3: Lecture — Healthcare-Specific Prompting Strategies (20 mins)

---

## Strategies Tailored to Clinical and Research Use

**Strategy 1: Evidence-level specification**

Instead of asking for general information, specify the level of evidence you need:

> "Summarize only randomized controlled trials published after 2020 that compare GLP-1 receptor agonists with SGLT2 inhibitors for cardiovascular outcomes in type 2 diabetes."

**Strategy 2: Patient-specific contextualization**

Provide patient details to get a tailored response:

> "Given a 45-year-old female with BMI 28, PCOS, and prediabetes (HbA1c 6.3%), what lifestyle and pharmacological interventions does the ADA recommend? Consider her reproductive age."

**Strategy 3: Structured output for clinical documentation**

> "Generate a SOAP note for the following encounter: 28-year-old male, chief complaint of persistent cough for 2 weeks, non-smoker, no fever, clear lung auscultation. Format as: Subjective, Objective, Assessment, Plan."

**Strategy 4: Critical appraisal prompting**

Ask the AI to evaluate rather than just summarize:

> "I will provide the abstract of a clinical trial. Identify potential sources of bias using the Cochrane Risk of Bias tool framework. For each domain, state the risk level (low/some concerns/high) and provide your reasoning."

**Strategy 5: Differential diagnosis with reasoning**

> "A 3-year-old child presents with barking cough worse at night, low-grade fever, and inspiratory stridor. List the top 5 differential diagnoses. For each, explain why it fits or does not fit, and state one test that would help confirm or rule it out."

**Common pitfalls:**

| Pitfall | Consequence | How to avoid |
|---------|------------|-------------|
| Asking for "the best" treatment | AI picks one option without nuance | Ask for "options with pros and cons" |
| Not specifying patient population | Response may be for adults when you need pediatric | Always include age, sex, comorbidities |
| Trusting the first response | First answer may contain errors | Ask the AI to critique its own response |

> **Can you guess:**
>
> - What happens if you ask an AI to "critique its own answer"?
> - *(Hint: self-critique prompting often catches errors that the initial response missed, though it can also introduce new errors)*

---

## Session 4: Hands-on — Designing Prompts for Clinical Scenarios (25 mins)

**Task:** Design, test, and compare prompts for three clinical scenarios.

**Scenario 1: Medication safety**

1. Write a zero-shot prompt asking about drug interactions for a specific patient case:
   - Patient: 72-year-old male on warfarin, newly prescribed fluconazole for oral candidiasis
   - Ask about the interaction risk and management
2. Now rewrite as a chain-of-thought prompt: "Think step by step about the pharmacological mechanism of the interaction, the clinical risk, and the recommended management."
3. Compare the two responses — which is more clinically useful?

**Scenario 2: Patient education**

1. Write a prompt to generate patient education material about a new diagnosis:
   - Disease: newly diagnosed heart failure with reduced ejection fraction (HFrEF)
   - Target audience: patient with high school education level
   - Language: plain language, avoid medical jargon
   - Format: one-page handout with sections
2. Evaluate: Is the content accurate? Is it truly written at the appropriate literacy level?

**Scenario 3: Research question**

1. Write a few-shot prompt to help formulate a PICO research question:
   - Provide 2 examples of well-formulated PICO questions
   - Then ask the AI to formulate a PICO question from a rough research idea of your choice
2. Evaluate: Does the AI-generated PICO follow the structure correctly?

**Class sharing:** Each group presents their best prompt and explains why it worked well. Discuss what made some prompts more effective than others.

---

## Take-home Message

1. **Prompt quality determines output quality** — specific, contextualized prompts with role assignment and format specification dramatically improve AI responses
2. **Choose the right technique** — zero-shot for simple tasks, few-shot for classification and formatting, chain-of-thought for complex reasoning
3. **Healthcare prompting requires clinical specificity** — always include patient context, evidence requirements, and output format to get clinically useful responses
