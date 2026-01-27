# Bronchiectasis Treatment Drugs - OLS Ontology IDs and Labels

This document provides ontology identifiers from the Ontology Lookup Service (OLS) for the drug entities mentioned in BRONCHIECTASIS_DRUGS.md.

## Drug Ontology Mappings

| **Drug Name** | **Primary Ontology ID** | **Ontology Label** | **Alternative IDs** |
|---|---|---|---|
| **Elexacaftor** | CHEBI:234518 | Elexacaftor | NCIT:C169935, SNOMED:827070004, DRON:00865534, MeSH:C000629074 |
| **Tezacaftor** | CHEBI:234517 | Tezacaftor | NCIT:C152581, SNOMED:771596001, DRON:00816343, MeSH:C000625213 |
| **Ivacaftor** | CHEBI:66901 | ivacaftor | NCIT:C166523, SNOMED:703823007, DRON:00020190, MeSH:C545203 |
| **Elexacaftor-tezacaftor-ivacaftor (ETI)** | MeSH:C000706587 | elexacaftor, ivacaftor, tezacaftor drug combination | SNOMED:827101002, DRON:00865544, DRON:00991316 |
| **Dupilumab** | NCIT:C162455 | Dupilumab | SNOMED:733487000, DRON:00904107, MeSH:C582203 |
| **Brensocatib (CHF-6333)** | NCIT:C171778 | Brensocatib | NCIT:C216798 (Brensocatib Monohydrate), MeSH:C000619932 |
| **Mucolytic (drug class)** | CHEBI:77034 | mucolytic | NCIT:C74536 (Mucolytic Agent), SNOMED:698759007 (Mucolytic drug therapy), SNOMED:773912002 (Mucolytic therapeutic role), MeSH:D005100 (Expectorants) |
| **N-acetylcysteine** | CHEBI:28939 | N-acetyl-L-cysteine | NCIT:C200 (Acetylcysteine), SNOMED:387440002, MeSH:D000111, MOD:00052, MI:0126 |
| **Trimethoprim-sulfamethoxazole** | CHEBI:3770 | co-trimoxazole | NCIT:C909, MeSH:D015662, ARO:3004024 |
| **Azithromycin** | CHEBI:2955 | Azithromycin | NCIT:C28844, SNOMED:387531004, MeSH:D017963, OMIT:0018219 |
| **Imipenem** | CHEBI:471744 | imipenem | NCIT:C570, SNOMED:46558003, MeSH:D015378, ARO:3000170, OMIT:0016147 |
| **Cilastatin** | CHEBI:3697 | cilastatin | NCIT:C61679, SNOMED:96058005, MeSH:D015377, ARO:3007063, OMIT:0016146 |
| **Imipenem-cilastatin** | CHEBI:5880 | Imipenem-cilastatin | NCIT:C2338 (Imipenem-Cilastatin Sodium), SNOMED:105212009, MeSH:D000077728, DRON:00731100 |
| **Sitafloxacin** | CHEBI:4304 | Sitafloxacin | NCIT:C76922, ARO:3003690, MeSH:C076246 |
| **Apigenin** | CHEBI:18388 | apigenin | NCIT:C68466, MeSH:D047310, OMIT:0023910, LIPIDMAPS:LMPK12110005 |
| **Bedaquiline** | CHEBI:72292 | bedaquiline | NCIT:C87658, SNOMED:714086004, ARO:3004492, MeSH:C493870 |
| **Triazole antifungals** | CHEBI:86426 | triazole antifungal agent | CHEBI:87101 (triazole antifungal drug), SNOMED:372632000, SNOMED:292823007 |
| **Aminoglycosides** | CHEBI:47779 | aminoglycoside | NCIT:C2363 (Aminoglycoside Antibiotic), SNOMED:763805006, MeSH:D000617 |
| **Rifamycins** | CHEBI:26580 | rifamycins | NCIT:C29406 (Rifamycin), SNOMED:768973004, MeSH:D012294, ARO:3000157, OMIT:0013204 |

## Drug Combination Products

| **Combination Product** | **Ontology ID** | **Label** | **Components** |
|---|---|---|---|
| Elexacaftor 100mg + Ivacaftor 75mg + Tezacaftor 50mg | DRON:00865924 | elexacaftor 100 MG / ivacaftor 75 MG / tezacaftor 50 MG Oral Tablet | Elexacaftor, Ivacaftor, Tezacaftor |
| Elexacaftor 50mg + Ivacaftor 37.5mg + Tezacaftor 25mg | DRON:00945522 | elexacaftor 50 MG / ivacaftor 37.5 MG / tezacaftor 25 MG Oral Tablet | Elexacaftor, Ivacaftor, Tezacaftor |
| Ivacaftor 150mg + Tezacaftor 100mg | SNOMED:1332199007 | Ivacaftor 150 mg and tezacaftor 100 mg oral tablet | Ivacaftor, Tezacaftor |
| Ivacaftor 75mg + Tezacaftor 50mg | SNOMED:1332200005 | Ivacaftor 75 mg and tezacaftor 50 mg oral tablet | Ivacaftor, Tezacaftor |
| Cilastatin 250mg + Imipenem 250mg | DRON:00777134 | cilastatin 250 MG / imipenem 250 MG Injection | Cilastatin, Imipenem |
| Cilastatin 500mg + Imipenem 500mg | DRON:00777137 | cilastatin 500 MG / imipenem 500 MG Injection | Cilastatin, Imipenem |

## Ontology Sources Used

- **CHEBI** (Chemical Entities of Biological Interest): Primary chemical compound ontology
- **NCIT** (NCI Thesaurus): Cancer and clinical terminology
- **SNOMED CT** (Systematized Nomenclature of Medicine): Clinical terminology
- **MeSH** (Medical Subject Headings): Biomedical vocabulary
- **DRON** (Drug Ontology): Drug products and their ingredients
- **ARO** (Antibiotic Resistance Ontology): Antibiotic mechanisms and resistance
- **OMIT** (Ontology for MicroRNA Target): Includes drug entities
- **LIPIDMAPS**: Lipid and small molecule database

## Drug Class Hierarchies

### CFTR Modulators
```
CHEBI:23888 (pharmaceutical) 
  └─ CFTR potentiator (ivacaftor)
  └─ CFTR corrector (elexacaftor, tezacaftor)
```

### Antibiotics
```
CHEBI:33281 (antibiotic)
  ├─ CHEBI:26790 (macrolide antibiotic)
  │   └─ CHEBI:2955 (Azithromycin)
  ├─ CHEBI:23066 (beta-lactam antibiotic)
  │   └─ CHEBI:471744 (imipenem)
  ├─ CHEBI:47779 (aminoglycoside)
  ├─ CHEBI:26580 (rifamycins)
  └─ CHEBI:24751 (fluoroquinolone)
      └─ CHEBI:4304 (Sitafloxacin)
```

### Antifungals
```
CHEBI:38068 (antifungal agent)
  └─ CHEBI:86426 (triazole antifungal agent)
      └─ CHEBI:87101 (triazole antifungal drug)
```

### Natural Products
```
CHEBI:26848 (tannin)
  └─ CHEBI:47916 (flavonoid)
      └─ CHEBI:18388 (apigenin)
```

## Notes on Ontology Mapping

1. **Multiple Identifiers**: Many drugs have multiple ontology identifiers across different databases, reflecting their use in various clinical and research contexts.

2. **Drug Combinations**: Combination products have distinct identifiers separate from their individual components.

3. **Salt Forms**: Different salt forms of the same drug (e.g., bedaquiline vs. bedaquiline fumarate) have different identifiers.

4. **Dose-Specific IDs**: DRON provides dose-specific identifiers for marketed drug products.

5. **Class Identifiers**: Drug classes (e.g., aminoglycosides, rifamycins) have their own identifiers distinct from individual members.

## Specific Ontology Details

### Brensocatib (CHF-6333)
- **NCIT:C171778**: Primary identifier
- **NCIT:C216798**: Brensocatib Monohydrate (specific salt form)
- **MeSH:C000619932**: MeSH supplementary concept
- **FDA Approval**: August 2025 as first disease-modifying therapy for bronchiectasis
- **Mechanism**: DPP-1 (dipeptidyl peptidase-1) inhibitor

### N-acetylcysteine (NAC)
- **CHEBI:28939**: N-acetyl-L-cysteine (specific stereoisomer)
- **MOD:00052**: Protein modification ontology term
- **MI:0126**: Molecular interactions database term
- **Multiple derivatives**: Over 10 different derivative compounds in CHEBI

### Dupilumab
- **Biologic**: Monoclonal antibody, not a small molecule
- **Target**: IL-4 and IL-13 receptor antagonist
- **DRON**: Multiple dose-specific formulations (150 mg/mL, 175 mg/mL, 200 mg/mL)

## Cross-References

For integration with `industry.owl`, these identifiers can be used to:
1. Link drug entities to standardized vocabularies
2. Enable semantic queries across multiple ontologies
3. Support interoperability with clinical databases
4. Facilitate drug-disease relationship modeling

---

**Document Created**: November 30, 2025  
**OLS Query Date**: November 30, 2025  
**Data Source**: Ontology Lookup Service (OLS4) via MCP  
**Related Files**: 
- BRONCHIECTASIS_DRUGS.md
- industry.owl
- BRONCHIECTASIS_GENES.md
