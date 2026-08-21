# How Large Language Models Work

**Herdiantri Sufriyana**
Graduate Institute of Artificial Intelligence and Big Data in Healthcare
National Taiwan University of Nursing and Health Sciences

---

## Subtopics

- From neural networks to transformers
- Capabilities and limitations of LLMs
- Hallucination and reliability
- Hands-on: First interaction with an LLM for a healthcare task

---

## Session 1: Lecture — From Neural Networks to Transformers (25 mins)

---

## The Building Blocks of AI

**Neural networks** are inspired by the brain — layers of connected nodes that learn patterns from data.

| Generation | Architecture | What it does well | Healthcare example |
|-----------|-------------|------------------|-------------------|
| **Traditional ML** | Decision trees, logistic regression | Structured data prediction | Predicting hospital readmission from lab values |
| **Deep learning** | Convolutional neural networks (CNNs) | Image recognition | Detecting diabetic retinopathy from fundus photos |
| **Sequence models** | Recurrent neural networks (RNNs) | Sequential data | Predicting next vital sign from ICU monitoring |
| **Transformers** | Self-attention mechanism | Language understanding and generation | ChatGPT, Claude, Gemini |

---

## What Makes Transformers Special?

**The key innovation: attention**

Before transformers, language models processed words one by one in sequence (left to right). Transformers process all words simultaneously and learn which words are most important to each other.

**Analogy:** Imagine reading a patient's chart. A sequential reader reads line by line. An attention-based reader can instantly connect "penicillin allergy" on page 1 with "amoxicillin prescribed" on page 5 — recognizing the relationship regardless of distance.

**How an LLM is built:**

| Step | What happens | Scale |
|------|-------------|-------|
| **1. Pre-training** | Model reads vast amounts of text and learns to predict the next word | Trillions of words from books, websites, papers |
| **2. Fine-tuning** | Model is trained on curated examples of helpful, harmless responses | Thousands of expert-labeled examples |
| **3. RLHF** | Human feedback teaches the model to prefer better answers | Reinforcement learning from human feedback |

**Important:** The model does not "know" facts — it has learned statistical patterns of how words follow each other. This is why it can generate fluent text about topics it has never "understood."

> **Can you guess:**
>
> - If an LLM was trained mostly on English medical textbooks, how well would it perform on Traditional Chinese medical records?
> - *(Hint: performance depends on representation in training data — languages and domains with less data get worse results)*

---

## Model Sizes and What They Mean

| Model | Parameters | Approximate analogy |
|-------|-----------|-------------------|
| GPT-2 (2019) | 1.5 billion | A well-read undergraduate |
| GPT-3 (2020) | 175 billion | — |
| GPT-4 (2023) | Estimated >1 trillion | — |
| Claude Opus 4 (2025) | Undisclosed | — |
| Llama 3 (2024, open) | 8-405 billion | Openly available for research |

**More parameters do not always mean better performance.** A smaller model fine-tuned on medical data can outperform a larger general-purpose model on clinical tasks.

---

## Session 2: Lecture — Capabilities and Limitations (20 mins)

---

## What LLMs Can Do

| Capability | Description | Clinical relevance |
|-----------|------------|-------------------|
| **Summarization** | Condense long documents | Summarize a 30-page guideline into key recommendations |
| **Question answering** | Respond to natural language queries | "What are the contraindications for metformin?" |
| **Translation** | Across languages and registers | Translate patient education from English to Mandarin |
| **Text generation** | Draft documents from prompts | Generate a first draft of a case report |
| **Reasoning** | Multi-step logical inference | Walk through a differential diagnosis step by step |
| **Information extraction** | Pull structured data from text | Extract medication names and doses from clinical notes |

---

## What LLMs Cannot Do

| Limitation | Explanation | Why it matters clinically |
|-----------|------------|-------------------------|
| **No real-time knowledge** | Training data has a cutoff date | Cannot know about a drug approved last month |
| **No database access** | Cannot query PubMed or hospital EHR directly (unless connected) | Answers are from memory, not live data |
| **No mathematical reasoning** | Calculates by pattern matching, not computation | May miscalculate drug doses or unit conversions |
| **No persistent memory** | Each conversation starts fresh (unless given context) | Forgets prior patient discussions |
| **No source verification** | Cannot check if a cited paper actually exists | May fabricate references with real-sounding titles |

> **Can you guess:**
>
> - If you ask an LLM to calculate BMI for a patient who is 170 cm and 80 kg, will it always get the right answer?
> - *(Hint: LLMs often get simple arithmetic right by pattern, but fail on unusual values or multi-step calculations)*

---

## Session 3: Lecture — Hallucination and Reliability (20 mins)

---

## What is Hallucination?

**Hallucination** occurs when an AI model generates information that sounds plausible but is factually incorrect or fabricated.

**Types of hallucination:**

| Type | Example |
|------|---------|
| **Fabricated facts** | "A 2023 study by Smith et al. in The Lancet showed..." — the paper does not exist |
| **Incorrect reasoning** | Correctly states premises but draws a wrong conclusion |
| **Confident errors** | States an incorrect drug dose with complete confidence |
| **Invented citations** | Creates realistic-looking references with real journal names and plausible authors |

**Why hallucination happens:**
- LLMs generate the most *likely* next word, not the most *true* next word
- The model has no mechanism to verify facts against a database
- Rare or specialized topics have less training data, increasing error rates

**Healthcare-specific risks:**

| Risk | Scenario |
|------|---------|
| **Drug interactions** | AI suggests a drug combination that is actually contraindicated |
| **Dosing errors** | AI recommends a pediatric dose for an adult, or vice versa |
| **Outdated guidelines** | AI cites a guideline that has been superseded |
| **Fabricated evidence** | AI invents a clinical trial to support its recommendation |

**How to reduce hallucination risk:**

1. **Always verify** — Cross-check AI outputs against authoritative sources
2. **Ask for sources** — Request specific citations, then verify they exist
3. **Use retrieval-augmented generation (RAG)** — Tools that search a database first, then generate answers based on retrieved documents
4. **Prefer specialized tools** — A medical AI tool with curated data is more reliable than a general-purpose chatbot for clinical questions

> **Can you guess:**
>
> - If an AI tool provides a citation with a DOI link, does that guarantee the paper is real?
> - *(Hint: no — the AI can fabricate DOIs that look valid but lead to error pages)*

---

## Session 4: Hands-on — First LLM Interaction for Healthcare (25 mins)

**Task:** Use an LLM to answer a clinical question and evaluate the response quality.

**Steps:**

1. Open any LLM you have access to (ChatGPT, Claude, Gemini, or Copilot)
2. Ask the following clinical question:
   "A 65-year-old female patient with type 2 diabetes and stage 3 chronic kidney disease asks about the safety of metformin. What is the current evidence and guideline recommendation?"
3. Read the response carefully and evaluate:

| Evaluation criterion | Your assessment |
|---------------------|-----------------|
| Is the response clinically accurate? | Yes / No / Partially |
| Does it cite specific guidelines? | Yes / No |
| Are the cited sources real? (Check one) | Verified / Could not verify / Fabricated |
| Does it mention limitations or contraindications? | Yes / No |
| Does it acknowledge uncertainty? | Yes / No |
| Would you trust this response for patient care? | Yes / With verification / No |

4. Now modify the question — ask the same LLM: "What is the maximum recommended dose of metformin for a patient with eGFR 35 mL/min?"
5. Compare the response to the KDIGO or ADA guidelines. Is the AI correct?
6. Try a second LLM with the same questions. Do you get different answers?

**Class discussion:**
- Which LLM gave more accurate responses?
- Did any LLM hallucinate or provide fabricated citations?
- How would you decide which AI tool to trust for clinical information?

---

## Take-home Message

1. **LLMs are pattern-matching systems, not knowledge databases** — they generate statistically likely text, which is often but not always correct
2. **Hallucination is an inherent limitation** — always verify AI outputs against authoritative sources, especially for drug dosing, guidelines, and citations
3. **Critical evaluation is your responsibility** — AI tools are assistants, not authorities; the clinician remains the final decision-maker
