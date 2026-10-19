# Heart failure signature (Stage 1 output)

- Dataset: GSE57338 (left ventricle, failing vs non-failing), GEO2R / limma
- Sign convention: logFC > 0 = HIGHER in failing hearts (validated: NPPA, FRZB, SMOC2 up; MYH6 down)
- Cleaning: dropped probes with no gene symbol, multi-gene probes ("///"), kept most significant probe per gene, removed sex-linked genes (Y-linked, XIST)
- Filter: adj.P.Val < 0.05, then top 150 up and top 150 down by logFC
- Files: hf_signature_up.txt, hf_signature_down.txt (one gene symbol per line), hf_full_results.csv
- Not done yet: etiology adjustment (DCM vs ICM), replication on a second cohort
