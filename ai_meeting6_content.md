# AI in Medical Imaging

**Herdiantri Sufriyana**
Graduate Institute of Artificial Intelligence and Big Data in Healthcare
National Taiwan University of Nursing and Health Sciences

---

## Subtopics

- Computer vision for radiology, pathology, dermatology
- Performance evaluation of imaging AI
- Clinical integration challenges
- Video and discussion: Real-world deployment examples

---

## Session 1: Lecture — Computer Vision for Medical Imaging (25 mins)

---

## How AI Sees Medical Images

**Computer vision** is the field of AI that enables machines to interpret and analyze visual information. In healthcare, it processes medical images to detect, classify, or segment abnormalities.

**How convolutional neural networks (CNNs) work — simplified:**

| Step | What happens | Analogy |
|------|-------------|---------|
| **1. Input** | The image is fed as a grid of pixel values | Like a digital photo — each pixel has a number |
| **2. Convolutional layers** | Filters detect low-level features (edges, textures) | Like a magnifying glass scanning for specific patterns |
| **3. Deeper layers** | Combine low-level features into high-level concepts | Edges combine into shapes, shapes into structures |
| **4. Classification** | Final layer outputs a probability for each class | "85% probability this is a malignant lesion" |

**Key point:** The AI does not "understand" anatomy. It recognizes statistical patterns in pixel arrangements that correlate with diagnoses in the training data.

---

## AI Applications by Imaging Specialty

**Radiology:**

| Application | What AI does | Example system |
|------------|-------------|---------------|
| **Chest X-ray triage** | Flags critical findings (pneumothorax, PE) for priority reading | Qure.ai, Aidoc |
| **Mammography** | Detects suspicious masses and calcifications | Lunit INSIGHT MMG, Transpara |
| **CT stroke detection** | Identifies large vessel occlusion | Viz.ai, RapidAI |
| **Lung nodule detection** | Measures and tracks pulmonary nodules on CT | Veye Lung Nodules |
| **Fracture detection** | Identifies fractures on X-ray | Imagen OsteoDetect |

**Pathology:**

| Application | What AI does | Example |
|------------|-------------|---------|
| **Whole slide image analysis** | Classifies tissue regions on digitized pathology slides | Paige AI (first FDA-authorized pathology AI) |
| **Mitosis counting** | Automates counting of dividing cells for cancer grading | Research tools, not yet widely deployed |
| **Biomarker detection** | Identifies molecular markers from tissue morphology | Predicting HER2 status from H&E slides |

**Dermatology:**

| Application | What AI does | Example |
|------------|-------------|---------|
| **Skin lesion classification** | Classifies moles/lesions as benign or malignant | DermAssist (Google), SkinVision |
| **Teledermatology triage** | Prioritizes lesions for dermatologist review | First Derm |
| **Wound assessment** | Measures wound size and healing progress | Swift Medical, Tissue Analytics |

> **Can you guess:**
>
> - A dermatology AI trained on light-skinned patients achieves 95% accuracy. What might happen when used on dark-skinned patients?
> - *(Hint: skin lesion appearance varies significantly across skin tones — if the training data lacks diversity, the AI will underperform on underrepresented populations)*

---

## Session 2: Lecture — Performance Evaluation of Imaging AI (25 mins)

---

## How to Evaluate an Imaging AI System

**Standard performance metrics:**

| Metric | What it measures | In imaging context |
|--------|-----------------|-------------------|
| **Sensitivity (Recall)** | Proportion of true positives correctly detected | "Of all cancers present, how many did the AI find?" |
| **Specificity** | Proportion of true negatives correctly identified | "Of all normal images, how many did the AI correctly call normal?" |
| **AUC-ROC** | Overall discriminative ability across all thresholds | Higher AUC = better separation between normal and abnormal |
| **PPV (Precision)** | Among AI-flagged images, how many are truly abnormal | Important when alert fatigue is a concern |
| **NPV** | Among AI-cleared images, how many are truly normal | Critical for screening — missed cancers are the worst outcome |

---

## Standalone AI vs. AI + Physician

**Three deployment models:**

| Model | How it works | When appropriate |
|-------|-------------|-----------------|
| **AI standalone** | AI makes the diagnosis without human review | Only for low-risk, well-validated tasks (e.g., IDx-DR) |
| **AI triage** | AI prioritizes cases for human review but does not diagnose | Chest X-ray triage — critical findings read first |
| **AI + physician** | AI provides a second read; physician makes final decision | Most current imaging AI deployments |

**Key study: AI vs. radiologists in mammography**

A 2024 Lancet Oncology study (Dembrower et al.) compared AI-supported mammography screening vs. standard double reading in Sweden:

- AI + one radiologist detected the same number of cancers as two radiologists
- Reduced radiologist workload by **44%**
- False positive rate was similar between groups
- Conclusion: AI can safely replace one of two radiologists in double-reading programs

**Performance in context — base rate matters:**

| Scenario | Prevalence | Sensitivity | Specificity | PPV |
|----------|-----------|-------------|-------------|-----|
| Mammography screening | 0.5% | 90% | 95% | 8.3% |
| ED chest X-ray triage | 5% | 90% | 95% | 48.6% |
| ICU pneumonia detection | 20% | 90% | 95% | 82.0% |

**Even with identical sensitivity and specificity, PPV varies dramatically with prevalence.** In screening (low prevalence), most AI "positive" findings are false positives.

> **Can you guess:**
>
> - If an AI mammography system has 90% sensitivity and 95% specificity, and you screen 10,000 women (prevalence 0.5%), how many false positives will there be?
> - *(Hint: 50 true cancers x 0.9 = 45 detected; 9,950 normal x 0.05 false positive rate = 498 false alarms — roughly 10 false positives for every true cancer detected)*

---

## Session 3: Lecture — Clinical Integration Challenges (20 mins)

---

## Why Deploying Imaging AI Is Harder Than Building It

| Challenge | Description | Real-world example |
|-----------|------------|-------------------|
| **Data shift** | Training data differs from deployment data | AI trained on US hospital images fails on images from a different scanner brand |
| **Workflow integration** | AI must fit into existing PACS and reading workflows | Radiologists will not open a separate app — AI must appear in their normal viewer |
| **Latency** | AI must return results fast enough to be useful | Stroke detection must alert within minutes, not hours |
| **Regulatory updates** | AI that learns from new data needs re-approval | Predetermined change control plans (FDA, 2023) address this |
| **Liability** | Who is responsible when AI makes an error? | The radiologist? The hospital? The AI manufacturer? |
| **Cost justification** | Hospitals must see return on investment | Does AI save enough time to justify the licensing fee? |
| **Bias and equity** | AI may perform worse on underrepresented populations | Chest X-ray AI has shown disparities across racial groups |

**The "last mile" problem:**
Building an accurate AI model is perhaps 20% of the challenge. The remaining 80% is integrating it into clinical workflows, ensuring consistent performance, maintaining regulatory compliance, and managing change among clinical staff.

> **Can you guess:**
>
> - A hospital purchases an AI chest X-ray system validated on data from US hospitals. They deploy it in Taiwan. What might go wrong?
> - *(Hint: differences in patient demographics, disease prevalence, scanner manufacturers, image protocols, and clinical workflows can all degrade performance)*

---

## Session 4: Discussion — Real-World Deployment Examples (20 mins)

**Example 1: Lunit INSIGHT MMG in South Korea**

Lunit's mammography AI was deployed across screening programs in South Korea:
- Increased cancer detection rate by 10% compared to radiologist-only reading
- The AI caught cancers that radiologists missed, and radiologists caught cancers the AI missed
- Combined AI + radiologist outperformed either alone
- Challenge: integration with existing PACS systems required significant IT investment

**Example 2: Qure.ai in India and Africa**

Qure.ai deployed chest X-ray AI for tuberculosis screening in low-resource settings:
- Designed to work on portable X-ray machines with lower image quality
- Achieved >95% sensitivity for TB detection in field conditions
- Reduced the need for specialist radiologists in rural areas
- Challenge: maintaining performance across different X-ray equipment and patient populations

**Example 3: Paige AI in Digital Pathology**

Paige received the first FDA authorization for AI in pathology (2021):
- Detects cancer on prostate biopsy slides
- Sensitivity increased from 89.5% (pathologist alone) to 96.0% (pathologist + AI)
- Significantly reduced the chance of missing cancer
- Challenge: requires digitization of glass slides — many pathology labs still use microscopes

**Discussion questions:**

1. All three examples show AI + human outperforming either alone. Is this always the case? When might AI alone be acceptable?
2. Qure.ai was designed for low-resource settings. How does the deployment context affect AI design choices?
3. Digital pathology requires complete workflow transformation (glass slides to digital). Is the performance improvement worth the infrastructure cost?
4. If you were designing an imaging AI for Taiwan's healthcare system, which application would have the most impact?

---

## Take-home Message

1. **Medical imaging AI is the most mature clinical AI application** — over 75% of FDA-authorized AI devices are in radiology, with growing applications in pathology and dermatology
2. **Performance metrics must be interpreted in clinical context** — the same sensitivity and specificity produce very different PPV depending on disease prevalence
3. **Clinical integration is the greatest challenge** — workflow fit, data shift, bias, liability, and cost justify are harder problems than model accuracy
