# edgeR RNA-seq outputs

This folder contains the original outputs from the primary RNA-seq differential-expression analysis performed with edgeR on the GSE194116 raw gene-count matrix.

## Result tables

| File | Description |
|---|---|
| `resP_edgeR_ESCC.txt` | Full edgeR result table for 24,315 genes retained after low-expression filtering. Columns are `ensembl_id`, `gene_name`, `logFC`, `logCPM`, quasi-likelihood `F`, raw `PValue`, and adjusted `FDR`. This is byte-identical to `results/resP_edgeR_ESCC.txt`. |
| `resP_edgeR_filtered_ESCC.txt` | FDR-filtered edgeR table containing 7,305 genes with FDR < 0.05. |

The sign of `logFC` follows the factor contrast encoded in the original notebook. Consult `Analysis_raw_count.Rmd` when assigning biological direction to positive and negative values.

## Figures

| File | Description |
|---|---|
| `plotMDS_ESCC.jpg` | Multidimensional scaling plot used to assess separation between the six ESCC and six adjacent-normal RNA-seq libraries. |
| `BCVplot_ESCC.jpg` | Biological coefficient of variation plot showing dispersion as a function of expression level after edgeR normalization and model setup. |
| `VolcanoPlot_ESCC.jpg` | Volcano plot of log2 fold change versus -log10 p-value; significant genes are highlighted in the original plotting code. |
| `resP_edgeR_ESCC_MA.jpg` | MA/MD plot showing log-fold change against average abundance for the edgeR test. |
| `resP_edgeR_ESCC_histogram.jpg` | Histogram of raw edgeR p-values, used as a diagnostic for the overall test distribution. |

## Place in the project

```text
GSE194116 raw count matrix
  -> low-expression filtering
  -> edgeR normalization and paired model
  -> complete and FDR-filtered tables
  -> QC and differential-expression figures
  -> copies of the main tables used in results/Comparison.Rmd
```
