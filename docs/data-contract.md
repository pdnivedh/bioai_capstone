# Data contract

Every stage reads the previous stage's output in exactly this format, so modules can be built in parallel.
Disease keys: `hf` (heart failure), `ra` (rheumatoid arthritis).

## A -> B: signature (signature/results/<disease>/)
| File | Format |
|---|---|
| `<disease>_signature_up.txt` | one HGNC gene symbol per line, genes higher in disease vs control |
| `<disease>_signature_down.txt` | one HGNC gene symbol per line, genes lower in disease vs control |
| `<disease>_full_results.csv` | cleaned DE table: ID, adj.P.Val, P.Value, t, B, logFC, Gene.symbol, Gene.title |

Sign convention: logFC > 0 means higher in disease (failing / RA). Gene symbols are unique per file.

## B -> C: candidates (proposal, agree as a team before building)
`repurposing/results/<disease>_candidates.csv` with columns: `rank, drug, reversal_score, source_db`

## C -> E: validation (proposal)
`binding/results/<disease>_binding.csv` with columns: `drug, target, predicted_affinity, model`
