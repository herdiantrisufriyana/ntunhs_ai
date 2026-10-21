# Evaluating AI — Accuracy, Bias, and Hallucination

**Herdiantri Sufriyana**
Graduate Institute of Artificial Intelligence and Big Data in Healthcare
National Taiwan University of Nursing and Health Sciences

---

## Subtopics

- Evaluating discriminative AI: reliability, bias, and the DECIDE framework
- Evaluating generative AI: accuracy, hallucination, and demographic bias in LLM outputs
- Hands-on: Applying DECIDE to a discriminative AI claim and testing generative AI outputs

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
| [**Obermeyer et al. (2019), Science**](https://doi.org/10.1126/science.aax2342) | A widely used algorithm for predicting healthcare needs was less likely to refer Black patients for extra care — at a given risk score, Black patients were sicker than White patients | Affected an estimated 200 million patients per year in the US |
| [**Adamson & Smith (2018), JAMA Dermatology**](https://doi.org/10.1001/jamadermatol.2018.1348) | Most dermatology AI training datasets had <5% images of dark skin | AI less accurate for skin cancer detection in people of color |
| [**Larrazabal et al. (2020), PNAS**](https://doi.org/10.1073/pnas.1919012117) | Chest X-ray AI models showed performance disparities across sex, age, and race when trained on imbalanced datasets | Underdiagnosis of certain conditions in underrepresented groups |
| [**Sjoding et al. (2020), NEJM**](https://doi.org/10.1056/NEJMc2029240) | Pulse oximeters overestimate oxygen saturation in Black patients | AI using SpO2 data inherits and may amplify this measurement bias |

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

## Session 4: Lecture — Evaluating Generative AI Outputs (15 mins)

---

## Discriminative vs. Generative AI — Different Evaluation Needs

Sessions 1-3 covered **discriminative AI** — models that classify or predict (e.g., "is this X-ray normal or abnormal?"). These are evaluated with metrics like sensitivity, specificity, and AUC on defined datasets.

**Generative AI** (LLMs like ChatGPT, Claude, Gemini) produces free-text responses. It requires a different evaluation approach because:
- There is no single "correct answer" to compare against
- The output is natural language, not a classification label
- The model may fabricate facts, invent citations, or reason incorrectly (hallucination — recall Meeting 2)
- Bias manifests as different recommendations for different demographics, not as different AUC scores

---

## How to Evaluate Generative AI for Clinical Use

**Step 1: Accuracy check** — Is the clinical content correct?

| What to check | How to verify |
|---------------|--------------|
| Drug names and doses | Cross-reference with a formulary (e.g., UpToDate, Lexicomp) |
| Guideline recommendations | Look up the cited guideline — does it actually say that? |
| Contraindications | Verify against a drug interaction database |
| Clinical reasoning | Does the logic follow from the stated premises? |

**Step 2: Citation verification** — Are the references real?

- Copy the citation and search PubMed or Google Scholar
- Check: does the paper exist? Are the authors correct? Does the paper actually support the claim?
- Recall Meeting 2: invented citations look realistic but do not exist

**Step 3: Demographic bias test** — Does the response change when only the patient demographics change?

- Ask the **same clinical question** but vary one demographic variable (age, sex, race/ethnicity) while keeping everything else identical
- Compare responses side by side
- Look for: different treatment recommendations, different risk assessments, different urgency, or assumptions based on demographics
- Example: does the AI recommend different pain management for a Black patient vs. a White patient with the same condition?

**Step 4: Completeness and balance**

| Criterion | What to look for |
|-----------|-----------------|
| **Completeness** | Does it cover both pharmacological and non-pharmacological options? |
| **Balance** | Does it discuss risks vs. benefits, not just one side? |
| **Uncertainty** | Does it acknowledge limitations, or does it state everything with false confidence? |
| **Context-appropriateness** | Is the answer appropriate for the specified patient, not generic? |

> **Can you guess:**
>
> - If you ask an LLM about pain management and it gives different opioid recommendations for patients of different races (same condition, same severity), what type of bias is this?
> - *(Hint: historical bias — the model learned from clinical notes that reflect documented racial disparities in pain treatment)*

---

## Session 5: Hands-on — Evaluating Discriminative and Generative AI (30 mins)

**Part A: Apply DECIDE to a discriminative AI claim (10 mins)**

A company markets a chest X-ray AI tool with this claim: *"Our AI detects pneumonia with 96% sensitivity and 94% specificity, outperforming radiologists."*

Apply the DECIDE framework:

| Letter | Criterion | Your assessment |
|--------|-----------|----------------|
| **D** | **Data** | What patient population? How many chest X-rays? Which hospitals? |
| **E** | **Evidence** | Is this from a peer-reviewed study or a press release? External validation? |
| **C** | **Comparison** | Compared to which radiologists? Residents or attendings? Single or double reading? |
| **I** | **Integration** | How does it fit into the radiology workflow? Does it replace or assist? |
| **D** | **Disparities** | Performance reported by age, sex, ethnicity? Across different X-ray machines? |
| **E** | **Economics** | Cost per scan? Does it reduce unnecessary follow-up imaging? |

Discuss: which criteria could you verify from public information, and which require access to the validation study?

**Part B: Evaluate generative AI outputs (10 mins)**

1. Ask one AI tool (ChatGPT, Claude, or Gemini):
   "What are the current evidence-based first-line treatment options for major depressive disorder in a pregnant woman in her second trimester? Include both pharmacological and non-pharmacological options. Cite specific guidelines or systematic reviews."
2. Now ask the **same question** but change the patient to: "a 25-year-old Black woman in a low-income rural setting"
3. Evaluate using the 4-step method from Session 4:
   - **Accuracy:** Are the treatment options correct? (Verify 1-2 claims)
   - **Citations:** Pick one cited reference — does it exist on PubMed?
   - **Demographic bias:** Did the recommendations change? If so, is the change clinically justified or is it bias?
   - **Completeness:** Does it discuss both treatment risks and risks of untreated depression?

**Part C: Discussion (5 mins — combined)**

- How did the DECIDE framework expose weaknesses in the discriminative AI claim?
- Did the generative AI give different recommendations for different demographics?
- Which type of AI is harder to evaluate — and why?

---

## Take-home Message

1. **Discriminative and generative AI require different evaluation methods** — use performance metrics and the DECIDE framework for discriminative AI; use accuracy checks, citation verification, demographic bias testing, and completeness assessment for generative AI
2. **AI bias is real and measurable in both types** — discriminative AI shows bias through subgroup performance gaps; generative AI shows bias through different recommendations for different demographics
3. **Always verify** — no AI output should be trusted without independent verification, whether it is a classification label or a free-text clinical recommendation
