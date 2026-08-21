# Generative AI in Healthcare

**Herdiantri Sufriyana**
Graduate Institute of Artificial Intelligence and Big Data in Healthcare
National Taiwan University of Nursing and Health Sciences

---

## Subtopics

- AI for medical report generation and patient communication
- AI for drug discovery and molecular design
- Quality control of generative AI outputs
- Case study: Generative AI in clinical and pharmaceutical settings

---

## Session 1: Lecture — Generative AI Fundamentals and Medical Report Generation (25 mins)

---

## What is Generative AI?

**Generative AI** refers to models that create new content — text, images, molecules, or structured data — based on patterns learned from training data.

**Key generative AI model types relevant to healthcare:**

| Model type | What it generates | Healthcare example |
|------------|-------------------|-------------------|
| **Large Language Models (LLMs)** | Text, summaries, translations | Radiology report drafts, patient discharge summaries |
| **Diffusion Models** | Images from text descriptions | Synthetic medical images for training, pathology augmentation |
| **Molecular Generative Models** | Chemical structures | Novel drug candidates, optimized molecular scaffolds |
| **Multimodal Models** | Text + image understanding | Interpreting medical images with textual explanations |

---

## AI for Medical Report Generation

Generative AI can draft clinical documents, reducing documentation burden — the leading cause of physician burnout.

**Current applications:**

| Application | How it works | Status (2026) |
|-------------|-------------|---------------|
| **Radiology report drafting** | LLM generates structured report from imaging findings | Commercially available (Nuance DAX, GPT-4 integrations) |
| **Discharge summary generation** | LLM summarizes hospital course from EHR data | Pilot programs at major medical centers |
| **Patient-facing communication** | LLM translates clinical notes into plain language | MyChart AI summaries in Epic EHR |
| **Clinical letter writing** | LLM drafts referral and insurance letters | Widely adopted in outpatient settings |

**Critical distinction — augmentation vs. replacement:**
- Generative AI **drafts** clinical documents; clinicians **review, edit, and sign**
- The clinician remains legally and ethically responsible for the final content
- Studies show AI-drafted reports reduce documentation time by 30-50% while maintaining quality when reviewed

> **Can you guess:**
>
> - Why is it dangerous to use generative AI for clinical reports without human review?
> - *(Hint: LLMs can "hallucinate" — generating plausible but factually incorrect medical information, including wrong lab values, fabricated findings, or inappropriate recommendations)*

---

## AI for Patient Communication

Generative AI is transforming how healthcare organizations communicate with patients.

**Applications in patient communication:**

1. **Plain-language explanations:** Converting complex medical terminology into understandable language at appropriate literacy levels
2. **Multilingual communication:** Real-time translation of clinical information for patients who speak different languages
3. **After-visit summaries:** Generating personalized summaries of what happened during a clinical visit
4. **Medication instructions:** Creating clear, specific instructions tailored to the patient's regimen

**Quality considerations:**
- Reading level must match patient health literacy (typically 6th-8th grade for general population)
- Cultural sensitivity in language and examples
- Accuracy of medical content must be verified before delivery

> **Can you guess:**
>
> - A patient receives an AI-generated summary saying "your CT scan was normal." The actual report says "no acute findings, but recommend follow-up for incidental lung nodule." What went wrong?
> - *(Hint: the AI simplified away clinically important nuance — generative AI may omit critical details when summarizing)*

---

## Session 2: Lecture — AI for Drug Discovery and Molecular Design (25 mins)

---

## The Drug Discovery Pipeline

Traditional drug discovery takes **10-15 years** and costs **USD 1-2 billion** per approved drug. Generative AI accelerates multiple stages.

**Where generative AI enters the pipeline:**

| Stage | Traditional approach | Generative AI approach | Time savings |
|-------|---------------------|----------------------|--------------|
| **Target identification** | Literature review, expert knowledge | LLM-based literature mining, knowledge graphs | Months to weeks |
| **Hit discovery** | Screening millions of compounds | Generative models design novel candidates | Years to months |
| **Lead optimization** | Iterative chemical modifications | AI-guided molecular optimization | Months to weeks |
| **Clinical trial design** | Manual protocol writing | AI-assisted protocol optimization, patient matching | Weeks to days |

---

## How Molecular Generative Models Work

Molecular generative models learn the "language" of chemistry — just as LLMs learn the language of text.

**Approaches:**

| Method | Representation | How it works |
|--------|---------------|-------------|
| **SMILES-based generation** | Text strings (e.g., CC(=O)Oc1ccccc1C(=O)O for aspirin) | LLM generates valid chemical strings |
| **Graph-based generation** | Molecular graphs (atoms as nodes, bonds as edges) | Graph neural network builds molecules atom by atom |
| **3D structure generation** | 3D coordinates of atoms | Diffusion models generate 3D molecular shapes |
| **Protein structure prediction** | Amino acid sequences | AlphaFold-style models predict protein folding |

**Real-world impact (2024-2026):**
- Insilico Medicine: AI-designed drug INS018_055 entered Phase II clinical trials for idiopathic pulmonary fibrosis — the first entirely AI-designed drug to reach Phase II
- Recursion Pharmaceuticals: Used generative AI to identify drug candidates for rare diseases in months instead of years
- Google DeepMind AlphaFold3: Predicted structures of protein-drug interactions, accelerating target validation

> **Can you guess:**
>
> - Why is generating a valid molecular structure harder than generating a sentence?
> - *(Hint: molecules must satisfy chemical valency rules, stability constraints, and synthesizability — not every plausible-looking structure can actually exist or be made in a lab)*

---

## Session 3: Lecture — Quality Control of Generative AI Outputs (20 mins)

---

## Why Quality Control Matters

Generative AI outputs are **probabilistic, not deterministic** — the same prompt can produce different outputs, and any output may contain errors.

**Types of generative AI errors in healthcare:**

| Error type | Description | Example | Risk level |
|------------|------------|---------|------------|
| **Hallucination** | Generating factually incorrect content that appears plausible | AI cites a medical study that does not exist | High |
| **Omission** | Leaving out critical information | Discharge summary omits drug allergy | High |
| **Bias amplification** | Reflecting or amplifying biases from training data | Treatment recommendations skewed toward one demographic | Medium-High |
| **Outdated information** | Using knowledge from training cutoff date | Recommending a drug that has since been recalled | Medium |
| **Inappropriate confidence** | Presenting uncertain information as definitive | "This patient definitely has condition X" | High |

---

## Quality Control Framework for Healthcare AI Outputs

**A systematic approach to evaluating generative AI outputs:**

1. **Factual verification:** Cross-check all claims, citations, and medical facts against authoritative sources
2. **Completeness check:** Ensure no critical information has been omitted
3. **Bias audit:** Evaluate whether outputs differ systematically across patient demographics
4. **Consistency testing:** Generate multiple outputs for the same input — inconsistency flags unreliability
5. **Expert review:** Clinical domain experts validate appropriateness and safety
6. **Patient safety screening:** Check for contraindications, drug interactions, and harmful advice

**Guardrails for clinical deployment:**
- Confidence thresholds — suppress outputs when model uncertainty is high
- Template constraints — restrict output format to reduce hallucination risk
- Human-in-the-loop — require clinician approval before any AI output reaches patients

> **Can you guess:**
>
> - If an AI generates 10 different discharge summaries for the same patient and 8 agree but 2 differ significantly, what should you do?
> - *(Hint: investigate the 2 outliers — they may reveal edge cases where the AI is uncertain, and the "consensus" of 8 is not necessarily correct either)*

---

## Session 4: Hands-on — Evaluating Generative AI for Clinical Tasks (25 mins)

---

## Activity: Testing and Evaluating AI-Generated Medical Content

**Task:** Use a publicly available LLM to generate clinical content, then systematically evaluate the output quality.

**Steps:**

1. Open ChatGPT, Claude, or Gemini in your browser
2. **Generate a radiology report:** Prompt the AI: "Write a structured radiology report for a chest X-ray showing bilateral pleural effusions in a 65-year-old male with congestive heart failure. Include findings, impressions, and recommendations."
3. **Evaluate the output** using this checklist:
   - Does the report follow standard radiology report structure (clinical history, technique, findings, impression)?
   - Are the findings medically accurate for the described condition?
   - Are the recommendations appropriate and safe?
   - Is there any hallucinated content (findings not supported by the described scenario)?
4. **Test for consistency:** Generate the same report 3 times — compare the outputs. Note any contradictions or significant variations
5. **Test for bias:** Change the patient demographics (age, sex) and regenerate — does the clinical content change inappropriately?
6. **Generate a patient-facing summary:** Ask the AI to explain the same radiology findings to a patient at a 6th-grade reading level. Evaluate whether it is accurate, complete, and understandable
7. **Document your findings:** Which errors or issues did you identify? How would you design a quality control process for this use case?

**Discussion questions:**
- Would you trust this AI-generated report enough to sign it as a radiologist? Why or why not?
- What additional safeguards would you want before this tool is deployed in your hospital?

---

## Session 5: Case Study Discussion — Generative AI in Practice (15 mins)

---

## Case Study: Epic MyChart AI and Google Med-PaLM

**Case A — Epic MyChart AI message drafting (2024-2026):**
- Epic integrated LLM-based message drafting into MyChart patient portal
- Physicians receive AI-drafted responses to patient messages; they review and send
- Early results: 60% of drafted responses accepted with minor or no edits
- Concern: physicians may become over-reliant and rubber-stamp AI responses without careful review

**Case B — Google Med-PaLM 2 (2023-2025):**
- Google developed Med-PaLM 2, an LLM fine-tuned for medical question answering
- On US Medical Licensing Exam questions, scored at expert physician level
- However: performance on real clinical scenarios with ambiguity and incomplete information was notably lower
- Lesson: exam performance does not equal clinical competence

**Discussion:**
- What is the difference between an AI that passes a medical exam and an AI that is safe for clinical use?
- How should hospitals decide which generative AI applications to adopt first?

---

## Take-home Message

1. **Generative AI** can draft medical reports and patient communications, reducing documentation burden — but clinicians must always review and verify outputs before use
2. **Drug discovery** is being accelerated by molecular generative models that design novel compounds, with the first AI-designed drugs now in clinical trials
3. **Quality control** is non-negotiable — hallucination, omission, bias, and inconsistency are common failure modes that require systematic evaluation frameworks
4. **The human-in-the-loop** principle applies to all generative AI in healthcare: AI generates, humans validate and take responsibility
