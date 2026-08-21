# AI Ethics, Regulation, and Governance in Healthcare

**Herdiantri Sufriyana**
Graduate Institute of Artificial Intelligence and Big Data in Healthcare
National Taiwan University of Nursing and Health Sciences

---

## Subtopics

- Privacy regulations — HIPAA, GDPR, Taiwan PDPA
- WHO and regulatory AI guidelines
- Responsible AI deployment principles
- Discussion: Ethical dilemmas in healthcare AI

---

## Session 1: Lecture — Privacy Regulations (25 mins)

---

## Why Privacy Matters for Healthcare AI

AI systems require large amounts of data to train — and in healthcare, that data is among the most sensitive information about a person. Privacy regulations establish the rules for how this data can be collected, used, and shared.

---

## Three Major Privacy Frameworks

**HIPAA (United States) — Health Insurance Portability and Accountability Act:**

| Aspect | Details |
|--------|---------|
| **Scope** | Covered entities (hospitals, insurers, providers) and their business associates |
| **Protected Health Information (PHI)** | Any individually identifiable health information — name, diagnosis, treatment, dates, etc. |
| **De-identification** | Safe Harbor method (remove 18 identifiers) or Expert Determination |
| **AI implication** | AI trained on PHI must comply with HIPAA; de-identified data can be used more freely |
| **Enforcement** | Fines up to USD 1.5 million per violation category per year |

**GDPR (European Union) — General Data Protection Regulation:**

| Aspect | Details |
|--------|---------|
| **Scope** | Any organization processing data of EU residents — applies globally |
| **Key rights** | Right to access, right to erasure ("right to be forgotten"), right to explanation of automated decisions |
| **Consent** | Must be explicit, informed, and freely given |
| **AI-specific** | Article 22: individuals have the right not to be subject to decisions based solely on automated processing |
| **Enforcement** | Fines up to 4% of global annual revenue or EUR 20 million |

**Taiwan PDPA — Personal Data Protection Act:**

| Aspect | Details |
|--------|---------|
| **Scope** | All public and private entities in Taiwan collecting personal data |
| **Medical data** | Classified as "sensitive personal data" — requires explicit consent or legal basis |
| **Cross-border transfer** | Allowed unless restricted by the central authority |
| **AI implication** | AI using patient data must comply with consent requirements; anonymization reduces restrictions |
| **Enforcement** | Fines up to NTD 500,000 for non-government entities (NTD 50 million for government) |

**Comparison:**

| Feature | HIPAA | GDPR | Taiwan PDPA |
|---------|-------|------|-------------|
| **Geographic scope** | US healthcare entities | Global (EU data subjects) | Taiwan |
| **Right to explanation** | Not explicit | Yes (Article 22) | Not explicit |
| **Right to erasure** | Limited | Yes | Yes (with exceptions) |
| **Consent model** | Implied for treatment, explicit for research | Explicit for all processing | Explicit for sensitive data |
| **AI-specific provisions** | Limited | Automated decision-making protections | Limited |

> **Can you guess:**
>
> - If a Taiwan hospital wants to use patient data to train an AI model, what steps must it take under the PDPA?
> - *(Hint: medical data is "sensitive personal data" — the hospital needs explicit consent or an approved legal basis, IRB approval for research, and proper anonymization practices)*

---

## Session 2: Lecture — WHO and Regulatory AI Guidelines (25 mins)

---

## International AI Governance Frameworks

**WHO Guidance on Ethics and Governance of AI for Health (2021, updated 2024):**

Six core principles:

| Principle | What it means | Healthcare application |
|-----------|-------------|----------------------|
| **1. Protect autonomy** | Humans must retain control over healthcare decisions | AI should inform, not replace, clinical judgment |
| **2. Promote well-being and safety** | AI must not cause harm | Rigorous validation before clinical deployment |
| **3. Ensure transparency** | AI processes should be understandable | Clinicians should know how the AI reaches its recommendations |
| **4. Foster accountability** | Clear responsibility when things go wrong | Defined liability — manufacturer, hospital, or clinician |
| **5. Ensure equity** | AI must not exacerbate health disparities | Performance validated across demographic subgroups |
| **6. Promote sustainability** | AI should be environmentally and socially sustainable | Consider computational costs and long-term maintenance |

---

## Regulatory Approaches Around the World

| Region | Regulatory body | Approach | AI-specific framework |
|--------|----------------|----------|----------------------|
| **United States** | FDA | Risk-based; 510(k), De Novo, PMA pathways | AI/ML Action Plan (2021); Predetermined Change Control Plan (2023) |
| **European Union** | EU AI Act + MDR | Risk-based classification (minimal to unacceptable) | EU AI Act (2024) — first comprehensive AI regulation globally |
| **Taiwan** | TFDA | Aligned with FDA framework | Guidance for AI medical devices under development |
| **China** | NMPA | Separate pathway for AI medical devices | Over 200 AI medical devices approved |
| **WHO** | Advisory (no enforcement) | Principles-based guidance | Six principles for AI in health |

---

## The EU AI Act (2024)

The world's first comprehensive AI law classifies AI systems by risk:

| Risk level | Definition | Healthcare examples | Requirements |
|-----------|-----------|-------------------|-------------|
| **Unacceptable** | AI that poses a clear threat to fundamental rights | Social scoring of patients | Banned |
| **High risk** | AI used in critical domains including healthcare | Diagnostic AI, treatment recommendation systems | Conformity assessment, data governance, transparency, human oversight |
| **Limited risk** | AI with transparency obligations | Chatbots for patient queries | Must disclose AI use |
| **Minimal risk** | Low-risk applications | Administrative scheduling AI | No specific requirements |

**Key requirements for high-risk healthcare AI under the EU AI Act:**
- Risk management system throughout the AI lifecycle
- Data governance — training data must be relevant, representative, and free from errors
- Technical documentation and record-keeping
- Transparency — users must be informed that they are interacting with AI
- Human oversight — ability to override or stop the AI system
- Accuracy, robustness, and cybersecurity requirements

> **Can you guess:**
>
> - Under the EU AI Act, would a chatbot that answers general health questions (not providing diagnoses) be classified as "high risk" or "limited risk"?
> - *(Hint: if the chatbot provides general wellness information without diagnostic claims, it is likely "limited risk" — but if it triages symptoms for urgency, it could be "high risk")*

---

## Session 3: Lecture — Responsible AI Deployment Principles (20 mins)

---

## From Regulation to Practice

Regulations set the floor. **Responsible AI deployment** sets a higher standard for ethical, safe, and equitable use.

**Core principles for responsible healthcare AI:**

| Principle | In practice |
|-----------|------------|
| **Informed consent** | Patients should know when AI is involved in their care |
| **Transparency** | Clinicians should understand AI capabilities and limitations |
| **Human-in-the-loop** | AI recommendations must be reviewed by qualified clinicians |
| **Continuous monitoring** | Track performance after deployment for drift and bias |
| **Fail-safe design** | When AI fails or is uncertain, default to the safer option |
| **Equity auditing** | Regularly assess performance across demographic groups |

---

## The Model Card

A **model card** (Mitchell et al., 2019) is a standardized document that accompanies an AI model:

| Section | Content |
|---------|---------|
| **Model details** | Who built it, version, type of model |
| **Intended use** | What it is designed for — and what it is NOT designed for |
| **Training data** | Description of data sources, demographics, size |
| **Performance** | Metrics on evaluation datasets, broken down by subgroup |
| **Limitations** | Known failure modes and populations where performance is degraded |
| **Ethical considerations** | Potential for bias, misuse, or harm |

**Why model cards matter for healthcare:**
- A clinician should be able to read the model card and decide whether the AI is appropriate for their patient population
- Without a model card, the clinician is deploying a black box with unknown limitations

> **Can you guess:**
>
> - If an AI vendor refuses to provide a model card, should a hospital still purchase the tool?
> - *(Hint: without transparency about training data, validation, and limitations, the hospital cannot evaluate safety — proceed with extreme caution or refuse)*

---

## Session 4: Discussion — Ethical Dilemmas in Healthcare AI (20 mins)

**Dilemma 1: Consent and awareness**

A hospital deploys an AI system that automatically prioritizes emergency department patients based on predicted acuity. Patients are not informed that AI is involved in their triage.

- Is it ethical to use AI in patient care without informing the patient?
- Does triage (prioritization) require the same level of consent as diagnosis?
- What if informing patients about AI causes anxiety or reduces trust?

**Dilemma 2: Algorithmic bias and resource allocation**

An AI model trained on historical US data is used to allocate post-discharge follow-up resources. The model systematically under-predicts risk for minority patients because the training data reflected lower healthcare utilization (due to access barriers, not lower need).

- Who is responsible for the disparity — the developer, the hospital, or the healthcare system?
- Should a hospital deploy an AI tool if they know it has performance disparities but no better alternative exists?
- How should the bias be communicated to clinicians using the tool?

**Dilemma 3: AI and the clinician's skill**

A radiology AI system detects subtle findings that junior radiologists would miss. Over time, junior radiologists begin to rely on the AI and develop less skill in detecting those findings independently.

- Does AI dependency erode clinical competence?
- If the AI system goes offline, can the radiologists still perform at an acceptable level?
- How should training programs adapt to the presence of AI?

**Dilemma 4: Cross-border data and AI**

A Taiwanese hospital wants to use a US-developed AI model. The model was trained on US patient data and validated on US populations. To fine-tune it for Taiwan, patient data would need to be shared with the US developer.

- What are the data sovereignty and privacy implications under Taiwan PDPA?
- If the model is not fine-tuned, performance may be suboptimal. If data is shared, privacy may be compromised. How do you balance these?
- Could synthetic data or federated learning solve this dilemma?

**Group activity:** Each group is assigned one dilemma. Discuss for 10 minutes, then present your group's position and reasoning to the class. Other groups may challenge or add perspectives.

---

## Take-home Message

1. **Privacy regulations (HIPAA, GDPR, Taiwan PDPA) set the legal boundaries** — but healthcare AI professionals must understand the specific requirements for medical data use, especially consent and de-identification
2. **Global governance is evolving rapidly** — WHO principles, FDA action plans, and the EU AI Act represent the emerging regulatory landscape; Taiwan's framework is developing in parallel
3. **Responsible deployment goes beyond compliance** — model cards, equity auditing, human oversight, and continuous monitoring are not optional extras; they are essential safeguards for patient safety
