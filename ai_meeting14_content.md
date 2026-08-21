# Emerging Trends and Global Perspectives in Healthcare AI

**Herdiantri Sufriyana**
Graduate Institute of Artificial Intelligence and Big Data in Healthcare
National Taiwan University of Nursing and Health Sciences

---

## Subtopics

- AI in global health and low-resource settings
- Wearables, digital therapeutics, and remote monitoring
- Future directions — what is coming in 2027-2030
- Discussion: How AI will reshape healthcare careers

---

## Session 1: Lecture — AI in Global Health and Low-Resource Settings (25 mins)

---

## The Global Health Challenge

**Healthcare access varies dramatically worldwide:**

| Indicator | High-income countries | Low- and middle-income countries (LMICs) |
|-----------|----------------------|------------------------------------------|
| **Physicians per 10,000 people** | 30-50 | 1-10 |
| **Radiologists per million** | 50-100 | 0.1-1 |
| **Pathologists per million** | 30-60 | 0.1-2 |
| **Hospital beds per 1,000** | 4-8 | 0.5-2 |
| **Health spending per capita** | USD 3,000-10,000 | USD 20-300 |

AI has the potential to bridge these gaps — but only if solutions are designed for low-resource contexts.

---

## AI Applications for Low-Resource Settings

**Key applications where AI can make the biggest impact in LMICs:**

| Application | Problem it solves | How it works | Example |
|-------------|------------------|-------------|---------|
| **AI-assisted diagnostics on mobile phones** | No specialists available | Deep learning model runs on smartphone camera | Skin disease classification, malaria detection from blood smears |
| **AI triage in community health** | Limited clinical workforce | Chatbot or decision support guides community health workers | Ada Health, Babylon Health in sub-Saharan Africa |
| **AI for medical imaging interpretation** | No radiologists | Cloud-based AI reads chest X-rays and mammograms | Qure.ai detecting tuberculosis on chest X-rays in India |
| **AI for disease surveillance** | Delayed outbreak detection | NLP monitors social media, news, and health records for outbreaks | BlueDot detected COVID-19 spread before WHO announcement |
| **AI for supply chain optimization** | Drug stockouts in remote areas | Predictive models forecast demand and optimize distribution | Zipline drone delivery + AI demand prediction in Rwanda |

---

## Design Constraints for Low-Resource AI

AI solutions for global health must work within severe constraints.

**Design requirements:**

| Constraint | Implication for AI design |
|------------|--------------------------|
| **Limited internet connectivity** | Models must run offline on devices (edge AI) |
| **Low-cost hardware** | Models must be small enough for basic smartphones |
| **Limited electricity** | Battery-efficient inference required |
| **Non-specialist users** | Interface must be simple with minimal training needed |
| **Diverse populations** | Model must work across ethnicities, body types, and disease presentations not well-represented in training data |
| **Different disease profiles** | Models trained on high-income country data may not transfer to LMIC disease patterns |

> **Can you guess:**
>
> - A skin disease AI trained on images from US and European patients is deployed in sub-Saharan Africa. What problem might arise?
> - *(Hint: the AI was trained predominantly on lighter skin tones — diagnostic accuracy drops significantly for darker skin, potentially causing misdiagnosis and harm)*

---

## Ethical Considerations in Global Health AI

| Issue | Description |
|-------|------------|
| **Data colonialism** | Collecting health data from LMICs to build AI products that are sold back at high prices |
| **Algorithmic bias** | Models that perform well on populations in training data but poorly on underrepresented groups |
| **Dependency** | Countries relying on foreign AI tools without building local capacity |
| **Consent and governance** | How to obtain meaningful informed consent in communities with low digital literacy |
| **Sustainability** | AI tools that require ongoing vendor support — what happens when the grant ends? |

> **Can you guess:**
>
> - A global health organization collects genomic data from an African population, trains an AI model, and patents the resulting drug target. Is this ethical?
> - *(Hint: this is a real and ongoing debate — benefit-sharing, data sovereignty, and the Nagoya Protocol on genetic resources are all relevant)*

---

## Session 2: Lecture — Wearables, Digital Therapeutics, and Remote Monitoring (25 mins)

---

## AI-Powered Wearable Devices

**The wearable health ecosystem (2026):**

| Device category | Sensors | AI-analyzed metrics | Clinical application |
|----------------|---------|-------------------|---------------------|
| **Smartwatches** | Optical heart rate, accelerometer, SpO2, temperature | Arrhythmia detection, fall detection, sleep staging | Apple Watch AFib detection (FDA-cleared) |
| **Continuous glucose monitors** | Subcutaneous glucose sensor | Blood sugar trends, insulin dosing prediction | Dexcom G7 + AI-based glucose prediction |
| **Smart rings** | PPG, temperature, accelerometer | HRV, menstrual cycle prediction, early illness detection | Oura Ring fever detection during COVID-19 |
| **Patch monitors** | ECG, accelerometer, respiration | Long-term cardiac monitoring, seizure detection | Zio patch 14-day continuous ECG |
| **Smart clothing** | Textile-embedded sensors | Gait analysis, muscle activity, posture | Rehabilitation monitoring for stroke patients |

---

## Digital Therapeutics (DTx)

**Digital therapeutics** are evidence-based software interventions that treat, manage, or prevent medical conditions — prescribed by clinicians, regulated like drugs.

**How DTx differs from wellness apps:**

| Feature | Wellness app | Digital therapeutic |
|---------|-------------|-------------------|
| **Regulatory status** | Not regulated | FDA-cleared or CE-marked |
| **Evidence required** | None | Randomized controlled trials |
| **Prescription** | Over-the-counter | Prescribed by clinician |
| **Reimbursement** | Patient pays out-of-pocket | Insurance-covered in many markets |
| **Clinical claims** | "May help with..." | "Treats [specific condition]" |

**FDA-cleared digital therapeutics (as of 2026):**

| Product | Condition | How AI is used |
|---------|-----------|---------------|
| **reSET / reSET-O** (Pear Therapeutics) | Substance use disorder | AI personalizes cognitive behavioral therapy modules |
| **EndeavorRx** (Akili) | ADHD in children | AI adapts game difficulty based on attention patterns |
| **Somryst/Pear-004** | Insomnia | AI-guided CBT-I with adaptive session scheduling |
| **Freespira** | PTSD, panic disorder | Biofeedback with AI-guided breathing protocols |

> **Can you guess:**
>
> - A patient asks: "Why do I need a prescription for an app?" How would you explain the difference between a wellness app and a digital therapeutic?
> - *(Hint: digital therapeutics are tested in clinical trials and proven to treat conditions, just like medications — the prescription ensures appropriate use and clinical oversight)*

---

## AI for Remote Patient Monitoring

**Remote patient monitoring (RPM)** uses connected devices and AI to track patients outside the hospital.

**How AI enhances RPM:**

| Traditional RPM | AI-enhanced RPM |
|----------------|-----------------|
| Sends data to clinician for review | AI analyzes data and alerts clinician only when intervention is needed |
| Threshold-based alerts (e.g., HR > 120) | Personalized alerts based on patient baseline and trends |
| Reactive — clinician responds after alert | Predictive — AI detects deterioration before symptoms appear |
| Generates data overload for clinical teams | AI filters and prioritizes, reducing alert burden |

**Example — heart failure remote monitoring:**
1. Patient wears a smart scale, blood pressure cuff, and pulse oximeter at home
2. AI model learns patient's personal baseline over 2 weeks
3. AI detects a pattern: gradual weight increase (2 kg over 3 days) + rising blood pressure + decreasing SpO2
4. AI generates alert to heart failure nurse: "Patient shows early decompensation pattern — consider diuretic adjustment"
5. Nurse contacts patient, adjusts medication — hospitalization prevented

> **Can you guess:**
>
> - Why are personalized baselines better than fixed thresholds for remote monitoring?
> - *(Hint: a resting heart rate of 90 bpm is abnormal for an athlete but normal for an elderly patient with chronic conditions — fixed thresholds generate too many false alarms)*

---

## Session 3: Lecture — Future Directions: 2027-2030 (20 mins)

---

## What is Coming in Healthcare AI?

**Near-term trends (2027-2028):**

| Trend | Description | Impact |
|-------|------------|--------|
| **Foundation models for medicine** | Large multimodal models trained on medical images, text, and genomics together | Single model handles radiology, pathology, and clinical reasoning |
| **Ambient AI in clinical settings** | AI passively observes clinical encounters and generates documentation | Near-complete elimination of manual documentation |
| **AI-native EHR systems** | New EHR systems designed with AI at the core, not bolted on | Natural language queries replace click-based navigation |
| **Federated learning at scale** | Hospitals train AI models collaboratively without sharing patient data | Better models for rare diseases, multi-institutional studies |

**Medium-term trends (2029-2030):**

| Trend | Description | Impact |
|-------|------------|--------|
| **Autonomous clinical decision support** | AI makes specific clinical recommendations with quantified confidence | Shift from "information" to "action" — AI suggests, clinician approves |
| **Digital twins for patients** | Computational model of individual patient physiology | Simulate treatment effects before administering |
| **AI-designed clinical trials** | AI selects endpoints, sample size, patient population, and adaptive rules | Faster, cheaper trials with higher success rates |
| **Continuous learning systems** | Models that update in real-time from clinical outcomes | Performance improves over time without manual retraining |

> **Can you guess:**
>
> - What regulatory challenge must be solved before "continuous learning" AI systems can be deployed in hospitals?
> - *(Hint: current FDA approval is for a fixed model — if the model changes after approval, does it need re-approval? The FDA's Predetermined Change Control Plan framework is trying to address this)*

---

## The Regulatory Landscape is Evolving

**Key regulatory developments:**

| Framework | Organization | Key provision |
|-----------|-------------|---------------|
| **AI/ML Action Plan** | US FDA | Framework for approving AI that learns and adapts over time |
| **AI Act** | European Union | Risk-based classification — high-risk medical AI requires conformity assessment |
| **Good Machine Learning Practice** | FDA + Health Canada + UK MHRA | 10 guiding principles for AI/ML in medical devices |
| **Predetermined Change Control Plan** | US FDA | Manufacturers can pre-specify how an AI model will be updated post-approval |

---

## Session 4: Hands-on — Exploring Emerging AI Health Technologies (20 mins)

---

## Activity: Evaluating Emerging Healthcare AI

**Task:** Research and evaluate an emerging healthcare AI technology using a structured framework.

**Steps:**

1. **Select one emerging technology** from the list below (or propose your own):
   - AI-powered mental health chatbots (e.g., Woebot, Wysa)
   - AI skin cancer detection apps (e.g., SkinVision, DermAssist)
   - AI-powered drug interaction checkers
   - AI ambient documentation (e.g., Nuance DAX, Abridge)
   - AI genetic risk calculators (e.g., 23andMe health reports)

2. **Research the technology** using your browser (10 mins):
   - What does it do? Who is the target user?
   - What AI/ML technique does it use?
   - Is it FDA-cleared or CE-marked?
   - What evidence supports its effectiveness?

3. **Evaluate using this framework:**

   | Criterion | Your assessment |
   |-----------|----------------|
   | **Clinical validity** — Is there evidence it works? | |
   | **Safety** — What could go wrong? | |
   | **Equity** — Does it work equally well for all populations? | |
   | **Usability** — Can the target user actually use it? | |
   | **Sustainability** — Will this technology exist in 5 years? | |
   | **Regulatory status** — Is it legally authorized for clinical use? | |

4. **Present your findings:** 2-minute summary to the class — would you recommend this technology for adoption in a Taiwan hospital?

---

## Session 5: Discussion — How AI Will Reshape Healthcare Careers (20 mins)

---

## AI and the Future of Healthcare Professions

**Which healthcare roles will be most affected by AI?**

| Role | AI impact | How the role changes |
|------|-----------|---------------------|
| **Radiologist** | High — AI can read many imaging types at expert level | Shift from "reading images" to "overseeing AI, handling complex cases, and communicating with clinicians" |
| **Pathologist** | High — AI achieves expert-level performance in histopathology | Shift from microscope work to computational pathology oversight |
| **Primary care physician** | Medium — AI assists with documentation, triage, and decision support | More time for patient relationships; less paperwork |
| **Nurse** | Medium — AI assists with monitoring, documentation, and care coordination | Shift from data collection to data-informed decision making |
| **Pharmacist** | Medium — AI checks interactions and optimizes dosing | Shift from dispensing to clinical pharmacology and AI oversight |
| **Health administrator** | Medium — AI optimizes scheduling, billing, and resource allocation | Shift from operational tasks to strategic leadership |
| **Data scientist / AI specialist** | Low — demand increasing | New role in healthcare; bridge between clinical and technical |

**Key insight:** AI will not replace healthcare professionals — it will replace healthcare professionals who do not learn to work with AI.

---

## Discussion Questions

Discuss in small groups (10 mins), then share with the class (10 mins):

1. **Personal impact:** How do you think AI will change YOUR specific career in healthcare over the next 5 years? What new skills should you develop?

2. **Equity question:** AI development is concentrated in high-income countries and large technology companies. How can we ensure that Taiwan's healthcare system benefits from AI without becoming dependent on foreign technology?

3. **Education question:** Should AI literacy be a required competency for all healthcare professionals? What should that curriculum include?

4. **Ethics question:** If an AI system can diagnose a condition more accurately than a human physician, should patients have the right to choose AI-only diagnosis? Why or why not?

5. **Looking ahead:** Based on everything you have learned in this course (Weeks 1-14), what is the single most important thing a healthcare organization should do TODAY to prepare for the AI-transformed healthcare of 2030?

---

## Course Wrap-up

**What we covered in this course:**

| Week | Topic |
|------|-------|
| 1-3 | Foundations — what is AI, types of AI, and AI in healthcare landscape |
| 4-5 | Clinical AI — medical imaging, NLP, clinical decision support |
| 6-7 | Data and ethics — healthcare data, privacy, bias, regulation |
| 8-9 | Evaluation — how to assess AI tools, clinical validation, real-world evidence |
| 10 | Generative AI — report generation, drug discovery, quality control |
| 11 | AI agents — autonomous workflows, no-code tools, governance |
| 12 | Precision medicine — genomics, biomarkers, multi-omics |
| 13 | AI strategy — implementation frameworks, cost-benefit, change management |
| 14 | Emerging trends — global health, wearables, digital therapeutics, future directions |

---

## Take-home Message

1. **AI in global health** can bridge healthcare access gaps — but solutions must be designed for low-resource constraints including limited connectivity, low-cost hardware, and diverse populations
2. **Wearables and digital therapeutics** are creating a new paradigm of continuous, AI-powered health monitoring outside the hospital — with FDA-cleared software treatments becoming mainstream
3. **The next 5 years** will bring foundation models, ambient AI, digital twins, and continuous learning systems — the regulatory landscape is adapting but lagging behind the technology
4. **Healthcare careers** will be reshaped, not replaced, by AI — the professionals who thrive will be those who learn to evaluate, use, and oversee AI tools effectively
