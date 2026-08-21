# AI for Precision Medicine and Genomics

**Herdiantri Sufriyana**
Graduate Institute of Artificial Intelligence and Big Data in Healthcare
National Taiwan University of Nursing and Health Sciences

---

## Subtopics

- AI in genomic analysis and biomarker discovery
- Personalized treatment recommendations
- Multi-omics data integration
- Case study: Recent AI-driven precision medicine publications

---

## Session 1: Lecture — Precision Medicine and AI (20 mins)

---

## What is Precision Medicine?

**Precision medicine** tailors medical treatment to the individual characteristics of each patient — moving from "one-size-fits-all" to targeted interventions based on a patient's genetic, environmental, and lifestyle factors.

**How precision medicine differs from traditional medicine:**

| Aspect | Traditional medicine | Precision medicine |
|--------|---------------------|-------------------|
| **Treatment selection** | Based on disease diagnosis | Based on molecular profile + diagnosis |
| **Drug dosing** | Standard dose for all patients | Pharmacogenomics-guided dosing |
| **Prevention** | Population-level screening | Risk-stratified screening based on genetics |
| **Outcome prediction** | Based on clinical staging | Integrated molecular and clinical prediction |

**Why AI is essential for precision medicine:**
- The human genome has ~3 billion base pairs and ~20,000 protein-coding genes
- A single tumor may have thousands of mutations — identifying which ones drive disease requires computational analysis
- Multi-omics datasets combine genomics, transcriptomics, proteomics, and metabolomics — too complex for manual interpretation

> **Can you guess:**
>
> - Why did precision medicine become feasible only in the last 15 years?
> - *(Hint: the cost of sequencing a human genome dropped from USD 100 million in 2001 to under USD 200 in 2024, and computing power scaled exponentially)*

---

## Session 2: Lecture — AI in Genomic Analysis and Biomarker Discovery (25 mins)

---

## How AI Analyzes Genomic Data

**Key AI applications in genomics:**

| Application | What AI does | Input data | Output |
|-------------|-------------|-----------|--------|
| **Variant calling** | Identifies genetic mutations from sequencing data | Raw DNA sequences | List of variants (SNPs, indels, structural variants) |
| **Variant classification** | Determines if a variant is pathogenic or benign | Variant information + population databases | Pathogenicity score |
| **Gene expression analysis** | Identifies differentially expressed genes | RNA sequencing data | Gene signatures |
| **Biomarker discovery** | Finds molecular markers that predict disease or treatment response | Multi-omics data | Candidate biomarkers |

---

## AI for Biomarker Discovery

**Biomarkers** are measurable indicators of biological processes, disease states, or treatment responses.

**Types of biomarkers AI can discover:**

| Biomarker type | Purpose | Example |
|---------------|---------|---------|
| **Diagnostic** | Detect disease presence | Circulating tumor DNA for cancer detection |
| **Prognostic** | Predict disease outcome | Gene expression signature predicting breast cancer recurrence |
| **Predictive** | Predict treatment response | HER2 status predicting response to trastuzumab |
| **Monitoring** | Track disease progression | PSA levels in prostate cancer surveillance |

**AI approaches for biomarker discovery:**

1. **Supervised learning:** Train models to predict outcomes, then identify which molecular features the model relies on (feature importance, SHAP values)
2. **Unsupervised learning:** Cluster patients by molecular profiles to discover subtypes with different outcomes
3. **Network analysis:** Build gene interaction networks and identify key hub genes
4. **Deep learning on sequences:** Convolutional or transformer models that learn patterns directly from raw sequences

> **Can you guess:**
>
> - From previous meetings, which ML concept is most directly related to biomarker discovery — feature selection or model evaluation?
> - *(Hint: biomarker discovery is essentially feature selection at the molecular level — identifying which molecular measurements are most informative for the clinical question)*

---

## Real-World Examples of AI in Genomics

**Foundation Medicine (Roche):**
- Comprehensive genomic profiling: sequences 300+ cancer-related genes
- AI classifies variants and matches patients to targeted therapies and clinical trials
- Used by oncologists worldwide for treatment decisions

**DeepVariant (Google):**
- Deep learning model for variant calling from sequencing data
- Outperformed traditional bioinformatics tools in the FDA PrecisionFDA Truth Challenge
- Open-source, freely available

**Tempus:**
- AI platform that integrates genomic, clinical, and imaging data
- Identifies biomarkers and matches patients to clinical trials
- Used by over 50% of US academic medical centers

---

## Session 3: Lecture — Personalized Treatment and Multi-Omics Integration (25 mins)

---

## AI for Personalized Treatment Recommendations

**How AI enables treatment personalization:**

| Approach | How it works | Clinical impact |
|----------|-------------|----------------|
| **Pharmacogenomics** | AI predicts drug metabolism based on genetic variants (CYP450 enzymes) | Dose adjustment for warfarin, clopidogrel, codeine |
| **Tumor molecular profiling** | AI identifies actionable mutations and matches to targeted therapies | Targeted therapy selection in oncology |
| **Treatment response prediction** | ML models predict which patients will respond to specific treatments | Avoiding ineffective treatments, reducing side effects |
| **Combination therapy optimization** | AI explores drug combination space to find synergistic pairs | Optimizing cancer treatment regimens |

**Example — pharmacogenomics in practice:**

A patient prescribed codeine for pain relief:
1. Genomic test reveals **CYP2D6 ultra-rapid metabolizer** status
2. AI system flags: codeine is converted to morphine too quickly → risk of respiratory depression
3. Recommendation: use alternative analgesic (e.g., acetaminophen, NSAID)
4. Without this information: patient could experience a life-threatening adverse event

> **Can you guess:**
>
> - If two patients with the same cancer type and stage receive the same chemotherapy, but one responds and the other does not — what might explain the difference?
> - *(Hint: different molecular subtypes — same clinical diagnosis can have different underlying biology that AI can help distinguish)*

---

## Multi-Omics Data Integration

**"Omics" layers and what they measure:**

| Omics layer | What it measures | Data type |
|-------------|-----------------|-----------|
| **Genomics** | DNA sequence and variants | Mutations, copy number variations |
| **Transcriptomics** | Gene expression (RNA levels) | Which genes are active and at what level |
| **Proteomics** | Protein abundance and modifications | Which proteins are present and functional |
| **Metabolomics** | Small molecule metabolites | Products of cellular metabolism |
| **Epigenomics** | DNA methylation and histone modifications | Gene regulation without sequence changes |

**Why integrate multiple omics layers?**
- DNA mutations do not always translate to protein changes (gene regulation)
- Gene expression does not always reflect protein activity (post-translational modifications)
- Each layer captures a different aspect of biology — integration provides a more complete picture

**AI methods for multi-omics integration:**

| Method | How it works | Strength |
|--------|-------------|----------|
| **Early integration** | Concatenate all omics features into one dataset, then train model | Simple; captures cross-omics interactions |
| **Late integration** | Train separate models per omics layer, combine predictions | Handles different data types well |
| **Intermediate integration** | Learn shared representations across omics layers using autoencoders or attention | Best performance; most complex |

> **Can you guess:**
>
> - With 20,000 genes, 10,000 proteins, and 5,000 metabolites as features, and only 200 patient samples — what is the biggest risk?
> - *(Hint: extreme overfitting — far more features than samples; dimensionality reduction and feature selection are critical)*

---

## Session 4: Hands-on — Exploring Precision Medicine AI Tools (25 mins)

---

## Activity: Exploring AI-Powered Precision Medicine Resources

**Task:** Explore publicly available precision medicine AI tools and databases to understand how AI translates genomic data into clinical decisions.

**Steps:**

1. **ClinVar — variant interpretation database:**
   - Go to [https://www.ncbi.nlm.nih.gov/clinvar/](https://www.ncbi.nlm.nih.gov/clinvar/)
   - Search for "BRCA1" — explore the list of variants and their clinical significance classifications (pathogenic, likely pathogenic, uncertain significance, benign)
   - Note: AI and ML models are increasingly used to classify variants of uncertain significance (VUS)

2. **OncoKB — precision oncology knowledge base:**
   - Go to [https://www.oncokb.org/](https://www.oncokb.org/)
   - Search for "BRAF V600E" — this is a common mutation in melanoma
   - Review the therapeutic implications: which targeted therapies are recommended?
   - Note: OncoKB integrates AI-curated evidence with expert oncologist review

3. **PharmGKB — pharmacogenomics database:**
   - Go to [https://www.pharmgkb.org/](https://www.pharmgkb.org/)
   - Search for "warfarin" — explore how genetic variants affect warfarin dosing
   - Review the clinical guideline: how does CYP2C9 genotype influence recommended dose?

4. **Discussion exercise:** For each resource, answer:
   - How does AI/ML contribute to this database or tool?
   - What is the role of human experts in validating AI outputs?
   - How would a clinician use this information at the point of care?

---

## Session 5: Case Study — Recent AI-Driven Precision Medicine (15 mins)

---

## Case Study: AI-Driven Precision Medicine Breakthroughs

**Case A — AlphaFold and drug target discovery:**
- DeepMind's AlphaFold predicted the 3D structure of virtually all known proteins (200+ million structures)
- Impact: researchers can now identify drug binding sites computationally, without expensive X-ray crystallography
- AlphaFold3 (2024) extended to protein-ligand, protein-DNA, and protein-RNA complexes
- This accelerates drug target validation from months to hours

**Case B — Liquid biopsy with AI analysis:**
- Companies like Grail (Galleri test) use AI to analyze cell-free DNA in blood samples
- Multi-cancer early detection: a single blood test screens for 50+ cancer types
- AI identifies cancer-specific methylation patterns in circulating DNA fragments
- FDA-approved pathway for clinical use; large-scale validation studies ongoing

**Case C — AI for rare disease diagnosis:**
- Face2Gene (FDNA) uses facial recognition AI to help diagnose rare genetic syndromes
- Trained on photos of patients with known genetic conditions
- Assists geneticists in identifying conditions they may not have encountered before
- Particularly valuable in regions with limited access to genetic specialists

**Discussion:**
- Which of these cases has the most immediate impact on patient care?
- What ethical concerns arise from using AI facial recognition for genetic diagnosis?
- How should we handle the uncertainty when AI suggests a diagnosis for a rare disease?

---

## Take-home Message

1. **Precision medicine** uses molecular data to tailor treatment to individual patients — AI is essential because the data complexity (billions of base pairs, thousands of genes) exceeds human analytical capacity
2. **AI discovers biomarkers** by identifying which molecular features predict disease outcomes or treatment response — this is feature selection at the molecular level
3. **Multi-omics integration** combines genomics, transcriptomics, proteomics, and metabolomics for a comprehensive biological picture — AI methods handle the complexity of merging different data types
4. **Clinical translation** requires rigorous validation — AI predictions must be confirmed through clinical studies before they can guide patient care decisions
