# Exploratory DESeq2 outputs

This folder preserves an alternative RNA-seq analysis generated with DESeq2. These files are supplementary/exploratory outputs; the primary differential-expression workflow documented in `Analysis_raw_count.Rmd` and used for the final multi-omics comparison is the edgeR analysis.

| File | Description |
|---|---|
| `DESeq2_results_ESCC.txt` | DESeq2 result table for 40,164 input genes. It contains `baseMean`, `log2FoldChange`, `lfcSE`, Wald `stat`, raw `pvalue`, and adjusted `padj`. The first unlabeled field stores the original row index. |
| `resP_deseq_ESCC_MA.jpg` | DESeq2 MA plot showing log2 fold change as a function of mean normalized abundance. |

The R script/notebook that generated this exploratory DESeq2 folder was not retained in the archived project. The files are included as original project artifacts, not as inputs to `results/Comparison.Rmd`.
