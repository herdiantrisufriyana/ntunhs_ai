# Capstone Project: AI Application Report

**Herdiantri Sufriyana**
Graduate Institute of Artificial Intelligence and Big Data in Healthcare
National Taiwan University of Nursing and Health Sciences

---

## Table of Contents

1. [Overview](#1-overview)
2. [Report Structure](#2-report-structure)
3. [Presentation Format](#3-presentation-format)
4. [Grading Rubric](#4-grading-rubric)
5. [Connecting Study Plan to Capstone](#5-connecting-study-plan-to-capstone)
6. [Peer Feedback Guidelines](#6-peer-feedback-guidelines)
7. [Submission Instructions](#7-submission-instructions)

---

## 1. Overview

This is the **capstone assessment** for the Innovative Applications of Artificial Intelligence course, worth **45% of the final grade**.

The capstone project extends your study plan from Meeting 09 (Week 9) into a completed AI application evaluation. Over Meetings 10-14, you learned about generative AI, AI agents, precision medicine, AI strategy, and emerging trends — these may have refined your understanding of the AI tool you proposed. The capstone is where you actually use the AI tool, evaluate its outputs, and present your findings.

**What the capstone demonstrates:**

- You can apply an AI tool to a real healthcare problem
- You can systematically evaluate AI outputs using the methods from this course
- You can present findings in a structured format with clinical interpretation
- You can make an evidence-based recommendation about AI adoption

**Relationship to the study plan:** Your capstone report should follow the proposal laid out in your study plan. If you discovered during Meetings 10-14 that parts of your plan needed adjustment (e.g., the tool was not suitable, a different evaluation approach was needed), document what changed and why. Deviations from the study plan are acceptable if justified.

> **Note:** The capstone is both a written report and an oral presentation. You submit the report and present your key findings to the class during Meeting 15.

[Back to Table of Contents](#table-of-contents)

---

## 2. Report Structure

Your written report must contain the following sections.

### 2.1 Introduction

- **Healthcare problem:** State the healthcare problem from your study plan, refined based on what you learned during Meetings 10-14
- **Background:** Briefly describe why this problem matters clinically (1-2 paragraphs). What is the current practice? What gap does AI address?
- **AI approach:** State the AI tool or approach you used and why you selected it (updated from your study plan if applicable)

### 2.2 Methods

- **AI tool description:** Name the tool, version, access method (web interface, API, institutional deployment). State whether it is generative or discriminative AI.
- **Evaluation methodology:** Describe how you evaluated the AI tool's outputs. Reference the evaluation framework from your study plan:
  - For generative AI: the 4-step method (accuracy check, citation verification, demographic bias test, completeness assessment)
  - For discriminative AI: DECIDE framework assessment
- **Test cases:** Describe the clinical scenarios or test cases you used. How many? How were they selected? Were they based on real clinical situations (de-identified) or constructed scenarios?
- **Deviations from study plan:** If your methods changed from the study plan, explain what changed and why.

### 2.3 Results

- **AI tool demonstration:** Show the AI tool in action — include the prompts you used (for generative AI) or the inputs you provided (for discriminative AI), and the outputs you received
- **Evaluation findings:** Present the results of your evaluation:
  - Accuracy: How many claims were correct vs. incorrect? Provide specific examples of errors found.
  - Citation verification: How many cited references were real? Provide examples of invented citations if found.
  - Demographic bias: Did responses differ when demographics were varied? Show side-by-side comparisons.
  - Completeness: What was included vs. missing?
  - For discriminative AI: DECIDE framework scores with justification for each criterion.
- **Summary table:** Present a concise summary of evaluation results:

| Evaluation criterion | Finding | Evidence |
|---------------------|---------|----------|
| Accuracy | e.g., 8/10 clinical claims verified as correct | List the 2 errors found |
| Citation verification | e.g., 3/5 citations were real | List the 2 invented citations |
| Demographic bias | e.g., No clinically significant differences found | Show comparison |
| Completeness | e.g., Missing non-pharmacological options | Describe the gap |

### 2.4 Discussion

- **Interpretation:** What do the evaluation results mean? Is this AI tool suitable for the stated healthcare problem?
- **Comparison with literature:** How do your findings compare with published evaluations of similar AI tools? Do they align with or contradict existing evidence?
- **Limitations encountered:** What limitations did you discover during execution that were not anticipated in the study plan? What surprised you?
- **Adoption recommendation:** Based on your evaluation, would you recommend this AI tool for clinical use? Under what conditions? With what safeguards?
  - If yes: specify the clinical setting, user group, and oversight requirements
  - If no: explain why, and suggest what would need to change for the tool to be suitable

[Back to Table of Contents](#table-of-contents)

---

## 3. Presentation Format

Each student presents their capstone project during Meeting 15.

**Time allocation:**

- **Presentation:** 15-20 minutes per student
- **Q&A:** 5-10 minutes following each presentation

**Presentation structure:**

Present your key findings, not every detail of the report. Focus on the following flow:

1. **Healthcare problem and AI approach** (2-3 minutes) — State the problem, why it matters, and which AI tool you used. The audience should understand the context immediately.
2. **Demonstration** (5-7 minutes) — Show the AI tool in action. Walk through 1-2 example prompts/inputs and outputs. Show evaluation results (accuracy, bias test, or DECIDE assessment).
3. **Key findings** (5-7 minutes) — Present the most important evaluation results. What worked? What failed? Show specific examples of errors, hallucinations, or bias if found.
4. **Recommendation** (3-4 minutes) — Would you recommend this tool? Under what conditions? What safeguards are needed? End with implications for healthcare practice.

**Presentation tips:**

- Use slides (PowerPoint, PDF, or equivalent) with large fonts and clear figures
- Include screenshots of actual AI tool inputs and outputs
- Show side-by-side comparisons for bias testing
- Practice the timing; 15 minutes goes quickly
- Anticipate questions about your evaluation methodology and recommendation

> **Note:** The presentation is not a reading of the report. It is a distilled version that communicates the core message. Think of it as explaining your findings to a hospital administrator who has 20 minutes to decide whether to invest in this AI tool.

[Back to Table of Contents](#table-of-contents)

---

## 4. Grading Rubric

The capstone is graded on a five-level rubric (A through E). Each higher grade builds on all criteria of the grade below it.

| Grade | Criteria |
|-------|----------|
| **E** | Not submitted or not presented, or submission/presentation is unrelated to the proposed AI application or healthcare problem. |
| **D** | Submitted/presented but shows minimal effort or major flaws (e.g., AI tool not actually used, results fabricated, or substantial mismatch with the proposed study plan). |
| **C** | Implements the proposed AI application with real examples, demonstrates its use for the healthcare problem, and presents results in a clear and structured manner. |
| **B** | Includes all C criteria, and additionally evaluates the AI tool's output quality with specific criteria (e.g., accuracy, relevance, completeness) and discusses practical implementation considerations. |
| **A** | Includes all B criteria, and additionally applies the evaluation frameworks from Meeting 07 comprehensively (DECIDE or 4-step method), addresses ethical and regulatory considerations using the responsible AI principles from Meeting 08, determines the appropriate human-AI interaction mode from Meeting 05, and presents a compelling evidence-based adoption recommendation. |

> **Note:** A grade of C requires a technically complete evaluation with real AI outputs. A grade of B additionally requires systematic evaluation using the course frameworks. A grade of A further requires comprehensive application of the course's evaluation, ethical, and deployment frameworks.

[Back to Table of Contents](#table-of-contents)

---

## 5. Connecting Study Plan to Capstone

The following table shows how each section of the study plan (Meeting 09) maps to the capstone report, and which meeting supports the content for each section.

| Study Plan Section (Meeting 09) | Capstone Report Section | Supporting Meeting(s) |
|---------------------------------|-------------------------|----------------------|
| Healthcare Problem (2.1) | Introduction: Problem and background | Meeting 03: PICO; Meeting 04: PICO in literature review |
| AI Tool Selection (2.2) | Introduction: AI approach | Meeting 01: AI landscape; Meeting 02: LLMs; Meeting 05: CDS tools; Meeting 07: discriminative vs generative |
| Prompting Strategy (2.3) | Methods: Prompts used | Meeting 03: Prompt engineering |
| Evaluation Plan (2.4) | Methods: Evaluation methodology | Meeting 07: Evaluating AI (DECIDE + 4-step method) |
| Literature Evidence (2.5) | Discussion: Comparison with literature | Meeting 04: AI for literature review |
| Limitations and Risks (2.6) | Discussion: Limitations encountered | Meeting 02: Hallucination; Meeting 07: Bias |
| Ethical Implications (2.7) | Discussion: Part of adoption recommendation | Meeting 08: AI ethics, regulation, governance |
| Implementation Considerations (2.8) | Discussion: Adoption recommendation | Meeting 05: CDS workflow, human-AI interaction framework |

> **Note:** The study plan is the design; the capstone is the execution. Every section of the study plan has a corresponding section in the capstone report. If a step in your study plan proved infeasible during execution, document the deviation in the Methods section of your report.

[Back to Table of Contents](#table-of-contents)

---

## 6. Peer Feedback Guidelines

During each presentation, the audience provides structured feedback. Focus on the following areas.

**Clarity of the healthcare problem:**

- Is the problem clearly stated and clinically relevant?
- Can you understand why AI is a suitable approach for this problem?
- Is the significance evident?

**Quality of evaluation:**

- Was the AI tool actually used with real inputs and outputs?
- Was the evaluation systematic (not just "it seems good")?
- Were appropriate methods used (4-step method for generative AI, DECIDE for discriminative AI)?
- Was demographic bias tested?

**Quality of demonstration:**

- Did the presenter show actual AI inputs and outputs?
- Were examples specific and illustrative (not generic)?
- Were errors, hallucinations, or bias clearly identified?

**Soundness of recommendation:**

- Does the recommendation follow logically from the evaluation results?
- Are conditions and safeguards specified?
- Does the presenter distinguish between "this tool works in my test" and "this tool is ready for clinical deployment"?
- Are limitations acknowledged honestly?

**How to give feedback:**

- Be specific: "Your bias test showed no difference in recommendations across demographics, which strengthens the adoption case" is more useful than "Good evaluation"
- Be constructive: "The evaluation would be stronger with more test cases" is more useful than "Not enough testing"
- Ask questions when something is unclear; the presenter may have a good reason for a decision that was not explained in the time available

[Back to Table of Contents](#table-of-contents)

---

## 7. Submission Instructions

Submit the following files via iCLASS by the end of Meeting 15 (Week 15).

**Required submissions:**

| File | Format | Description |
|------|--------|-------------|
| Capstone report | PDF or DOCX | The written report containing all sections described in Section 2 |
| AI tool outputs | PDF or screenshots | The actual AI inputs and outputs used in your evaluation (appendix or embedded in report) |

**File naming convention:**

- Report: `StudentID_Capstone.pdf` or `StudentID_Capstone.docx`

**Report formatting:**

- No strict page limit, but a complete report typically requires 5-10 pages including screenshots and tables
- Include all AI tool screenshots and evaluation tables within the report
- Number all figures and tables sequentially (Figure 1, Figure 2, Table 1, etc.)
- Use a readable font size (11-12 pt) and standard margins

**Presentation slides:**

- Slides are used during the oral presentation but do not need to be submitted unless the instructor requests them
- If submitted, use the naming convention: `StudentID_Capstone_Slides.pdf`

> **Note:** The AI tool outputs (screenshots of prompts and responses) are required because they demonstrate that you actually used the tool and allow the instructor to verify your evaluation. Make sure screenshots are legible and include both your input and the AI's output.

[Back to Table of Contents](#table-of-contents)
