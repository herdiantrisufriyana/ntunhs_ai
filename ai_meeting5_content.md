# AI for Clinical Decision Support

**Herdiantri Sufriyana**
Graduate Institute of Artificial Intelligence and Big Data in Healthcare
National Taiwan University of Nursing and Health Sciences

---

## Subtopics

- Current clinical decision support systems
- Evidence-based AI tools in clinical practice
- FDA-approved AI medical devices
- Case study: Deployed clinical AI tools

---

## Session 1: Lecture — Clinical Decision Support Systems (25 mins)

---

## What is Clinical Decision Support?

**Clinical decision support (CDS)** provides clinicians, patients, or other healthcare stakeholders with knowledge and person-specific information to enhance health and healthcare decisions at the point of care.

**Evolution of CDS:**

| Generation | Era | How it works | Example |
|-----------|-----|-------------|---------|
| **Rule-based** | 1990s-2010s | If-then rules coded by experts | "If potassium > 6.0, alert physician" |
| **Guideline-based** | 2000s-2010s | Encodes clinical practice guidelines | Antibiotic selection based on infection site and local resistance |
| **ML-based** | 2015-present | Learns patterns from patient data | Predicting 30-day readmission risk from EHR data |
| **LLM-enhanced** | 2023-present | Natural language interaction with medical knowledge | Chatbot that answers clinical questions with cited evidence |

---

## Where CDS Fits in Clinical Workflow

| Decision point | CDS function | Example tool |
|---------------|-------------|-------------|
| **Triage** | Risk stratification | ESI algorithm, AI-based acuity prediction |
| **Diagnosis** | Differential diagnosis support | Glass AI, Isabel Healthcare |
| **Ordering** | Drug interaction and allergy checks | EHR-integrated alerts (Epic, Cerner) |
| **Treatment** | Guideline-concordant therapy selection | UpToDate, DynaMedex |
| **Monitoring** | Early warning scores | NEWS2, Modified Early Warning Score |
| **Discharge** | Readmission risk prediction | HOSPITAL score, LACE index |

**The alert fatigue problem:**
- EHR systems generate an overwhelming number of alerts
- Studies show clinicians override **49-96%** of drug interaction alerts
- If everything is flagged, nothing is prioritized — this is a critical design failure
- Modern AI-based CDS aims to reduce alert volume while improving signal quality

> **Can you guess:**
>
> - Why might a CDS system with 95% sensitivity and 80% specificity still fail in practice?
> - *(Hint: if the baseline event rate is low, even 80% specificity generates many false alarms — consider a hospital with 1,000 patients per day)*

---

## Session 2: Lecture — Evidence-Based AI Tools in Practice (20 mins)

---

## AI-Powered CDS Tools Available Today

**Diagnostic AI tools:**

| Tool | Application | How it works |
|------|------------|-------------|
| **Isabel Healthcare** | Differential diagnosis generator | Enter symptoms, get ranked differential — used in >350 healthcare systems |
| **Glass AI** | AI-generated differential and workup plan | LLM-based, generates DDx with reasoning |
| **VisualDx** | Dermatology and visual diagnosis | Image + symptom matching for skin conditions |
| **Babylon Health (Symptom Checker)** | Patient-facing triage | Chatbot asks questions, suggests urgency level |

**Documentation AI tools:**

| Tool | Application | Status |
|------|------------|--------|
| **DAX Copilot (Nuance/Microsoft)** | Ambient clinical documentation | Deployed in major health systems (2024-2025) |
| **Abridge** | Conversation-to-note generation | Used by Epic-integrated health systems |
| **Suki** | Voice-enabled documentation assistant | Integrates with multiple EHR platforms |

**Research and knowledge AI tools:**

| Tool | Application | Advantage |
|------|------------|-----------|
| **UpToDate with AI** | Evidence synthesis | Curated by physicians, continuously updated |
| **DynaMedex** | Point-of-care decision support | Systematic review-based recommendations |
| **Consensus** | AI search over peer-reviewed papers | Shows level of agreement across studies |

**Important distinction:**
- **General-purpose LLMs** (ChatGPT, Claude) are NOT clinical decision support systems — they are general AI assistants
- **CDS tools** are specifically designed, validated, and often regulated for clinical use
- Using a general LLM for clinical decisions is like using Google for diagnosis — possible, but risky

> **Can you guess:**
>
> - What is the difference between Glass AI and ChatGPT for generating a differential diagnosis?
> - *(Hint: Glass AI is specifically designed for clinical DDx with structured medical reasoning, while ChatGPT is general-purpose and may hallucinate medical facts)*

---

## Session 3: Lecture — FDA-Approved AI Medical Devices (20 mins)

---

## The Regulatory Landscape

**FDA authorization of AI/ML medical devices (as of 2025):**

| Year | Cumulative authorized devices | Notable examples |
|------|------------------------------|-----------------|
| 2018 | 100+ | IDx-DR (first autonomous AI diagnostic — diabetic retinopathy) |
| 2020 | 300+ | Caption Health (cardiac ultrasound guidance) |
| 2022 | 521 | Rapid growth in radiology AI |
| 2023 | 692 | Expansion into pathology, ophthalmology |
| 2024 | 882 | Radiology still >75% of all authorized devices |
| 2025 | 950+ | First wave of AI-enabled ambient documentation |

**Distribution by specialty:**

| Specialty | Share of FDA-authorized AI devices | Common applications |
|-----------|-----------------------------------|-------------------|
| **Radiology** | ~75% | CT/MRI triage, chest X-ray analysis, mammography |
| **Cardiology** | ~10% | ECG interpretation, echocardiogram analysis |
| **Ophthalmology** | ~5% | Diabetic retinopathy, glaucoma screening |
| **Pathology** | ~3% | Digital pathology slide analysis |
| **Other** | ~7% | Dermatology, neurology, orthopedics |

**FDA regulatory pathways for AI:**

| Pathway | Timeline | Requirement | Used for |
|---------|----------|-------------|---------|
| **510(k)** | 3-6 months | Substantially equivalent to existing device | Most AI medical devices |
| **De Novo** | 6-12 months | Novel device, low-moderate risk | First-in-class AI devices (e.g., IDx-DR) |
| **PMA** | 1-3 years | Highest evidence burden | High-risk devices |
| **Predetermined Change Control Plan** | Varies | Allows AI to update without new submission | Adaptive AI that learns over time (2023 framework) |

**Taiwan's regulatory framework:**
- TFDA follows a similar pathway structure to FDA
- AI medical device regulations are still evolving
- Most hospitals in Taiwan use internationally authorized devices

> **Can you guess:**
>
> - Why does radiology dominate FDA-authorized AI devices?
> - *(Hint: radiology produces standardized digital images, has well-defined classification tasks, and has large labeled training datasets)*

---

## Session 4: Discussion — Deployed Clinical AI Case Studies (25 mins)

**Case 1: IDx-DR — Autonomous Diabetic Retinopathy Screening**

- **What:** First FDA-authorized autonomous AI diagnostic (2018, De Novo pathway)
- **How it works:** Patient's retinal photos are taken by a technician; AI analyzes images and provides a diagnosis without physician interpretation
- **Performance:** 87.2% sensitivity, 90.7% specificity in the pivotal trial
- **Deployment:** Used in primary care clinics, pharmacies, and endocrinology practices
- **Impact:** Enables screening in settings without an ophthalmologist

**Case 2: Viz.ai — Large Vessel Occlusion Stroke Detection**

- **What:** AI analyzes CT angiograms to detect large vessel occlusion (LVO) strokes
- **How it works:** Automatically alerts the stroke team when LVO is detected, reducing time to treatment
- **Performance:** Reduced time from imaging to specialist notification by ~30 minutes
- **Deployment:** Used in over 1,400 hospitals in the US
- **Impact:** Faster treatment in stroke — every minute saved preserves brain tissue

**Discussion questions:**

1. IDx-DR works autonomously (no physician reviews the image). When is autonomous AI appropriate vs. AI that assists a physician?
2. Viz.ai does not diagnose — it alerts. Is an alerting system less risky than a diagnostic system? Why?
3. Both tools were validated in controlled trials. What could go wrong in a hospital with different patient demographics?
4. Would these tools work in Taiwan's healthcare system? What adaptations would be needed?
5. If you were a hospital administrator, what evidence would you require before purchasing an AI clinical tool?

**Group activity:** Each group picks one FDA-authorized AI device from [FDA's AI/ML device list](https://www.fda.gov/medical-devices/software-medical-device-samd/artificial-intelligence-and-machine-learning-aiml-enabled-medical-devices) and presents: what it does, what evidence supports it, and whether they would recommend it for a Taiwan hospital.

---

## Take-home Message

1. **Clinical decision support is evolving from simple rule-based alerts to AI-powered systems** — but alert fatigue remains a major unsolved problem
2. **Over 950 AI medical devices are FDA-authorized** — predominantly in radiology, with the first autonomous diagnostic (IDx-DR) setting a precedent for AI without physician oversight
3. **Regulatory approval does not guarantee real-world success** — validation in controlled trials may not reflect performance in your hospital's patient population
