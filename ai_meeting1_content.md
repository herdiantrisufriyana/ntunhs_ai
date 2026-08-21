# Introduction — The AI Revolution in Healthcare

**Herdiantri Sufriyana**
Graduate Institute of Artificial Intelligence and Big Data in Healthcare
National Taiwan University of Nursing and Health Sciences

---

## Subtopics

- What AI can and cannot do in 2026
- Overview of major AI tools and platforms
- AI in healthcare timeline 2020-2026
- Discussion: A healthcare AI deployment case study

---

## Session 1: Lecture — What AI Can and Cannot Do in 2026 (20 mins)

---

## What is Artificial Intelligence?

**Artificial intelligence (AI)** refers to computer systems that perform tasks typically requiring human intelligence — recognizing patterns, understanding language, making decisions, and generating content.

**Key distinction:**

| Term | What it means | Example |
|------|--------------|---------|
| **Narrow AI** | Trained for a specific task | Chest X-ray abnormality detection |
| **General AI** | Hypothetical system that can do any intellectual task | Does not exist yet |
| **Generative AI** | Creates new content (text, images, code) from learned patterns | ChatGPT, Claude, Gemini |

---

## What AI Can Do in 2026

| Capability | Healthcare example |
|------------|-------------------|
| **Summarize literature** | Condense 50 papers into a structured summary in minutes |
| **Draft clinical documentation** | Generate discharge summaries from structured notes |
| **Detect patterns in images** | Flag suspicious lesions on mammograms or skin photos |
| **Answer clinical questions** | Provide evidence-based differential diagnoses |
| **Translate languages** | Real-time translation for patient-provider communication |
| **Extract data from records** | Pull structured variables from unstructured clinical notes |

---

## What AI Cannot Do in 2026

| Limitation | Why it matters |
|-----------|---------------|
| **Guarantee factual accuracy** | AI can generate plausible but wrong information (hallucination) |
| **Replace clinical judgment** | AI lacks patient context, values, and physical examination |
| **Learn from a single case** | Models need large datasets; rare diseases are underrepresented |
| **Explain its reasoning reliably** | Explanations are often post-hoc rationalizations, not actual reasoning |
| **Understand causation** | AI finds correlations, not causes — an important distinction for treatment decisions |
| **Be accountable** | Legal and ethical responsibility remains with the clinician |

> **Can you guess:**
>
> - If an AI system correctly identifies pneumonia on 98% of chest X-rays, does that mean it is safe to deploy?
> - *(Hint: consider what happens with the other 2%, and whether the training data represents your hospital's patient population)*

---

## Session 2: Lecture — Major AI Tools and Platforms (20 mins)

---

## Landscape of AI Tools for Healthcare Professionals

**Large language models (LLMs):**

| Tool | Developer | Key strength | Access |
|------|-----------|-------------|--------|
| **ChatGPT** | OpenAI | Widely known, plugins, image input | Free (GPT-4o mini) / paid |
| **Claude** | Anthropic | Long documents, careful reasoning | Free / paid |
| **Gemini** | Google | Integration with Google Workspace | Free / paid |
| **Copilot** | Microsoft | Embedded in Office 365 and Edge | Free / paid |
| **Perplexity** | Perplexity AI | Search with cited sources | Free / paid |

**Specialized healthcare AI tools:**

| Tool | Function | Example use |
|------|----------|-------------|
| **Consensus** | AI-powered academic search | Find research evidence with cited papers |
| **Elicit** | Research assistant | Extract data from papers for systematic reviews |
| **Glass AI** | Clinical decision support | Generate differential diagnoses from symptoms |
| **DAX Copilot** | Clinical documentation | Ambient listening for clinical notes (Nuance/Microsoft) |
| **FDA-cleared AI devices** | Diagnostic imaging | Over 950 FDA-authorized AI medical devices as of 2025 |

> **Can you guess:**
>
> - Why are there so many different AI tools instead of one tool that does everything?
> - *(Hint: think about the tradeoff between being general-purpose and being specialized for a specific task)*

---

## Session 3: Lecture — AI in Healthcare Timeline 2020-2026 (20 mins)

---

## Key Milestones

| Year | Milestone | Significance |
|------|-----------|-------------|
| **2020** | GPT-3 released | First LLM capable of generating coherent long text |
| **2021** | AlphaFold2 solves protein folding | AI achieves breakthrough in structural biology |
| **2022** | ChatGPT launched (Nov) | Public access to conversational AI — 100M users in 2 months |
| **2023** | GPT-4 passes USMLE | AI matches physician-level performance on medical exams |
| **2023** | Med-PaLM 2 (Google) | First AI to reach "expert" level on medical question-answering |
| **2024** | AI agents emerge | Systems that can plan, search, and execute multi-step tasks |
| **2024** | 882 FDA-authorized AI devices | Radiology dominates (>75%), cardiology second |
| **2025** | Claude, GPT-4o, Gemini 2 | Multimodal AI — text, image, audio, video in one model |
| **2025** | Ambient clinical documentation | DAX Copilot, Abridge deployed in major health systems |
| **2026** | Agentic AI in research | AI systems that autonomously search, analyze, and synthesize |

**Trend:** AI is moving from research curiosity to clinical deployment — but adoption is uneven, and most tools remain "assistive" rather than autonomous.

> **Can you guess:**
>
> - Which medical specialty has the most FDA-authorized AI devices, and why?
> - *(Hint: think about which specialty generates the most standardized digital images)*

---

## Session 4: Discussion — Healthcare AI Deployment Case Study (20 mins)

**Case: Epic Sepsis Model**

Epic Systems deployed a sepsis prediction model across hundreds of hospitals in the United States. A 2021 study (Wong et al., JAMA Internal Medicine) evaluated the model at 241 hospitals and found:

- **Sensitivity:** Only 7% of sepsis cases were identified by the model
- **Alert fatigue:** 18% of all hospitalized patients triggered an alert
- **Performance gap:** The model performed far worse in real-world deployment than in Epic's internal validation

**Discussion questions:**

1. Why might a model that works well in development fail in real-world deployment?
2. The model was trained on data from a limited set of hospitals. How does this affect generalizability?
3. With only 7% sensitivity, would you want this model running in your hospital? What sensitivity would be acceptable?
4. What should hospitals require from AI vendors before deploying a clinical prediction model?
5. How does this case change your view of AI marketing claims in healthcare?

> Wong A, Otles E, Donnelly JP, et al. External Validation of a Widely Implemented Proprietary Sepsis Prediction Model in Hospitalized Patients. JAMA Intern Med. 2021;181(8):1065-1070.

**Activity:** In small groups, draft a 5-point checklist that a hospital should use before deploying any AI clinical tool. Share with the class.

---

## Session 5: Wrap-up — Course Overview (10 mins)

**What this course covers (Weeks 1-8):**

| Week | Topic |
|------|-------|
| 1 | Introduction — The AI revolution in healthcare |
| 2 | How large language models work |
| 3 | Prompt engineering for healthcare |
| 4 | AI for literature review and research |
| 5 | AI for clinical decision support |
| 6 | AI in medical imaging |
| 7 | Evaluating AI — accuracy, bias, and hallucination |
| 8 | AI ethics, regulation, and governance |

**Course philosophy:**
- This is a **no-coding** course — you will use AI tools through their web interfaces
- Focus on **understanding, evaluating, and strategically applying** AI, not building it
- Every week includes hands-on practice with real AI tools
- Critical thinking is more important than technical knowledge

---

## Take-home Message

1. **AI in 2026 is powerful but limited** — it can summarize, detect patterns, and generate content, but it cannot replace clinical judgment, guarantee accuracy, or be held accountable
2. **The AI healthcare landscape is expanding rapidly** — from 0 to over 950 FDA-authorized AI devices in a decade, with LLMs now accessible to every clinician
3. **Healthy skepticism is essential** — real-world performance often falls short of marketing claims, as the Epic sepsis case demonstrates
