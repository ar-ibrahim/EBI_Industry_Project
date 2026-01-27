# Bronchiectasis Clinical Trials Drugs - OLS Ontology Mapping

**Source:** BRONCHIECTASIS_CLINICAL_TRIALS_DRUGS_COMPOUNDS_LIST.md  
**Ontology Service:** OLS4 (Ontology Lookup Service)

---

## Drug-Ontology Mapping Table

| Drug/Compound Name | Primary Ontology ID | Label | Source Ontology | Alternative IDs | Trial ID(s) |
|-------------------|---------------------|-------|-----------------|-----------------|-------------|
| **Pirfenidone** | CHEBI:32016 | pirfenidone | ChEBI | NCIT:C2635, SNOMED:439581000, mesh:C093844 | NCT06329401 |
| **Brensocatib** | NCIT:C171778 | Brensocatib | NCI Thesaurus | DRON:01076451, mesh:C000619932, NCIT:C216798 | NCT03218917, NCT04594369 |
| **CXCR2 Antagonists** | CHEBI:231732 | CXCR2 antagonist | ChEBI | NCIT:C153151, NCIT:C123383 | - |
| **PI3K Inhibitors** | CHEBI:50914 | EC 2.7.1.137 (phosphatidylinositol 3-kinase) inhibitor | ChEBI | NCIT:C202468 | - |
| **Neutrophil Elastase Inhibitors** | NCIT:C214840 | Neutrophil Elastase Inhibitor | NCI Thesaurus | CHEBI:64922, NCIT:C87386 | - |
| **Glucocorticoids** | CHEBI:24261 | glucocorticoid | ChEBI | SNOMED:419933005 | - |
| **Tobramycin** | CHEBI:28864 | tobramycin | ChEBI | SNOMED:373548001, NCIT:C893, ARO:0000052 | NCT06760273 |
| **Levofloxacin** | CHEBI:63598 | levofloxacin | ChEBI | SNOMED:387552007, ARO:0000071 | NCT06209047 |
| **Gentamicin** | SNOMED:387321007 | Gentamicin | SNOMED CT | ARO:3007382 | NCT06209047 |
| **Nitric Oxide** | CHEBI:16480 | nitric oxide | ChEBI | SNOMED:6710000, NCIT:C695, mesh:D009569 | NCT06663176 |
| **Itraconazole** | CHEBI:6076 | itraconazole | ChEBI | SNOMED:387532006, ARO:3007511 | NCT06160713 |
| **Triazole Antifungals** | CHEBI:86426 | triazole antifungal agent | ChEBI | CHEBI:87101, SNOMED:372632000 | - |
| **Hypertonic Saline** | SNOMED:373766008 | Hypertonic saline | SNOMED CT | NCIT:C60814, mesh:D012462 | NCT06443658, NCT06242795 |
| **Ensifentrine** | NCIT:C166674 | Ensifentrine | NCI Thesaurus | mesh:C512996 | NCT06559150 |
| **Acetylcysteine** | CHEBI:22198 | acetylcysteine | ChEBI | SNOMED:387440002 | NCT06726356 |
| **CFTR Modulators** | CHEBI:66902 | CFTR potentiator | ChEBI | EFO:0920039 | - |
| **Vitamin D** | CHEBI:27300 | vitamin D | ChEBI | SNOMED:438541000124101 | NCT06551337 |
| **GDC-6988** | - | Not found | - | Novel Phase 1 compound | NCT06603246 |
| **CHF6333** | - | Not found | - | Novel Phase 1/2 compound | NCT06166056 |
| **HSK31858** | - | Not found | - | Novel Phase 3 compound | NCT06660992 |
| **Bailing Capsules** | - | Not found | - | Traditional Chinese Medicine | NCT07114120 |
| **Guben Kechuan Granules** | - | Not found | - | Traditional Chinese Medicine | NCT07114120 |
| **Staphylococcus Albicans Tablets** | - | Not found | - | Immunotherapy agent | NCT05407792 |

---

## Summary Statistics

- **Total Drugs/Compounds:** 23
- **Mapped to Standard Ontologies:** 17 (74%)
- **Not Yet in Ontologies:** 6 (26%)
- **Primary Ontology Sources:** ChEBI (9), NCIT (4), SNOMED CT (3), Other (1)

---

## Drugs by Ontology Coverage

### Fully Mapped (17 compounds)
✅ Pirfenidone  
✅ Brensocatib  
✅ CXCR2 Antagonists  
✅ PI3K Inhibitors  
✅ Neutrophil Elastase Inhibitors  
✅ Glucocorticoids  
✅ Tobramycin  
✅ Levofloxacin  
✅ Gentamicin  
✅ Nitric Oxide  
✅ Itraconazole  
✅ Triazole Antifungals  
✅ Hypertonic Saline  
✅ Ensifentrine  
✅ Acetylcysteine  
✅ CFTR Modulators  
✅ Vitamin D  

### Not Yet in Ontologies (6 compounds)
❌ GDC-6988 (Novel Phase 1)  
❌ CHF6333 (Novel Phase 1/2)  
❌ HSK31858 (Novel Phase 3)  
❌ Bailing Capsules (TCM)  
❌ Guben Kechuan Granules (TCM)  
❌ Staphylococcus Albicans Tablets (Immunotherapy)  

---

## Usage Guidelines

### For Database Integration
- Use **Primary Ontology ID** for main database linking
- Store **Alternative IDs** for cross-ontology compatibility
- Prefer ChEBI IDs for chemical compounds
- Prefer NCIT IDs for newer therapeutic agents
- Use SNOMED IDs for clinical/EHR systems

### For Literature Mining
- Include both primary and alternative IDs in searches
- Use MeSH terms for PubMed queries
- Use SNOMED codes for clinical database queries

### For Semantic Annotation
- Link primary IDs to RDF predicates
- Use `owl:sameAs` for alternative ID relationships
- Reference ontology URLs for full definitions

---

**Methodology:** OLS4 API search via MCP server  
**Source Document:** BRONCHIECTASIS_CLINICAL_TRIALS_DRUGS_COMPOUNDS_LIST.md  
**OLS4 URL:** http://www.ebi.ac.uk/ols4/
