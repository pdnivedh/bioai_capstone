# RA raw data (not added yet)

Plan: discovery on GSE55457 (13 RA vs 10 normal synovium), replication on GSE55235 (10 RA vs 10 normal).
Both are Affymetrix HG-U133A (GPL96). Leave the osteoarthritis (OA) samples out of the comparison.

1. Run GEO2R on the series with two groups: RA and normal.
2. Download the full results table and save it here, e.g. `GSE55457_top_table.tsv`.
3. In `signature/01_signature_extraction.ipynb`, set DISEASE = "ra" and INPUT_FILE to that file.
