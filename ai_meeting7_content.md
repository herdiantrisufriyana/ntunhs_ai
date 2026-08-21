# Evaluating AI — Accuracy, Bias, and Hallucination

**Herdiantri Sufriyana**
Graduate Institute of Artificial Intelligence and Big Data in Healthcare
National Taiwan University of Nursing and Health Sciences

---

## Subtopics

- How to assess AI tool reliability
- Bias in training data and model outputs
- Framework for evaluating AI claims in healthcare
- Hands-on: Evaluating outputs from different AI tools

---

## Session 1: Lecture — Assessing AI Tool Reliability (25 mins)

---

## Why Evaluation Matters

Every AI tool makes claims about its performance. As healthcare professionals, you must be able to critically evaluate these claims — just as you evaluate the evidence behind a new drug or diagnostic test.

**The credibility spectrum:**

| Evidence level | Source | Trustworthiness |
|---------------|--------|----------------|
| **Peer-reviewed validation study** | Independent researchers test the tool on external data | Highest |
| **Regulatory submission data** | Data submitted to FDA/TFDA for clearance | High (but selected by manufacturer) |
| **Preprint** | Not yet peer-reviewed | Moderate — results may change after review |
| **Company white paper** | Published by the tool's developer | Low — selection bias, no independent verification |
| **Marketing claims** | Website or press release | Lowest — often cherry-picked metrics |

---

## Key Questions to Ask About Any AI Tool

| Question | Why it matters | Red flag |
|----------|---------------|----------|
| **What data was it trained on?** | Training data determines what the AI knows | "Proprietary data" with no description of demographics or sources |
| **Was it validated externally?** | Internal validation overestimates performance | Only tested on data from the same institution that built it |
| **What population was studied?** | Performance varies across demographics | Tested only on one age group, ethnicity, or healthcare setting |
| **What metrics are reported?** | Some metrics are misleading | Reporting only accuracy without sensitivity/specificity |
| **What is the comparison?** | AI must be compared to the current standard of care | Compared to no intervention rather than to standard practice |
| **What is the intended use?** | Performance is valid only for the stated use case | Tool marketed for uses beyond its validation scope |

---

## Common Ways AI Performance Is Overstated

| Tactic | How it misleads | Example |
|--------|----------------|---------|
| **Reporting only accuracy** | Hides poor sensitivity or specificity | "99% accuracy" on a dataset where 99% are normal — model just predicts "normal" for everyone |
| **Internal validation only** | Overestimates real-world performance | AUC 0.95 on development data, 0.72 on external data |
| **Selective population** | Results do not generalize | AI tested on adults 30-50 marketed for all ages |
| **No confidence intervals** | Point estimates hide uncertainty | "Sensitivity 92%" — could be 85-99% with wide confidence interval |
| **Comparing to untrained humans** | AI vs. medical students is not AI vs. specialists | "AI outperforms doctors" — but tested against residents, not attendings |

> **Can you guess:**
>
> - A company claims their AI achieves "physician-level performance" on chest X-ray reading. What questions should you ask?
> - *(Hint: which physicians? Reading what types of images? On which patient population? With what prevalence of disease? Compared to single or double reading?)*

---

## Session 2: Lecture — Bias in AI (25 mins)

---

## What is AI Bias?

**AI bias** occurs when a system produces systematically unfair or inaccurate results for certain groups of people.

**Sources of bias:**

| Source | How it enters | Healthcare example |
|--------|-------------|-------------------|
| **Training data** | Underrepresentation of certain groups | Dermatology AI trained mostly on light skin |
| **Label bias** | Ground truth labels reflect existing disparities | Chest X-ray labels based on radiologist reports that underdiagnose women |
| **Selection bias** | Training data not representative of deployment population | Model trained on academic medical center data, deployed in community clinics |
| **Measurement bias** | Differences in how data is collected across groups | Pulse oximetry less accurate for darker skin tones — AI trained on these measurements inherits the error |
| **Historical bias** | Past clinical practices encoded into data | Pain assessment disparities by race reflected in clinical notes |

---

## Documented Examples of AI Bias in Healthcare

| Study | Finding | Impact |
|-------|---------|--------|
| **Obermeyer et al. (2019), Science** | A widely used algorithm for predicting healthcare needs was less likely to refer Black patients for extra care — at a given risk score, Black patients were sicker than White patients | Affected an estimated 200 million patients per year in the US |
| **Adamson & Smith (2018), JAMA Dermatology** | Most dermatology AI training datasets had <5% images of dark skin | AI less accurate for skin cancer detection in people of color |
| **Larrazabal et al. (2020), PNAS** | Chest X-ray AI models showed performance disparities across sex, age, and race when trained on imbalanced datasets | Underdiagnosis of certain conditions in underrepresented groups |
| **Sjoding et al. (2020), NEJM** | Pulse oximeters overestimate oxygen saturation in Black patients | AI using SpO2 data inherits and may amplify this measurement bias |

**Bias mitigation strategies:**

| Strategy | What it involves |
|----------|-----------------|
| **Diverse training data** | Ensure representation across demographics |
| **Subgroup analysis** | Report performance separately for each group |
| **Fairness metrics** | Equalized odds, demographic parity, calibration across groups |
| **Ongoing monitoring** | Track performance disparities after deployment |
| **Inclusive development teams** | Diverse perspectives catch biases earlier |

> **Can you guess:**
>
> - If an AI tool reports "overall AUC 0.92" but does not break down performance by sex or ethnicity, should you be concerned?
> - *(Hint: yes — a high overall AUC can mask large disparities between subgroups)*

---

## Session 3: Lecture — A Framework for Evaluating AI Claims (15 mins)

---

## The DECIDE Framework for Healthcare AI Evaluation

Use this checklist when evaluating any AI tool for clinical use:

| Letter | Criterion | Key question |
|--------|-----------|-------------|
| **D** | **Data** | What data was the AI trained and validated on? Is it representative? |
| **E** | **Evidence** | Is there peer-reviewed, externally validated evidence of performance? |
| **C** | **Comparison** | Was the AI compared to the current standard of care (not just "no AI")? |
| **I** | **Integration** | How does the AI fit into existing clinical workflows? |
| **D** | **Disparities** | Has performance been assessed across demographic subgroups? |
| **E** | **Economics** | Does the AI provide value relative to its cost? |

**Applying DECIDE to a marketing claim:**

*Claim: "Our AI detects lung cancer with 97% accuracy on CT scans."*

| Criterion | Assessment |
|-----------|-----------|
| **Data** | What CT scanners? What patient population? How many cases? |
| **Evidence** | Published where? Peer-reviewed? External validation? |
| **Comparison** | Compared to what? Radiologist alone? No screening? |
| **Integration** | Does it integrate with existing PACS? How fast is the result? |
| **Disparities** | Performance across age, sex, smoking history, scanner brand? |
| **Economics** | What is the cost per scan? Does it reduce false positives enough to justify the cost? |

> **Can you guess:**
>
> - Using the DECIDE framework, what is the single most common weakness in AI marketing claims?
> - *(Hint: lack of external validation — most claims are based on internal testing only)*

---

## Session 4: Hands-on — Evaluating Outputs from Different AI Tools (25 mins)

**Task:** Test the same clinical question across three AI tools and systematically compare their reliability.

**Clinical question:** "What are the current first-line treatment options for major depressive disorder in pregnant women?"

**Part A: Collect responses (10 mins)**

1. Ask the question to three different AI tools (e.g., ChatGPT, Claude, Gemini)
2. Use this prompt for all three:
   "What are the current evidence-based first-line treatment options for major depressive disorder in a pregnant woman in her second trimester? Include both pharmacological and non-pharmacological options. Cite specific guidelines or systematic reviews."
3. Save or copy each response

**Part B: Evaluate each response (10 mins)**

Use this evaluation table for each tool:

| Criterion | Tool A | Tool B | Tool C |
|-----------|--------|--------|--------|
| Are treatment options clinically accurate? | | | |
| Does it mention both pharmacological and non-pharmacological options? | | | |
| Does it address trimester-specific considerations? | | | |
| Does it cite real guidelines? (Verify 1-2) | | | |
| Does it discuss risks vs. benefits of treatment? | | | |
| Does it mention risks of untreated depression? | | | |
| Does it acknowledge uncertainty? | | | |
| Would you trust this response to guide clinical practice? | | | |

**Part C: Discussion (5 mins)**

4. Compare your evaluations across the class:
   - Did any tool hallucinate a guideline or treatment?
   - Which tool provided the most balanced response?
   - Did any tool miss the critical point that untreated depression also carries fetal risk?
   - How would bias in training data affect the response (e.g., US-centric guidelines vs. global practice)?

---

## Take-home Message

1. **Critically evaluate every AI tool claim** — ask for external validation, subgroup analysis, and comparison to standard of care; use the DECIDE framework
2. **AI bias is real and measurable** — training data gaps produce systematic performance disparities across demographics, and these have been documented in healthcare
3. **Side-by-side comparison is powerful** — testing the same question across multiple AI tools reveals inconsistencies, hallucinations, and gaps that a single-tool evaluation would miss
