# Exploratory limma RNA-seq outputs

This folder preserves an alternative RNA-seq differential-expression analysis generated with limma. It is supplementary to the edgeR workflow used in the main comparison.

## Result tables

| File | Description |
|---|---|
| `resP_limma_ESCC.txt` | Complete limma result table for 24,315 filtered genes. Columns include Ensembl/gene annotation, `logFC`, average expression (`AveExpr`), moderated `t`, raw `P.Value`, adjusted `adj.P.Val`, and log-odds statistic `B`. |
| `resP_limma_filtered_ESCC.txt` | FDR-filtered limma table containing 7,205 genes with adjusted p-value < 0.05. |

## Figures

| File | Description |
|---|---|
| `VolcanoPlot_ESCC.jpg` | Limma volcano plot summarizing effect size and statistical significance. |
| `resP_limma_ESCC_MA.jpg` | Limma MA plot showing log-fold change versus average expression. |
| `resP_limma_ESCC_histogram.jpg` | Histogram of the raw limma p-values. |

The code that generated this exploratory limma folder was not retained as a separate notebook in the archived project. These outputs were not the primary inputs to `results/Comparison.Rmd`; that comparison used the edgeR-derived `RNAseq_results.txt`.
