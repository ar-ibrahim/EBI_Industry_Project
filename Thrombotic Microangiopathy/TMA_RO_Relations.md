# OBO Relations Ontology (RO) Mappings for Thrombotic Microangiopathy

This document proposes semantic relations from the [OBO Relations Ontology (RO)](http://www.obofoundry.org/ontology/ro.html) to formally link Thrombotic Microangiopathy (TMA; MONDO:0019737) with its subtypes, phenotypes, pathophysiology nodes, causative genes, and therapeutic agents.

---

## 1. Disease → Subtypes

| Subject | RO Term | Object |
|---------|---------|--------|
| TMA (MONDO:0019737) | `rdfs:subClassOf` | Microangiopathy |
| TTP (MONDO:0018896) | `rdfs:subClassOf` | TMA (MONDO:0019737) |
| HUS (MONDO:0001549) | `RO:0002610` has_phenotype_manifestation_of / correlated with | TMA (MONDO:0019737) |

**Notes:**
- TTP is a formal MONDO subclass of TMA → use `rdfs:subClassOf`.
- HUS is clinically grouped under TMA but is **not** a formal MONDO subclass; `RO:0002610` (correlated with) captures the clinical association without asserting strict subsumption.
- Drug-induced TMA and Secondary TMA have no MONDO terms; they are best captured as clinical phenotype groupings described in natural language.

---

## 2. Disease → Phenotypes

| Subject | RO Term | Label | Object |
|---------|---------|-------|--------|
| TMA (MONDO:0019737) | `RO:0002200` | has phenotype | Thrombocytopenia (HP:0001873) |
| TMA (MONDO:0019737) | `RO:0002200` | has phenotype | Microangiopathic hemolytic anemia (HP:0001937) |
| TMA (MONDO:0019737) | `RO:0002200` | has phenotype | Acute kidney injury (HP:0001919) |
| TMA (MONDO:0019737) | `RO:0002200` | has phenotype | Seizure (HP:0001250) |
| TMA (MONDO:0019737) | `RO:0002200` | has phenotype | Elevated lactate dehydrogenase (HP:0025435) |
| TMA (MONDO:0019737) | `RO:0002200` | has phenotype | Schistocytosis (HP:0001981) |

**`RO:0002200`** — *has phenotype*: Connects a disease to its characteristic signs/symptoms. This is the standard OBO relation used in OMIM, Monarch, and HPO disease-phenotype associations.

---

## 3. Disease → Pathophysiological Basis

### 3a. Dysfunction of molecular mechanisms

| Subject | RO Term | Label | Object |
|---------|---------|-------|--------|
| TTP (MONDO:0018896) | `RO:0004020` | disease has basis in dysfunction of | ADAMTS13 enzyme activity |
| TTP (MONDO:0018896) | `RO:0004021` | disease has basis in disruption of | VWF multimer cleavage |
| aHUS | `RO:0004020` | disease has basis in dysfunction of | Complement alternative pathway regulation |
| TMA (MONDO:0019737) | `RO:0004020` | disease has basis in dysfunction of | Endothelial cell homeostasis |
| TMA (MONDO:0019737) | `RO:0004024` | disease causes disruption of | Glomerular filtration (renal function) |
| TMA (MONDO:0019737) | `RO:0004025` | disease causes dysfunction of | Platelet aggregation regulation |

**Key RO terms:**
- `RO:0004020` — *disease has basis in dysfunction of*: The disease arises because a normal biological function is impaired.
- `RO:0004021` — *disease has basis in disruption of*: A structural or process disruption underlies the disease.
- `RO:0004024` — *disease causes disruption of*: The disease actively disrupts a downstream process (ischemia, organ failure).
- `RO:0004025` — *disease causes dysfunction of*: The disease impairs a biological function as a consequence.

### 3b. Feature relations (pathological hallmarks)

| Subject | RO Term | Label | Object |
|---------|---------|-------|--------|
| TMA (MONDO:0019737) | `RO:0004029` | disease has feature | Microvascular thrombosis |
| TMA (MONDO:0019737) | `RO:0004029` | disease has feature | Microangiopathic hemolysis |
| TMA (MONDO:0019737) | `RO:0004029` | disease has feature | Endothelial cell activation |

**`RO:0004029`** — *disease has feature*: Captures pathological features (lesions, histological hallmarks) that define the disease, distinct from symptoms (`has phenotype`).

---

## 4. Disease → Causative Genes (Genetic Basis)

| Subject | RO Term | Label | Object |
|---------|---------|-------|--------|
| TTP / Upshaw-Schulman syndrome | `RO:0004003` | has material basis in germline mutation in | ADAMTS13 (HGNC:1366) |
| aHUS | `RO:0004003` | has material basis in germline mutation in | CFH (HGNC:4883) |
| aHUS | `RO:0004003` | has material basis in germline mutation in | CFI (HGNC:5394) |
| aHUS | `RO:0004003` | has material basis in germline mutation in | CD46 / MCP (HGNC:6953) |
| aHUS | `RO:0004003` | has material basis in germline mutation in | CFB (HGNC:1zhf / HGNC:1379) |
| aHUS | `RO:0004003` | has material basis in germline mutation in | C3 (HGNC:1327) |
| aHUS | `RO:0004003` | has material basis in germline mutation in | THBD (HGNC:11529) |
| aHUS | `RO:0004003` | has material basis in germline mutation in | DGKE (HGNC:2849) |
| TTP (acquired) | `RO:0004006` | has partial material basis in germline mutation in | ADAMTS13 (HGNC:1366) |
| TMA (general) | `RO:0004023` | causal relationship with disease as subject | VWF (HGNC:12726) — modifier gene |

**Key RO terms:**
- `RO:0004003` — *has material basis in germline mutation in*: The disease is caused by an inherited mutation in this gene. Appropriate for Upshaw-Schulman syndrome (congenital TTP) and complement gene mutations in aHUS.
- `RO:0004004` — *has material basis in somatic mutation in*: For somatic variants (not typically applicable here; most TMA mutations are germline).
- `RO:0004006` — *has partial material basis in germline mutation in*: When a gene contributes but is not solely causative (e.g., ADAMTS13 in acquired TTP where autoantibodies are the proximal cause).
- `RO:0004023` — *causal relationship with disease as subject*: A broader causal link where directionality or mechanism is less defined.

---

## 5. Therapeutic Agent → Disease

| Subject | RO Term | Label | Object |
|---------|---------|-------|--------|
| Caplacizumab (NCIT:C128625) | `RO:0002606` | is substance that treats | TMA / TTP |
| Eculizumab (NCIT:C48386) | `RO:0002606` | is substance that treats | aHUS / TMA |
| Ravulizumab (NCIT:C124657) | `RO:0002606` | is substance that treats | aHUS / TMA |
| Rituximab (NCIT:C1702) | `RO:0002606` | is substance that treats | Acquired TTP |
| Corticosteroid (CHEBI:50858) | `RO:0002606` | is substance that treats | Acquired TTP |

**`RO:0002606`** — *is substance that treats*: The canonical OBO relation linking a chemical entity to the disease it treats. Used in DrugBank, ChEMBL, and disease ontology mappings.

---

## 6. Participants in Pathological Processes

| Subject | RO Term | Label | Object |
|---------|---------|-------|--------|
| Platelet aggregation (GO:0070527) | `RO:0000057` | has participant | Platelet (CL:0000233) |
| Complement activation (GO:0006958) | `RO:0000057` | has participant | Glomerular endothelial cell (CL:0002188) |
| Endothelial cell activation | `RO:0000057` | has participant | Endothelial cell (CL:0000115) |

**`RO:0000057`** — *has participant*: Links a process to the entities (cells, molecules) that participate in it. Appropriate for GO biological process ↔ CL cell type associations.

---

## 7. Summary Table

| Relation IRI | Label | Primary Use in TMA |
|-------------|-------|--------------------|
| `RO:0002200` | has phenotype | TMA → HP phenotype terms |
| `RO:0004020` | disease has basis in dysfunction of | TMA/TTP/aHUS → impaired molecular function |
| `RO:0004021` | disease has basis in disruption of | TMA → disrupted VWF cleavage, complement regulation |
| `RO:0004022` | disease has basis in feature | TMA → pathological hallmarks |
| `RO:0004023` | causal relationship with disease as subject | TMA ↔ modifier genes |
| `RO:0004024` | disease causes disruption of | TMA → organ dysfunction (renal, neurological) |
| `RO:0004025` | disease causes dysfunction of | TMA → platelet/coagulation dysregulation |
| `RO:0004029` | disease has feature | TMA → microvascular thrombosis, hemolysis |
| `RO:0004003` | has material basis in germline mutation in | aHUS/congenital TTP → CFH, ADAMTS13, etc. |
| `RO:0004006` | has partial material basis in germline mutation in | Acquired TTP → ADAMTS13 (partial basis) |
| `RO:0002606` | is substance that treats | Caplacizumab, eculizumab, etc. → TMA |
| `RO:0002610` | correlated with | HUS ↔ TMA (clinical grouping, not subclass) |
| `RO:0000057` | has participant | GO processes → CL cell types |
| `rdfs:subClassOf` | subclass of | TTP → TMA (formal MONDO hierarchy) |

---

## References

- OBO Relations Ontology: https://www.obofoundry.org/ontology/ro.html
- Monarch Disease-Phenotype Associations (uses RO:0002200): https://monarchinitiative.org
- MONDO Disease Ontology: https://mondo.monarchinitiative.org
- OMIM Gene-Disease Relations (uses RO:0004003): https://omim.org
