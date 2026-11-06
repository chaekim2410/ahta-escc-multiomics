# B. DNA methylation analysis

This folder contains the EPIC methylation-array analysis. Each probe measures methylation at a CpG site. The paired comparison asks whether methylation differs between ESCC and adjacent normal tissue from the same patient.

## Pipeline

1. `minfi` reads red and green IDAT signals and creates methylation objects.
2. `ENmix` performs sample/CpG QC and intensity preprocessing, including background and dye-bias correction.
3. Quantile normalization makes signal distributions more comparable between samples.
4. `limma` models M-values with tissue type while blocking on patient ID.
5. Probe annotation connects CpGs to genes, promoters, CpG islands, and genomic positions.
6. `bumphunter` groups nearby changing CpGs into DMRs and tests region-level changes.
7. CpG-associated and DMR-associated genes are used for GO enrichment to describe biological processes.

## Files

- `Methylation_Analysis.Rmd` / `.html`: original code and rendered report.
- `figures/figure-latex/`: raw QC and MDS figures generated while rendering the notebook.
- `results/`: gene identifiers and GO tables produced by the methylation and DMR analyses.

The most important results are the CpG result table, the DMR-associated gene list, and the two GO tables. Detailed file meanings are in `results/README.md`.
