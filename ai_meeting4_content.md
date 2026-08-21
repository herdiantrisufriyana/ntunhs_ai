# AI for Literature Review and Research

**Herdiantri Sufriyana**
Graduate Institute of Artificial Intelligence and Big Data in Healthcare
National Taiwan University of Nursing and Health Sciences

---

## Subtopics

- AI-powered search and summarization tools
- AI-assisted systematic reviews
- Evaluating AI-generated summaries
- Hands-on: Using AI to search and synthesize research papers

---

## Session 1: Lecture — AI-Powered Search and Summarization Tools (25 mins)

---

## The Research Information Overload Problem

- PubMed contains over **37 million** citations as of 2026
- Over **1.8 million** new biomedical articles are published per year
- A systematic review can take **12-18 months** using traditional methods
- No human can keep up with the evidence — AI can help, but with caveats

---

## AI Tools for Literature Search and Summarization

| Tool | What it does | Strength | Limitation |
|------|-------------|----------|-----------|
| **PubMed** | Traditional keyword/MeSH search | Gold standard database, comprehensive | Requires manual search strategy design |
| **Consensus** | AI-powered search over peer-reviewed papers | Shows agreement/disagreement across studies | Limited to indexed papers |
| **Elicit** | Research assistant — extracts data from papers | Structured extraction, identifies study design | May miss nuanced findings |
| **Semantic Scholar** | AI-ranked academic search | Finds conceptually related papers beyond keywords | Covers CS and biomedical, not all journals |
| **Perplexity** | Search + AI synthesis with citations | Real-time web search with source links | Sources may include non-peer-reviewed content |
| **ChatGPT/Claude** | General-purpose summarization | Flexible, can follow complex instructions | No direct database access, hallucination risk |
| **Scite** | Citation analysis — shows supporting/contrasting citations | Reveals how a paper has been received | Requires subscription for full features |

---

## How AI Search Differs from Traditional Search

| Feature | Traditional (PubMed) | AI-powered (Consensus, Elicit) |
|---------|---------------------|-------------------------------|
| **Query format** | Boolean operators, MeSH terms | Natural language questions |
| **Results** | List of papers matching keywords | Synthesized answer with cited papers |
| **Ranking** | By date or relevance score | By semantic similarity to question |
| **Extraction** | Manual reading | Automated extraction of key findings |
| **Reproducibility** | Fully reproducible search strategy | Less transparent — different sessions may give different results |

> **Can you guess:**
>
> - Why might a systematic review still require PubMed even if AI tools exist?
> - *(Hint: systematic reviews require reproducible, comprehensive searches — AI tools may miss papers and cannot guarantee reproducibility)*

---

## Session 2: Lecture — AI-Assisted Systematic Reviews (20 mins)

---

## The Systematic Review Pipeline

A systematic review follows a structured process. AI can assist at multiple stages:

| Stage | Traditional approach | AI-assisted approach |
|-------|---------------------|---------------------|
| **1. Formulate question** | PICO framework | LLM helps refine PICO, suggests search terms |
| **2. Search strategy** | Boolean queries in PubMed, Embase, Cochrane | AI suggests MeSH terms and synonyms |
| **3. Screening** | Two reviewers read titles/abstracts | AI pre-screens and ranks by relevance |
| **4. Data extraction** | Manual reading and form filling | AI extracts study design, sample size, outcomes |
| **5. Quality assessment** | Cochrane RoB, PROBAST, etc. | AI drafts initial assessments for human review |
| **6. Synthesis** | Meta-analysis, narrative synthesis | AI summarizes findings across studies |
| **7. Writing** | Manual drafting | AI drafts sections for human editing |

**Key principle:** AI assists but does not replace the researcher. Every AI output must be verified by a human expert.

---

## Risks of AI in Systematic Reviews

| Risk | Example | Mitigation |
|------|---------|-----------|
| **Incomplete search** | AI tool does not cover all databases | Always search PubMed, Embase, and Cochrane independently |
| **Screening errors** | AI incorrectly excludes a relevant paper | Human must review AI exclusions |
| **Extraction errors** | AI misreads a confidence interval or p-value | Double-check extracted numbers against original paper |
| **Hallucinated data** | AI invents a result not in the paper | Always verify against the source PDF |
| **Reproducibility** | AI tools may give different results on different days | Document the tool, version, and date used |

> **Can you guess:**
>
> - If an AI tool pre-screens 5,000 abstracts and excludes 4,000 as irrelevant, how would you verify the exclusions are correct?
> - *(Hint: sample-check a random subset of excluded papers — if more than a few are actually relevant, the AI screening is unreliable)*

---

## Session 3: Lecture — Evaluating AI-Generated Summaries (20 mins)

---

## How to Assess AI Summary Quality

When an AI tool summarizes research, evaluate using these criteria:

| Criterion | What to check | Red flag |
|-----------|--------------|----------|
| **Accuracy** | Do the stated findings match the original papers? | Numbers, effect sizes, or conclusions that differ from the source |
| **Completeness** | Are important studies or findings missing? | AI may cherry-pick studies that fit a narrative |
| **Citation validity** | Do the cited papers actually exist? | Fabricated references with plausible-looking titles |
| **Recency** | Are the most current guidelines and studies included? | AI may rely on outdated evidence |
| **Nuance** | Does the summary acknowledge conflicting evidence? | Oversimplified "X is effective" without mentioning limitations |
| **Bias** | Does the summary favor one conclusion without justification? | Systematic tendency to recommend certain treatments |

**Verification workflow:**

1. Read the AI summary
2. Pick 3-5 cited references and verify they exist (search by title in PubMed or Google Scholar)
3. For 2-3 key claims, read the original paper abstract to confirm the AI accurately represents the findings
4. Check whether the summary mentions limitations or conflicting evidence
5. Compare with your own knowledge of the topic

> **Can you guess:**
>
> - If every citation in an AI summary is real but the conclusions are wrong, what went wrong?
> - *(Hint: the AI may have correctly cited papers but misinterpreted or selectively quoted their findings)*

---

## Session 4: Hands-on — Using AI to Search and Synthesize Research (25 mins)

**Task:** Use AI tools to research a clinical question and evaluate the output quality.

**Clinical question:** "What is the evidence for using AI-based tools to detect diabetic retinopathy in primary care settings?"

**Part A: Consensus search (10 mins)**

1. Go to [consensus.app](https://consensus.app)
2. Enter the clinical question as a natural language query
3. Review the results:
   - How many studies does it find?
   - Does it show a "consensus meter" (agreement/disagreement)?
   - Pick 2 cited papers — verify they exist in PubMed
4. Record: Are the findings accurately represented?

**Part B: LLM synthesis (10 mins)**

1. Open an LLM (ChatGPT, Claude, or Gemini)
2. Use this prompt:
   "Summarize the evidence from peer-reviewed studies published after 2020 on using AI tools for diabetic retinopathy screening in primary care. Include: (1) sensitivity and specificity of major AI systems, (2) FDA clearance status, (3) implementation challenges. Cite specific studies with authors, year, and journal."
3. Evaluate the response:

| Check | Result |
|-------|--------|
| Are specific studies cited? | |
| Do the cited studies exist? (Verify 2-3 in PubMed) | |
| Are sensitivity/specificity numbers accurate? | |
| Are FDA-cleared devices correctly identified? | |
| Does it mention implementation challenges? | |

**Part C: Comparison (5 mins)**

4. Compare the Consensus and LLM outputs:
   - Which provided more reliable citations?
   - Which gave a more nuanced synthesis?
   - Which would you trust more for a systematic review?

**Class discussion:** Share findings. Did anyone find a hallucinated citation?

---

## Take-home Message

1. **AI tools can dramatically accelerate literature search and synthesis** — but they cannot replace rigorous systematic review methodology or human verification
2. **Different tools have different strengths** — use specialized tools (Consensus, Elicit) for finding real papers, and LLMs for synthesizing and structuring information
3. **Always verify AI outputs** — check that citations exist, findings are accurately represented, and conflicting evidence is not omitted
