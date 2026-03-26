# Thrombotic Microangiopathy - Curation Summary

## Metadata
- **Disease term**: MONDO:0019737 (thrombotic microangiopathy)
- **Category**: Complex

---

## Disease Relationships

### Parents
- Microangiopathy
- Thrombotic Disease (MONDO:0000831)

### Subtypes (4)

1. **Thrombotic Thrombocytopenic Purpura (TTP)**: Caused by severe ADAMTS13 deficiency (immune-mediated or congenital Upshaw-Schulman syndrome)
2. **Hemolytic Uremic Syndrome (HUS)**: STEC-HUS (Shiga toxin-triggered) or atypical HUS (complement dysregulation)
3. **Drug-induced Thrombotic Microangiopathy**: Triggered by quinine, calcineurin inhibitors, VEGF inhibitors, platinum compounds, gemcitabine
4. **Secondary Thrombotic Microangiopathy**: Associated with malignant hypertension, pregnancy complications, SLE, antiphospholipid syndrome, HSCT

### Subtype Ontology Mappings

| Subtype | MONDO Term | Classification | Notes |
|---------|-----------|----------------|-------|
| Thrombotic Thrombocytopenic Purpura | `MONDO:0018896` | `mondo_nested_subclass` | TTP is formally a MONDO subclass of TMA |
| Hemolytic Uremic Syndrome | `MONDO:0001549` | `clinical_phenotype` | HUS has its own MONDO term but is not formally classified under TMA in MONDO |
| Drug-induced TMA | — | `clinical_phenotype` | No specific MONDO term exists |
| Secondary TMA | — | `clinical_phenotype` | No specific MONDO term exists |

---

## Pathophysiology (7 nodes)

1. **Endothelial Cell Injury and Activation**
   - Initiating event across all TMA subtypes
   - Exposes subendothelial matrix, triggers VWF release, activates coagulation
   - Cell types: endothelial cell (CL:0000115)
   - Processes: endothelial cell activation (GO:0042118, ↑), blood coagulation (GO:0007596, ↑)
   - Evidence: PMID:28416508

2. **ADAMTS13 Deficiency and Ultra-Large VWF Multimers**
   - TTP-specific mechanism
   - Prevents cleavage of UL-VWF, causing platelet-rich microthrombi
   - Cell types: endothelial cell (CL:0000115)
   - Processes: VWF cleavage (GO:0002576, ↓)
   - Evidence: PMID:11586351, PMID:30625070, PMID:12660343

3. **Complement Alternative Pathway Dysregulation**
   - aHUS-specific mechanism
   - Mutations in CFH, CFI, MCP/CD46 or anti-CFH autoantibodies
   - Cell types: glomerular endothelial cell (CL:0002188)
   - Evidence: PMID:23738544, PMID:28416508

4. **Shiga Toxin-Mediated Endothelial Injury**
   - STEC-HUS mechanism
   - Stx binds Gb3 receptors on renal endothelial cells
   - Cell types: glomerular endothelial cell (CL:0002188)
   - Evidence: PMID:28416508

5. **Platelet Aggregation and Microvascular Thrombosis**
   - Universal downstream mechanism
   - Platelet-rich thrombi cause ischemia and mechanical erythrocyte destruction
   - Cell types: platelet (CL:0000233)
   - Evidence: PMID:28416508, PMID:30625070

6. **Microangiopathic Hemolytic Anemia**
   - Mechanical shear-induced RBC fragmentation
   - Produces schistocytes, elevated LDH, low haptoglobin
   - Evidence: PMID:12660343, PMID:28416508

7. **Organ Ischemia and End-Organ Damage**
   - TTP: neurological involvement (confusion, seizures, stroke)
   - HUS: renal involvement (acute kidney injury)
   - Cell types: glomerular endothelial cell (CL:0002188)
   - Evidence: PMID:30625070, PMID:28416508

---

## Phenotypes (6 total)

### Clinical (4)
1. **Microangiopathic Hemolytic Anemia**: Schistocytes on smear, elevated LDH, negative Coombs — HP:0001937
2. **Thrombocytopenia**: Consumptive, typically <30,000/μL in TTP — HP:0001873
3. **Acute Kidney Injury**: Predominant in HUS, may require dialysis — HP:0001919
4. **Neurological Manifestations**: Confusion, seizures, coma in TTP — HP:0001250

### Laboratory (2)
1. **Elevated Lactate Dehydrogenase**: Often >1000 U/L in active TTP — HP:0025435
2. **Schistocytes on Peripheral Blood Smear**: Diagnostic hallmark — HP:0001981

---

## Treatments (4)

| Treatment | MAXO Term | Therapeutic Agents | Notes |
|-----------|-----------|-------------------|-------|
| Plasma Exchange Therapy | MAXO:0000950 (supportive care) | — | Cornerstone of TTP; reduces mortality >90% → ~10-20% |
| Caplacizumab | MAXO:0000058 (pharmacotherapy) | NCIT:C128625 (Caplacizumab) | Anti-VWF nanobody; adjunct to TPE in acquired TTP |
| Immunosuppression | MAXO:0000058 (pharmacotherapy) | CHEBI:50858 (corticosteroid), NCIT:C1702 (Rituximab) | Suppresses anti-ADAMTS13 autoantibodies in immune TTP |
| Eculizumab and Ravulizumab | MAXO:0000058 (pharmacotherapy) | NCIT:C48386 (Eculizumab), NCIT:C124657 (Ravulizumab) | Terminal complement C5 inhibitors; transformed aHUS outcomes |

---

## Genetic Associations (9 genes)

| Gene | HGNC ID | OGG ID | Association | Subtype | Inheritance |
|------|---------|--------|-------------|---------|-------------|
| ADAMTS13 | HGNC:1366 | OGG:3000011093 | Causative | TTP | Autosomal Recessive |
| CFH | HGNC:4883 | OGG:3000003075 | Causative | aHUS | AD / AR |
| CFI | HGNC:5394 | OGG:3000003426 | Causative | aHUS | Autosomal Dominant |
| CD46 (MCP) | HGNC:6953 | OGG:3000004179 | Causative | aHUS | Autosomal Dominant |
| CFB | HGNC:1037 | OGG:3000000629 | Causative | aHUS | Autosomal Dominant |
| C3 | HGNC:1318 | OGG:3000000718 | Causative | aHUS | Autosomal Dominant |
| THBD | HGNC:11784 | OGG:3000007056 | Causative | aHUS | Autosomal Dominant |
| DGKE | HGNC:2852 | OGG:3000008526 | Causative | aHUS | Autosomal Recessive |
| VWF | HGNC:12726 | OGG:3000007450 | Modifier | TTP | — |

**Notes:**
- ADAMTS13: biallelic LoF → congenital TTP (Upshaw-Schulman); autoantibodies → acquired TTP
- CFH: most common aHUS gene (~20-30% of cases); anti-CFH autoantibodies produce acquired phenocopy
- DGKE: complement-independent aHUS; eculizumab typically less effective
- VWF: directly cleaved by ADAMTS13; UL-VWF multimers are the pathogenic species in TTP

---

## Clinical Trials (6)

| NCT | Phase | Status | Drug | Therapeutic Agent ID | Target |
|-----|-------|--------|------|---------------------|--------|
| NCT02553317 (HERCULES) | Phase III | Completed | Caplacizumab | NCIT:C128625 | TTP |
| NCT03922308 | Phase II | Completed | Recombinant ADAMTS13 (apadamtase alfa) | NCIT:C169784 | TTP |
| NCT06831058 | Phase II | Recruiting | Efgartigimod (FcRn inhibitor) | NCIT:C171817 | Immune TTP |
| NCT04889430 | Phase III | Active, not recruiting | Iptacopan (factor B inhibitor) | CHEBI:229652 | aHUS |
| NCT02205541 (ECULISHU) | Phase III | Completed | Eculizumab | NCIT:C48386 | STEC-HUS |
| NCT06389474 | Phase III | Recruiting | INM004 (anti-Shiga toxin antibody) | — (not in OLS) | STEC-HUS |

**Key findings:**
- HERCULES (NCT02553317): Established caplacizumab as the first approved targeted TTP therapy
- NCT03922308: First controlled evaluation of recombinant ADAMTS13 enzyme replacement
- NCT06831058: Novel FcRn inhibition approach to deplete anti-ADAMTS13 IgG autoantibodies
- NCT04889430: First oral complement inhibitor (iptacopan/factor B) evaluated in aHUS
- NCT02205541 (ECULISHU): Negative result — eculizumab does not benefit STEC-HUS
- NCT06389474: Targets Shiga toxin neutralization; first disease-modifying trial for STEC-HUS

---

## Evidence Quality Summary
- Total unique PMIDs: 5 (11586351, 12660343, 23738544, 28416508, 30625070)
- All evidence classified as HUMAN_CLINICAL
- All evidence rated as SUPPORT (PARTIAL for plasma exchange / aHUS context)
- Key landmark papers included: ADAMTS13 discovery (PMID:11586351), HERCULES trial (PMID:30625070), eculizumab aHUS trials (PMID:23738544)

---

## OBO Relations Ontology (RO) Mappings

See `TMA_RO_Relations.md` for a full table of proposed semantic relations linking TMA to its subtypes, phenotypes, pathophysiology, genes, and therapeutic agents.

Key relations used:
- `RO:0002200` — has phenotype → HP terms
- `RO:0004003` — has material basis in germline mutation in → aHUS/TTP genes
- `RO:0002606` — is substance that treats → caplacizumab, eculizumab, iptacopan, etc.
- `RO:0004020` — disease has basis in dysfunction of → ADAMTS13, complement pathway
- `rdfs:subClassOf` — TTP → TMA (formal MONDO hierarchy)
