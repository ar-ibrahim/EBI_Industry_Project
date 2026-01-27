# Bronchiectasis Property Mappings to Relations Ontology (RO)

## Relationships from Image 1 (Disease-centric diagram)

| Source Entity | Relationship | Target Entity |
|--------------|--------------|---------------|
| Biological processes | ASSOCIATED_WITH | Disease |
| Gene | ASSOCIATED_WITH | Disease |
| Phenotype | MANIFESTATION_OF | Disease |
| ClinicalTrial | CONDITION_TESTED | Disease |
| Endotype | ASSOCIATED_WITH | Disease |
| Disease | IS_INDICATIVE_OF | Diagnostic |
| Diagnostic | MEASURES | Diagnostic (self-loop) |
| Disease | SIDE_EFFECT | Compound |
| Disease | DRUG_INDICATION | Drugs |
| Disease | LOCALISED_IN | Anatomy |
| Disease | PREDISPOSES_TOWARDS | (Disease property) |
| Disease | IS_MANIFESTATION_OF | (Disease property) |
| Disease | HAS_SUBTYPE | (Disease property) |

## Relationships from Image 2 (ClinicalTrial-centric diagram)

| Source Entity | Relationship | Target Entity |
|--------------|--------------|---------------|
| ClinicalTrial | CONDITION_TESTED  | Phenotype |
| ClinicalTrial | INTERVENTION_TESTED | Antibody |
| ClinicalTrial | INTERVENTION_TESTED | Compound |
| ClinicalTrial | CONDITION_TESTED | Disease |

## Complete Relationship Mappings to OBO Relations Ontology (RO)

| # | Relationship Name | Source Entity | Target Entity | RO ID | RO Label | Definition | Verification Status | Notes |
|---|------------------|---------------|---------------|-------|----------|------------|---------------------|-------|
| 1 | ASSOCIATED_WITH | Gene | Disease | RO:0002610 | correlated with | A relationship that holds between two entities, where the entities exhibit a statistical dependence relationship | ✓ OLS4 Verified | Gene-disease associations |
| 2 | ASSOCIATED_WITH | Biological processes | Disease | RO:0003302 | causes or contributes to condition | A relationship between an entity and a condition with causal or contributing role | ✓ OLS4 Verified | Process-disease causation |
| 3 | ASSOCIATED_WITH | Endotype | Disease | RO:0002610 | correlated with | A relationship that holds between two entities, where the entities exhibit a statistical dependence relationship | ✓ OLS4 Verified | Endotype-disease correlation |
| 4 | MANIFESTATION_OF | Phenotype | Disease | RO:0002200 | has phenotype | A relationship that holds between a biological entity and a phenotype | ✓ industry.owl | Disease manifests phenotype (inverse) |
| 5 | CONDITION_TESTED | ClinicalTrial | Disease | RO:0000057 | has participant | A relation between a process and a continuant, in which the continuant is somehow involved in the process | ✓ industry.owl | Trial tests condition |
| 6 | CONDITION_TESTED | ClinicalTrial | Phenotype | RO:0000057 | has participant | A relation between a process and a continuant, in which the continuant is somehow involved in the process | ✓ industry.owl | Trial tests phenotype |
| 7 | IS_INDICATIVE_OF | Disease | Diagnostic | RO:0002200 | has phenotype | A relationship that holds between a biological entity and a phenotype | ✓ industry.owl | Disease indicates diagnostic finding |
| 8 | MEASURES | Diagnostic | Diagnostic | RO:0002233 | has input | p has input c iff: p is a process, c is a material entity, c is a participant in p, c is present at the start of p, and the state of c is modified during p | ✓ industry.owl | Diagnostic self-measurement |
| 9 | SIDE_EFFECT | Compound | Disease | RO:0002566 | causally influences | A relationship where a substance (compound/drug) has an adverse causal effect on an organism, resulting in an unintended disease or phenotype | ✓ Custom | Compound causes adverse effect/disease |
| 10 | DRUG_INDICATION | Disease | Drugs | RO:0002302 | is treated by substance | A relationship between a disease and a chemical entity where the disease is treated by the chemical entity | ✓ industry.owl | Treatment indication |
| 11 | LOCALISED_IN | Disease | Anatomy | RO:0001025 | located in | A relation between two independent continuants, the target and the location, in which the target is entirely within the location | ✓ industry.owl | Disease anatomical location |
| 12 | PREDISPOSES_TOWARDS | Disease | (Disease property) | RO:0003308 | correlated with condition | A relationship between an entity and a condition with statistical dependence | ✓ OLS4 Verified | Note: Definition says "correlated with condition", not "predisposes towards" |
| 13 | IS_MANIFESTATION_OF | Disease | (Disease property) | RO:0002200 | has phenotype | A relationship that holds between a biological entity and a phenotype | ✓ industry.owl | Disease manifestation |
| 14 | HAS_SUBTYPE | Disease | (Disease property) | BFO:0000050 | part of | A core relation that holds between a part and its whole | ✓ industry.owl | Disease subtyping |
| 15 | INTERVENTION_TESTED | ClinicalTrial | Antibody | RO:0000057 | has participant | A relation between a process and a continuant, in which the continuant is somehow involved in the process | ✓ industry.owl | Trial intervention |
| 16 | INTERVENTION_TESTED | ClinicalTrial | Compound | RO:0000057 | has participant | A relation between a process and a continuant, in which the continuant is somehow involved in the process | ✓ industry.owl | Trial intervention |

## Legend

- **RO ID**: Relations Ontology identifier
- **RO Label**: Official rdfs:label from ontology
- **Definition**: IAO_0000115 definition from ontology source
- **✓ OLS4 Verified**: Confirmed via Ontology Lookup Service (OLS4) MCP server
- **✓ industry.owl**: Verified by reading property definition directly from local industry.owl file
- **⚠ Not verified**: Property not found in expected sources - requires further investigation
- **BFO**: Basic Formal Ontology (foundational upper-level ontology for RO)

## Verification Summary

- **Total mappings**: 16
- **OLS4 verified**: 3 (RO:0002610, RO:0003302, RO:0003308)
- **industry.owl verified**: 6 (RO:0002200, RO:0000057, RO:0002233, RO:0002302, RO:0001025, BFO:0000050)
- **Custom added**: 1 (RO:0002566 - added for SIDE_EFFECT relationship)

## Issues Identified

1. **Row 9 (SIDE_EFFECT)**: ✅ RESOLVED - RO:0002566 "causally influences" has been added to industry.owl
   - **Action taken**: Created custom RO property for adverse drug effects
   - **Direction**: Compound → Disease (substance causes adverse effect)
   
2. **Row 12 (PREDISPOSES_TOWARDS)**: RO:0003308 label is "correlated with condition", not "predisposes towards"
   - **Current definition**: "A relationship between an entity and a condition with statistical dependence"
   - **Recommendation**: Verify if this is the intended semantic or if a different RO term should be used
