# Study Plan: AI Application Proposal

**Herdiantri Sufriyana**
Graduate Institute of Artificial Intelligence and Big Data in Healthcare
National Taiwan University of Nursing and Health Sciences

---

## Table of Contents

1. [Overview](#1-overview)
2. [Study Plan Requirements](#2-study-plan-requirements)
3. [Grading Rubric](#3-grading-rubric)
4. [Example Study Plan Outline](#4-example-study-plan-outline)
5. [Submission Instructions](#5-submission-instructions)
6. [Recap](#6-recap)

---

## 1. Overview

The study plan is worth **25% of the final grade** and is part of the capstone project. It is a written document where you propose an AI application to address a specific healthcare problem. You will identify the problem, select an appropriate AI tool or approach, design an evaluation plan, review supporting evidence, and consider limitations, ethics, and implementation.

**Purpose:** The study plan demonstrates your ability to integrate the foundational knowledge from Meetings 01-08 into a coherent AI application proposal. It tests whether you can translate a healthcare problem into a structured plan for applying and evaluating an AI tool.

**Connection to the capstone (Meeting 15):** The study plan is the design component of your capstone project. Your capstone report will include the study plan plus the results of actually carrying out the AI application. In Meetings 10-14, you will learn about generative AI, AI agents, precision medicine, AI strategy, and emerging trends — these may further inform or refine your proposal. A well-constructed study plan makes the capstone straightforward; a poorly defined plan leads to confusion during execution.

**Submit early, revise to reach A:** The study plan can be submitted any time up to the capstone due date (Meeting 15). You are encouraged to submit as early as possible — the instructor will provide feedback and you can revise and resubmit until the due date. Earlier submission gives you more revision cycles to improve your grade.

[Back to Table of Contents](#table-of-contents)

---

## 2. Study Plan Requirements

Your study plan must include all of the following sections. Each section should be specific enough that another person could understand and replicate your proposed approach.

### 2.1 Healthcare Problem

State a healthcare problem that an AI tool could help address. Frame the problem using the following structure:

- **P** (Population) — Which patients, clinicians, or healthcare stakeholders?
- **P** (Problem) — What specific problem or unmet need exists?
- **A** (AI approach) — What type of AI tool or method could address it?
- **O** (Outcome) — What improvement or result do you expect?

The problem should be grounded in real clinical or healthcare operational challenges. It should not be a hypothetical scenario with no basis in current practice.

Examples of appropriate problems:
- Generating accurate discharge summaries for heart failure patients using an LLM
- Screening diabetic retinopathy images using a discriminative AI tool in primary care
- Summarizing systematic review evidence on a clinical topic using AI-assisted literature search
- Triaging patient messages in a hospital portal using an AI chatbot

### 2.2 AI Tool Selection

Describe the AI tool or approach you plan to use:

- **Tool name or type:** Specify the tool (e.g., ChatGPT, Claude, a specific FDA-authorized device) or the general approach (e.g., LLM-based summarization, computer vision classification)
- **AI type:** Is this a discriminative AI (classifies or predicts) or generative AI (produces text, images, or other content)? See Meeting 07 for the distinction.
- **Justification:** Why is this tool appropriate for the stated problem? What are its strengths for this use case?
- **Alternatives considered:** What other AI tools or approaches could address this problem? Why did you choose this one over the alternatives?

### 2.3 Evaluation Plan

Describe how you will evaluate whether the AI tool works for your stated problem. The evaluation method should match the AI type.

**For generative AI** (recall Meeting 07, Session 4):

| Step | What to evaluate | How to verify |
|------|-----------------|--------------|
| Accuracy check | Is the clinical content correct? | Cross-reference with authoritative sources (guidelines, formulary, UpToDate) |
| Citation verification | Are the references real? | Search PubMed or Google Scholar for each cited reference |
| Demographic bias test | Does the response change when only demographics change? | Ask the same question with varied patient demographics, compare side by side |
| Completeness and balance | Does it cover all relevant aspects? | Check for pharmacological + non-pharmacological options, risks vs. benefits, uncertainty acknowledgment |

**For discriminative AI** (recall Meeting 07, Sessions 1-3):

Apply the DECIDE framework:

| Letter | Criterion | What to assess |
|--------|-----------|---------------|
| **D** | Data | What data was the AI trained and validated on? Is it representative? |
| **E** | Evidence | Is there peer-reviewed, externally validated evidence? |
| **C** | Comparison | Was it compared to the current standard of care? |
| **I** | Integration | How does it fit into existing clinical workflows? |
| **D** | Disparities | Has performance been assessed across demographic subgroups? |
| **E** | Economics | Does it provide value relative to its cost? |

### 2.4 Literature Evidence

Provide evidence from existing literature that supports your proposed AI application:

- **At least two references** — peer-reviewed studies, systematic reviews, or authoritative guidelines that demonstrate the feasibility or effectiveness of the proposed approach
- **For each reference:** State the key finding and how it supports your proposal
- **Evidence gap:** If direct evidence for your specific application is lacking, explain what related evidence exists and why it is reasonable to extrapolate

### 2.5 Limitations and Risks

Identify at least two limitations or risks of your proposed AI application:

- **Hallucination risk** (for generative AI): Could the tool fabricate facts, invent citations, or produce incorrect clinical information?
- **Bias risk:** Could the tool perform differently for different patient populations? What demographic groups might be underserved?
- **Regulatory gaps:** Is the tool authorized for clinical use? If not, what regulatory pathway would it require?
- **Reliability and reproducibility:** Does the tool give consistent answers when asked the same question multiple times?
- **Scope limitations:** What can the tool NOT do? What are the boundaries of its applicability?

### 2.6 Ethical Implications

Address the following:

- **Privacy:** Does the AI application require patient data? How will data be protected?
- **Consent:** Should patients be informed that AI is being used in their care? Under what circumstances?
- **Fairness:** Who could be harmed if the AI fails or performs poorly? Are vulnerable populations at greater risk?
- **Accountability:** If the AI makes an error that harms a patient, who is responsible — the clinician, the hospital, or the AI developer?
- **Transparency:** Can the AI explain its reasoning? Should it be required to?

### 2.7 Implementation Considerations

Describe how the AI application would be deployed in practice:

- **Who** uses the tool? (clinicians, nurses, patients, administrators)
- **When** in the clinical workflow is it used? (triage, diagnosis, treatment planning, documentation, discharge)
- **How** is the output delivered? (EHR integration, standalone app, web interface, printed report)
- **What training** would users need? (brief orientation, certification, ongoing education)
- **What happens** when the AI is wrong? (human override, escalation protocol, feedback mechanism)

[Back to Table of Contents](#table-of-contents)

---

## 3. Grading Rubric

The study plan is graded on a five-level rubric (A through E). Each higher grade builds on all criteria of the grade below it.

| Grade | Criteria |
|-------|----------|
| **E** | Not submitted, or content is unrelated to the selected healthcare problem or AI application. |
| **D** | Submitted but the healthcare problem is unclear, or the proposed AI application is not feasible or coherent with the stated problem. |
| **C** | Clearly identifies a healthcare problem, proposes an appropriate AI tool or approach, and outlines a basic evaluation plan including expected outcomes and data requirements. |
| **B** | Includes all C criteria, and additionally provides evidence from literature supporting the proposed approach and discusses potential limitations and risks of the AI application. |
| **A** | Includes all B criteria, and additionally demonstrates strategic depth by comparing multiple AI approaches, considering implementation barriers, and addressing ethical implications including bias and privacy. |

> **Note:** A grade of C requires a complete, internally consistent proposal. A grade of B additionally requires evidence of critical thinking about evidence and risks. A grade of A further requires strategic depth and ethical awareness.

[Back to Table of Contents](#table-of-contents)

---

## 4. Example Study Plan Outline

The following is a brief worked example. Each section contains 1-2 sentences of placeholder content to illustrate the expected level of specificity.

---

**Healthcare Problem:** Heart failure patients receive discharge summaries that are often incomplete or delayed, leading to miscommunication with primary care providers. Can an LLM generate accurate, structured discharge summaries from clinical notes to reduce documentation burden and improve care transitions?

- P (Population): Hospitalized heart failure patients and their discharge care teams
- P (Problem): Discharge summaries are frequently incomplete, delayed, or missing key information
- A (AI approach): LLM-based text generation from structured clinical data and notes
- O (Outcome): Discharge summaries that are clinically accurate, complete, and produced faster than manual documentation

---

**AI Tool Selection:** Claude (Anthropic) — a general-purpose LLM accessed via web interface. Generative AI type. Selected because it can process long clinical text inputs and generate structured outputs. Alternative considered: GPT-4 (OpenAI) — similar capability, but Claude was chosen for its longer context window and safety-oriented design. Also considered: DAX Copilot (Nuance/Microsoft) — a specialized documentation AI, but it requires EHR integration not available in this evaluation.

---

**Evaluation Plan:** Generative AI evaluation (4-step method from Meeting 07):
1. Accuracy: Compare AI-generated summary against the physician-written summary for 5 sample cases, checking medications, diagnoses, follow-up instructions
2. Citation verification: Not applicable (discharge summaries do not cite literature)
3. Demographic bias: Generate summaries for patients of different demographics (age, sex) with equivalent clinical scenarios, compare completeness and tone
4. Completeness: Check whether AI-generated summaries include all required elements (diagnosis, hospital course, medications at discharge, follow-up plan, pending results)

---

**Literature Evidence:**
1. Patel & Lam (2024), JAMIA: LLMs generated discharge summaries with 89% clinical accuracy compared to physician-written summaries, with significant time savings. Supports the feasibility of LLM-based discharge documentation.
2. WHO (2021), Ethics and Governance of AI for Health: Provides framework for responsible deployment of AI in clinical documentation, supporting the ethical evaluation component of this proposal.

---

**Limitations and Risks:** Hallucination risk — the LLM may fabricate medication names or dosages not present in the source notes. Bias risk — discharge summaries for patients with limited English proficiency may receive less detailed AI-generated content if the source notes are sparse. Reliability — LLM outputs may vary across runs; the same input may produce different summaries.

---

**Ethical Implications:** Patient data must be de-identified before input to the LLM (no real patient data should be entered into a commercial LLM without institutional approval). Patients should be informed if AI is used in their documentation. If an AI-generated summary contains an error that leads to a medication mistake, the discharging physician remains responsible. The LLM cannot explain why it included or omitted specific information.

---

**Implementation Considerations:** Used by discharging physicians or nurse practitioners. Applied at the point of discharge, after all clinical decisions are made. Output delivered as a draft summary for physician review and editing (not autonomous — physician signs the final version). Users would need a 30-minute orientation on prompt formatting and verification procedures. When the AI produces an inaccurate summary, the physician edits it directly; persistent errors are reported to the implementation team for prompt refinement.

---

> **Note:** This example is intentionally brief. Your actual study plan should expand each section with more detail, particularly the evaluation plan and limitations.

[Back to Table of Contents](#table-of-contents)

---

## 5. Submission Instructions

- **Format:** Submit as PDF or DOCX
- **Length:** No strict page limit, but a well-structured plan typically requires 3-5 pages
- **Platform:** Submit via iCLASS
- **Due date:** Same as the capstone (Meeting 15, Week 15). However, submit as early as possible to receive feedback and revise.
- **File naming:** Use the format `StudentID_StudyPlan.pdf` or `StudentID_StudyPlan.docx`

> **Note:** Start your study plan early. The instructor will provide feedback on each submission, and you can revise and resubmit until the due date. More revision cycles = more opportunities to reach grade A. The healthcare problem and AI tool selection require careful thought. Use the example in Section 4 as a structural template, but choose your own healthcare problem and AI approach.

[Back to Table of Contents](#table-of-contents)

---

## 6. Recap

The following table maps each section of the study plan to the meeting(s) whose content it draws from. Use this to review relevant material as you prepare your plan.

| Study Plan Section | Relevant Meeting(s) | Key Content |
|--------------------|----------------------|-------------|
| Healthcare Problem | Meeting 01: The AI revolution in healthcare | What AI can and cannot do, healthcare AI use cases |
| AI Tool Selection | Meeting 02: How LLMs work + Meeting 05: Clinical decision support | LLM capabilities and limitations, discriminative vs generative AI, available CDS tools |
| Evaluation Plan (generative) | Meeting 07: Evaluating AI (Session 4) | 4-step evaluation: accuracy, citation verification, demographic bias test, completeness |
| Evaluation Plan (discriminative) | Meeting 07: Evaluating AI (Sessions 1-3) | DECIDE framework, reliability assessment, performance metrics |
| Literature Evidence | Meeting 04: AI for literature review | AI-powered search tools, evaluating AI-generated summaries |
| Limitations and Risks | Meeting 02: Hallucination + Meeting 07: Bias | Types of hallucination, sources of bias, documented bias examples |
| Ethical Implications | Meeting 08: AI ethics, regulation, and governance | Privacy regulations, responsible AI, accountability |
| Implementation Considerations | Meeting 05: Clinical decision support + Meeting 06: Medical imaging | Workflow integration, alert fatigue, deployment considerations |

[Back to Table of Contents](#table-of-contents)
