# Omics-driven drug repurposing with target validation

Module 4 capstone, AI in Molecular Sciences. Pipeline: disease signature -> repurposing match (LINCS L1000) -> binding-affinity validation.
Diseases: heart failure (GSE57338, validation case) and rheumatoid arthritis (motivating case).

## Layout
| Folder | Owner | Content |
|---|---|---|
| `signature/` | Person A | Notebook + signature outputs per disease |
| `repurposing/` | Person B | Reversal scoring against LINCS |
| `binding/` | Person C | Binding-affinity models |
| `pipeline/` | Person D | Orchestration, CI |
| `report/` | Person E | Figures, final report |
| `docs/` | all | Data contract |

## Run (signature stage)
```bash
pip install -r requirements.txt
jupyter notebook signature/01_signature_extraction.ipynb
```
Input is a GEO2R full results table placed in `data/raw/<disease>/`. See `docs/data-contract.md` for formats.
