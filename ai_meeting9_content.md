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

### 2.1 Clinical Deployment Scenario

Frame your proposed AI application using PICO. Throughout this course, PICO has been used to frame how AI tools are evaluated for clinical deployment — for example, IDx-DR (Meeting 05: P=adults at risk for diabetic retinopathy, I=autonomous AI screening, C=ophthalmologist referral, O=detection rate) and the Dembrower mammography study (Meeting 06: P=women in screening, I=AI + one radiologist, C=double reading by two radiologists, O=cancer detection rate). Your PICO defines the deployment context and determines what kind of AI tool you need.

- **P** (Population) — What is the target patient population in your setting?
- **I** (Intervention) — What would the AI tool do in practice?
- **C** (Comparison) — What is the current standard of care it would replace or augment?
- **O** (Outcome) — What clinical outcome should improve?

This framing directly feeds into AI tool selection (does the tool match this PICO?) and evaluation (Meeting 07 DECIDE framework — does the tool's training data match your P? Was it compared against your C?).

Examples:
- P: Heart failure patients discharged from a teaching hospital. I: LLM generates structured discharge summaries from clinical notes. C: Physicians manually write discharge summaries. O: Completeness and timeliness of discharge documentation.
- P: Adults at risk for diabetic retinopathy in primary care clinics without ophthalmologists. I: AI screening tool analyzes retinal fundus photos. C: Referral to ophthalmologist for screening. O: Screening rate and detection sensitivity.
- P: Researchers conducting a systematic review on a clinical topic. I: AI-assisted literature search and screening. C: Manual PubMed search and two-reviewer screening. O: Time to complete screening with equivalent recall.
- P: Patients sending messages through a hospital portal. I: AI chatbot triages messages by urgency. C: Nurse telephone triage. O: Response time and triage accuracy.

### 2.2 AI Tool Selection

Describe the AI tool or approach you plan to use:

- **Tool name or type:** Specify the tool (e.g., ChatGPT, Claude, a specific FDA-authorized device) or the general approach (e.g., LLM-based summarization, computer vision classification). See Meeting 01 for the AI tool landscape and Meeting 05 for available clinical decision support tools.
- **AI type:** Is this a discriminative AI (classifies or predicts) or generative AI (produces text, images, or other content)? See Meeting 07 for the distinction.
- **Justification:** Why is this tool appropriate for the stated problem? What are its strengths and limitations for this use case? See Meeting 02 for LLM capabilities and limitations.

### 2.3 Prompting Strategy (for generative AI)

If your selected tool is a generative AI (LLM), describe how you will prompt it. Apply the principles and techniques from Meeting 03:

- **Prompt design:** Which of the five principles will you apply? (Be specific, provide context, define format, assign role, set constraints)
- **Prompting technique:** Will you use zero-shot, one-shot, few-shot, or chain-of-thought? Why is this technique appropriate for your task?
- **Example prompt:** Write out the actual prompt you plan to use, showing how you applied the principles above

If your selected tool is a discriminative AI (e.g., an FDA-authorized device), this section is not applicable — state so and proceed to 2.4.

### 2.4 Evaluation Plan

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

### 2.5 Literature Evidence

Provide evidence from existing literature that supports your proposed AI application:

- **At least two references** — peer-reviewed studies, systematic reviews, or authoritative guidelines that demonstrate the feasibility or effectiveness of the proposed approach
- **For each reference:** State the key finding and how it supports your proposal
- **Evidence gap:** If direct evidence for your specific application is lacking, explain what related evidence exists and why it is reasonable to extrapolate

### 2.6 Limitations and Risks

Identify at least two limitations or risks of your proposed AI application:

- **Hallucination risk** (for generative AI): Could the tool fabricate facts, invent citations, or produce incorrect clinical information?
- **Bias risk:** Could the tool perform differently for different patient populations? What demographic groups might be underserved?
- **Regulatory gaps:** Is the tool authorized for clinical use? If not, what regulatory pathway would it require?
- **Reliability and reproducibility:** Does the tool give consistent answers when asked the same question multiple times?
- **Scope limitations:** What can the tool NOT do? What are the boundaries of its applicability?

### 2.7 Ethical Implications

Address the following:

- **Privacy:** Does the AI application require patient data? How will data be protected?
- **Consent:** Should patients be informed that AI is being used in their care? Under what circumstances?
- **Fairness:** Who could be harmed if the AI fails or performs poorly? Are vulnerable populations at greater risk?
- **Accountability:** If the AI makes an error that harms a patient, who is responsible — the clinician, the hospital, or the AI developer?
- **Transparency:** Can the AI explain its reasoning? Should it be required to?

### 2.8 Implementation Considerations

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
| **A** | Includes all B criteria, and additionally addresses ethical implications using the responsible AI principles from Meeting 08 (privacy, consent, fairness, accountability, transparency) and considers the appropriate human-AI interaction mode from Meeting 05 for implementation. |

> **Note:** A grade of C requires a complete, internally consistent proposal. A grade of B additionally requires evidence of critical thinking about evidence and risks. A grade of A further requires ethical awareness and consideration of how the tool fits into clinical workflow.

[Back to Table of Contents](#table-of-contents)

---

## 4. Example Study Plan Outline

The following is a brief worked example. Each section contains 1-2 sentences of placeholder content to illustrate the expected level of specificity.

---

**Clinical Deployment Scenario:** Heart failure patients receive discharge summaries that are often incomplete or delayed, leading to miscommunication with primary care providers.

- P (Population): Heart failure patients discharged from a teaching hospital
- I (Intervention): LLM generates structured discharge summaries from clinical notes
- C (Comparison): Physicians manually write discharge summaries
- O (Outcome): Completeness and timeliness of discharge documentation

This PICO tells us: we need a generative AI tool that can process clinical notes and produce structured text. The tool must have been validated on similar clinical documentation tasks (DECIDE — Data). It will be compared against physician-written summaries (DECIDE — Comparison).

---

**AI Tool Selection:** Claude (Anthropic) — a general-purpose LLM accessed via web interface. Generative AI type (Meeting 07). Selected because it can process long clinical text inputs and generate structured outputs. Key limitation: as a general-purpose LLM, it may hallucinate clinical details not present in the source notes (Meeting 02).

---

**Prompting Strategy:** Generative AI — applicable. Using the five principles from Meeting 03: (1) Be specific — specify the patient's diagnoses, medications, and hospital course; (2) Provide context — include all relevant clinical details from the encounter; (3) Define format — request SOAP-style structured output with sections for diagnosis, hospital course, medications at discharge, follow-up plan, and pending results; (4) Assign role — "Act as a hospitalist writing a discharge summary"; (5) Set constraints — "Use only the information provided; do not add information not in the clinical notes." Prompting technique: one-shot — provide one example of a well-structured discharge summary, then ask the LLM to generate one from the patient's clinical data.

Example prompt: "Act as a hospitalist writing a discharge summary. Using only the clinical information below, generate a structured discharge summary with the following sections: Primary Diagnosis, Hospital Course, Medications at Discharge, Follow-up Plan, Pending Results. Here is an example of the expected format: [example]. Now generate a discharge summary for this patient: [patient clinical data]."

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
| Clinical Deployment Scenario (2.1) | Meeting 05: Case studies (IDx-DR, Viz.ai PICO framing) + Meeting 06: Dembrower study PICO framing + Meeting 07: DECIDE (Data, Comparison) | PICO to define deployment context; determines AI tool requirements and evaluation criteria |
| AI Tool Selection (2.2) | Meeting 01: AI revolution + Meeting 02: How LLMs work + Meeting 05: Clinical decision support + Meeting 07: Evaluating AI | AI tool landscape, LLM capabilities and limitations, available CDS tools, discriminative vs generative AI |
| Prompting Strategy (2.3) | Meeting 03: Prompt engineering | Five principles, zero/one/few-shot, chain-of-thought, healthcare-specific strategies |
| Evaluation Plan (2.4, generative) | Meeting 07: Evaluating AI (Session 4) | 4-step evaluation: accuracy, citation verification, demographic bias test, completeness |
| Evaluation Plan (2.4, discriminative) | Meeting 07: Evaluating AI (Sessions 1-3) | DECIDE framework, reliability assessment, performance metrics |
| Literature Evidence (2.5) | Meeting 04: AI for literature review | AI-powered search tools, evaluating AI-generated summaries |
| Limitations and Risks (2.6) | Meeting 02: Hallucination + Meeting 07: Bias | Types of hallucination, sources of bias, documented bias examples |
| Ethical Implications (2.7) | Meeting 08: AI ethics, regulation, and governance | Privacy regulations, responsible AI principles, accountability, model cards |
| Implementation Considerations (2.8) | Meeting 05: Clinical decision support + Meeting 06: Medical imaging | Workflow integration, human-AI interaction framework, deployment considerations |

[Back to Table of Contents](#table-of-contents)
