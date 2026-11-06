# C results: primary RNA-seq outputs

| File | Meaning |
|---|---|
| `resP_edgeR_ESCC.txt` | Full edgeR differential-expression table after filtering. It contains logFC, abundance, test statistics, p-values, and FDR. |
| `resP_edgeR_filtered_ESCC.txt` | edgeR genes passing the project FDR threshold. |
| `RNAseq_results.txt` | Sorted RNA result table used by the integration analysis. |
| `RNAseq_GSA_results.txt` | GO Biological Process enrichment results for significant RNA genes. |
| `plotMDS_ESCC.jpg` | Sample-level expression similarity and grouping diagnostic. |
| `BCVplot_ESCC.jpg` | Biological coefficient of variation diagnostic. |
| `VolcanoPlot_ESCC.jpg` | Significance versus fold-change overview. |
| `resP_edgeR_ESCC_MA.jpg` | Fold change versus average abundance diagnostic. |

The tables answer which genes change between paired ESCC and normal samples; the figures show whether the model and result distribution look reasonable.
