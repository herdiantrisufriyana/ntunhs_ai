# AI Agents and Workflow Automation

**Herdiantri Sufriyana**
Graduate Institute of Artificial Intelligence and Big Data in Healthcare
National Taiwan University of Nursing and Health Sciences

---

## Subtopics

- What are AI agents — from chatbots to autonomous workflows
- No-code and low-code AI tools for healthcare
- Designing multi-step AI workflows
- Hands-on: Building a simple AI-assisted healthcare workflow

---

## Session 1: Lecture — What Are AI Agents? (25 mins)

---

## From Chatbots to AI Agents

The evolution of AI systems follows a spectrum of increasing autonomy.

**Levels of AI autonomy:**

| Level | Type | What it does | Example |
|-------|------|-------------|---------|
| **1** | **Chatbot** | Responds to single questions; no memory across turns | FAQ bot on a hospital website |
| **2** | **Conversational AI** | Maintains context within a session; follows instructions | ChatGPT, Claude — answering medical questions in dialogue |
| **3** | **Tool-using AI** | Calls external tools (search, calculator, database) based on the conversation | AI assistant that searches PubMed and summarizes results |
| **4** | **AI Agent** | Plans multi-step tasks, uses tools, makes decisions, and iterates autonomously | AI that reviews patient records, identifies gaps, drafts care plans, and schedules follow-ups |
| **5** | **Multi-agent system** | Multiple AI agents collaborate, each with specialized roles | One agent extracts data from EHR, another reviews guidelines, a third drafts recommendations |

---

## What Makes an AI Agent Different?

An AI agent has three capabilities that distinguish it from a simple chatbot:

1. **Planning:** The agent breaks a complex goal into sub-tasks and determines execution order
2. **Tool use:** The agent can call external systems — databases, APIs, calculators, web searches
3. **Feedback loops:** The agent evaluates its own outputs and iterates until the goal is met

**Architecture of a healthcare AI agent:**

| Component | Function | Healthcare example |
|-----------|----------|-------------------|
| **Goal** | What the agent is trying to achieve | "Generate a prior authorization letter for this patient" |
| **Memory** | Information the agent retains across steps | Patient history, insurance requirements, previous denials |
| **Tools** | External capabilities the agent can invoke | EHR query, drug formulary lookup, letter template |
| **Reasoning** | How the agent decides what to do next | Check if medication requires prior auth → gather clinical justification → draft letter |

> **Can you guess:**
>
> - Why is a chatbot that answers "What is the dosage of metformin?" NOT an AI agent?
> - *(Hint: it responds to a single query without planning, tool use, or iteration — an agent would check the patient's renal function, current medications, and guidelines before recommending a specific dosage)*

---

## AI Agents in Healthcare Today (2025-2026)

**Current real-world applications:**

| Application | What the agent does | Organization |
|-------------|-------------------|--------------|
| **Prior authorization** | Extracts clinical data, matches to payer criteria, drafts authorization | Olive AI, Waystar |
| **Clinical trial matching** | Screens patient records against trial eligibility criteria | Tempus, Deep 6 AI |
| **Ambient clinical documentation** | Listens to patient-provider conversation, generates clinical notes | Nuance DAX Copilot, Abridge |
| **Medication reconciliation** | Compares medication lists across care settings, flags discrepancies | Various health systems piloting |
| **Scheduling optimization** | Balances patient preferences, provider availability, and urgency | Qventus |

> **Can you guess:**
>
> - Which of these applications involves the most steps and decisions? Why?
> - *(Hint: clinical trial matching requires reading inclusion/exclusion criteria, extracting patient data from multiple sources, and making complex eligibility determinations)*

---

## Session 2: Lecture — No-Code and Low-Code AI Tools (20 mins)

---

## No-Code and Low-Code AI for Healthcare

Not all AI workflows require programming. **No-code** and **low-code** platforms let healthcare professionals design AI workflows visually.

**Platform categories:**

| Category | What it does | Examples | Healthcare use |
|----------|-------------|---------|---------------|
| **AI workflow builders** | Drag-and-drop AI pipeline design | Zapier AI, Make (Integromat), n8n | Auto-triage patient messages, route referrals |
| **Custom GPTs / AI assistants** | Build specialized chatbots with custom knowledge | OpenAI GPT Builder, Claude Projects, Google Gems | Clinical guideline assistant, patient education bot |
| **Form + AI automation** | Connect forms to AI processing | Microsoft Power Automate, Google AppSheet | Auto-classify patient intake forms |
| **Document AI** | Extract structured data from documents | Google Document AI, Azure AI Document Intelligence | Extract data from scanned medical records |

**Key principle:** No-code does not mean no expertise. You still need:
- **Domain knowledge** to define what the AI should do
- **Data governance** to ensure patient data is handled appropriately
- **Validation** to verify the AI workflow produces correct results

---

## Choosing the Right Level of Automation

**Decision framework:**

| Question | If yes → | If no → |
|----------|----------|---------|
| Is the task repetitive and rule-based? | Automate fully | Consider AI augmentation |
| Does the task require clinical judgment? | AI drafts, human decides | AI may execute autonomously |
| Is patient safety at risk if the AI is wrong? | Human-in-the-loop required | Consider full automation with monitoring |
| Does the task involve protected health information? | Ensure HIPAA/local compliance | Standard data handling |

> **Can you guess:**
>
> - Should appointment reminder messages be fully automated or require human review?
> - *(Hint: standard reminders are low-risk and repetitive — good candidates for full automation; but reminders containing clinical information need more caution)*

---

## Session 3: Lecture — Designing Multi-Step AI Workflows (20 mins)

---

## Anatomy of a Multi-Step AI Workflow

A multi-step AI workflow chains together multiple actions where the output of one step becomes the input of the next.

**Example — automated patient intake workflow:**

| Step | Action | Tool/AI used | Output |
|------|--------|-------------|--------|
| 1 | Patient fills intake form online | Web form | Structured patient data |
| 2 | AI extracts key medical history | LLM with extraction prompt | Structured medical summary |
| 3 | AI checks for drug interactions | Drug interaction database API | Interaction alerts |
| 4 | AI generates pre-visit summary for provider | LLM with summarization prompt | Provider-facing summary |
| 5 | System sends confirmation to patient | Email/SMS automation | Patient confirmation |

**Design principles:**

1. **Define inputs and outputs** for each step before building
2. **Error handling:** What happens when a step fails? (e.g., AI cannot extract a medication name)
3. **Validation checkpoints:** Insert human review at high-risk steps
4. **Logging:** Record all AI decisions for audit and quality improvement
5. **Fallback paths:** When AI confidence is low, route to a human

---

## Common Workflow Patterns in Healthcare

| Pattern | Description | Example |
|---------|------------|---------|
| **Sequential** | Steps execute in order | Intake → extraction → summary |
| **Branching** | Different paths based on conditions | If high-risk → urgent review; if low-risk → standard processing |
| **Loop** | Repeat a step until criteria are met | Re-extract medication list until all entries are verified |
| **Parallel** | Multiple steps run simultaneously | Check drug interactions AND check allergy history at the same time |
| **Human-in-the-loop** | AI pauses for human approval before continuing | AI drafts referral letter → clinician reviews → system sends |

> **Can you guess:**
>
> - In the patient intake workflow above, which step should have a human-in-the-loop checkpoint?
> - *(Hint: Step 4 — the provider-facing summary could contain errors that affect clinical decisions; Steps 2-3 should also be validated periodically)*

---

## Session 4: Hands-on — Building a Simple AI-Assisted Healthcare Workflow (30 mins)

---

## Activity: Build a Multi-Step AI Workflow with Make

**Task:** Use [Make](https://www.make.com) (formerly Integromat) to build a multi-step AI workflow that automates a medication reconciliation task. Make is a free, no-code visual workflow builder with native modules for OpenAI, Claude (Anthropic), and Gemini — use whichever AI you prefer.

**Scenario:** A nurse receives a patient's medication list from a referral hospital. The list is in free-text format with abbreviations and inconsistencies. The goal is to produce a clean, verified medication reconciliation.

**Setup (5 mins):**

1. Go to [make.com](https://www.make.com) and sign up for a free account (Google login works)
2. Click **Create a scenario**
3. You will see the visual canvas where you connect modules (nodes) to build your workflow

**Build the workflow (15 mins):**

**Step 1 — Set variable:**

1. Click the **+** icon on the empty canvas
2. In the left sidebar, click **Built-in tools**. Select **Set variable**.
3. In the module settings: Variable name: `medication_list`. Variable value: `pt takes metformin 500 BID, lisinopril 10mg daily, atorvastatin 20 qhs, ASA 81mg daily, and insulin glargine 20u SC qhs. Also on PRN albuterol MDI 2 puffs q4-6h.`
4. Click **Save**
5. Right-click the module and select **Rename**. Name it `Input: Medication List`

**Step 2 — AI extracts and standardizes medications:**

1. Click the **+** icon on the Set variable module
2. In the left sidebar, click **AI by Make**. Under **Custom prompt**, select **Simple Text Prompt**.
3. In the module settings: Connection is already set to **Make's AI Provider (default)** — no API key needed. For Model, select **Small** (free) — this is a straightforward extraction task. In the Text field, type: `Extract the following free-text medication list into a structured table with columns: medication name, dose, frequency, route. Expand all abbreviations into full clinical terms. Input:` — then click inside the text field to open the output panel on the right. Under **Input: Medication List**, click **medication_list** to insert it.
4. Click **Save**
5. Right-click the module and select **Rename**. Name it `AI: Extract Medications`

**Step 3 — AI checks drug interactions:**

1. Click the **+** icon on the Step 2 module
2. Click **AI by Make** → **Simple Text Prompt** again
3. Connection: same as Step 2. For Model, select **Medium** (free) — interaction checking requires more complex reasoning. In the Text field, type: `Given this medication list, identify any potential drug-drug interactions. For each interaction, state the medications involved, the risk level, and the clinical recommendation.` — then click inside the text field to open the output panel. Under **AI: Extract Medications**, click **Answer** to insert the extracted medication table from Step 2.
4. Click **Save**
5. Right-click the module and select **Rename**. Name it `AI: Check Interactions`

**Step 4 — AI generates reconciliation document:**

1. Click the **+** icon on the Step 3 module
2. Click **AI by Make** → **Simple Text Prompt** again
3. Connection: same as Step 2. For Model, select **Medium** (free) — generating a clinical document requires synthesis across multiple inputs. In the Text field, type: `Using the structured medication list and the interaction check below, generate a clean medication reconciliation document suitable for a hospital admission record. Flag any interactions that require physician review. Medication list:` — then click inside the text field to open the output panel. Under **AI: Extract Medications**, click **Answer** to insert the medication table. Then type ` Interaction check:` and under **AI: Check Interactions**, click **Answer** to insert the interaction results.
4. Click **Save**
5. Right-click the module and select **Rename**. Name it `AI: Generate Reconciliation`

**Step 5 — Extract structured fields from reconciliation:**

1. Click the **+** icon on the Step 4 module
2. In the left sidebar, click **AI by Make**. Scroll down to **Text**, select **Extract information from text**.
3. In the module settings:
   - **Connection:** Already set to **Make's AI Provider (default)**
   - **Model:** Select **Small** (free) — this is a straightforward extraction task
   - **Text:** Click inside the field to open the output panel on the right. Under **AI: Generate Reconciliation**, click **Answer** to insert the reconciliation text from Step 4
4. Under **Information**, click **+ Add information** seven times, once for each field. Fill in each item:

| Name | Description | Type |
|------|------------|------|
| `medication_name` | The name of the medication | Text |
| `dose` | The numeric dose value of the medication | Number |
| `dose_unit` | The unit of the dose (e.g., mg, units, puffs) | Text |
| `frequency` | How often the medication is taken | Text |
| `route` | The route of administration | Text |
| `interaction_flag` | Whether this medication has a drug-drug interaction | Boolean |
| `interaction_detail` | Description of the interaction and clinical recommendation, if any | Text |

5. Click **Save**
6. Right-click the module and select **Rename**. Name it `Extract: Reconciliation Fields`

**Run the workflow:** Click **Run once** (bottom left) to execute all 5 steps in sequence. Compare Step 4's free-text output with Step 5's structured fields — this demonstrates why structured output matters in healthcare workflows.

**Evaluate the output (10 mins):**

5. Review the final medication reconciliation document:
   - Did the AI correctly identify all 6 medications?
   - Were the abbreviation expansions accurate? (BID = twice daily, qhs = every night at bedtime, PRN = as needed, SC = subcutaneous, MDI = metered-dose inhaler, q4-6h = every 4-6 hours)
   - Were the drug interaction checks reliable? (Verify against a reference like Medscape or Lexicomp)
   - Did the reconciliation document flag interactions appropriately?

6. Discuss with the class:
   - What would you change to make this workflow safe for real use?
   - Where would you add a human review checkpoint? (Hint: before the final reconciliation document is sent to the admission record)
   - What happens if the AI hallucinates an interaction that does not exist?
   - How does the Make free tier (1,000 operations/month, 2 active scenarios) affect real-world deployment?

> **Note:** The free Make account provides 1,000 operations per month. This 4-step workflow uses ~4 operations per run, so you have ~250 test runs — more than enough for this exercise.

---

## Session 5: Discussion — Risks and Governance of AI Agents (15 mins)

---

## Governance Challenges for AI Agents

As AI agents become more autonomous, governance becomes critical.

**Key risks:**

| Risk | Description | Mitigation |
|------|------------|------------|
| **Scope creep** | Agent takes actions beyond its intended purpose | Define strict boundaries and permissions |
| **Error propagation** | An error in step 1 cascades through all subsequent steps | Validate outputs at each step |
| **Accountability gap** | When an AI agent makes a harmful decision, who is responsible? | Clear human oversight assignment |
| **Data leakage** | Agent sends patient data to external AI services | Use on-premises or BAA-covered AI services |
| **Over-automation** | Automating tasks that require human judgment | Regular review of automation scope |

**Discussion questions:**
- Should AI agents be allowed to make any clinical decisions autonomously, even low-risk ones?
- How would you design an "off switch" for a healthcare AI agent that is mid-workflow?

---

## Take-home Message

1. **AI agents** go beyond chatbots by combining planning, tool use, and feedback loops — they can handle multi-step healthcare tasks like prior authorization, clinical trial matching, and documentation
2. **No-code and low-code tools** make AI workflow design accessible to healthcare professionals without programming skills — but domain expertise and validation remain essential
3. **Multi-step AI workflows** require careful design with error handling, validation checkpoints, and human-in-the-loop at high-risk steps
4. **Governance** is the key challenge — as AI agents become more autonomous, clear accountability, boundaries, and oversight mechanisms must be in place
