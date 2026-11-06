# Integrated analysis results

This folder contains the original multi-omics comparison notebook and the result tables it reads. The comparison maps methylation-associated Entrez IDs to Ensembl IDs, compares them with significant RNA-seq genes, and examines overlap among gene sets and GO Biological Process terms.

## Files

| File | Description |
|---|---|
| `Comparison.Rmd` | Original R Markdown source for the RNA-methylation integration. It loads the result tables below, filters RNA genes at FDR < 0.05, maps identifiers with `org.Hs.eg.db`, creates Venn diagrams, and extracts common genes and GO terms. |
| `Comparison.html` | Rendered version of `Comparison.Rmd`, including the original code, output, Venn diagrams, and candidate-gene tables. |
| `resP_edgeR_ESCC.txt` | Complete edgeR quasi-likelihood test table after low-expression filtering: 24,315 genes plus the header. This file is byte-identical to `rna_output/resP_edgeR_ESCC.txt`. |
| `RNAseq_results.txt` | The 7,305 RNA-seq genes retained at FDR < 0.05 and sorted for the downstream comparison. This is the input called `RNAseq_results` in `Comparison.Rmd`. |
| `RNAseq_GSA_results.txt` | Top 100 RNA-seq GO Biological Process results generated with `limma::goana()` / `topGO()`. |
| `EntrezIDs_CpG_results.txt` | 2,212 CpG-associated Entrez IDs after the original nearest-gene mapping and removal of duplicated or missing IDs. Row names store gene symbols and column `x` stores Entrez IDs. |
| `CpG_GSA_results.txt` | Top 100 GO Biological Process results for genes associated with significant individual CpG probes. |
| `EntrezIDs_bmp_results.txt` | Three Entrez IDs associated with significant bumphunter regions: `SEPTIN9`, `ZNF790`, and `TXNRD1`. The original code refers to DMRs as “bumps,” hence `bmp` in the filename. |
| `bmp_GSA_results.txt` | Top 100 GO Biological Process results for genes associated with significant DMRs/bumps. |

## Table-column guide

### edgeR result tables

| Column | Meaning |
|---|---|
| `ensembl_id` | Ensembl identifier carried into the original result table. |
| `gene_name` | Gene annotation column from the input count matrix. |
| `logFC` | Log2 fold change for the contrast encoded in the original edgeR design. |
| `logCPM` | Average log2 counts per million. |
| `F` | Quasi-likelihood F statistic. |
| `PValue` | Raw differential-expression p-value. |
| `FDR` | Benjamini-Hochberg adjusted p-value. |

### GO result tables

| Column | Meaning |
|---|---|
| `Term` | GO term identifier stored as the row name plus its biological-process description. |
| `Ont` | GO ontology; these tables contain Biological Process (`BP`) results. |
| `N` | Number of genes in the tested GO term. |
| `DE` | Number of selected/differential genes assigned to the term. |
| `P.DE` | Over-representation p-value. |
| `FDR.DE` | Benjamini-Hochberg adjusted enrichment p-value. |

## How these files connect

```text
RNAseq_results.txt + EntrezIDs_CpG_results.txt
  -> RNA-CpG gene overlap

RNAseq_results.txt + EntrezIDs_bmp_results.txt
  -> RNA-DMR gene overlap

RNAseq_GSA_results.txt + methylation GSA tables
  -> common GO Biological Process terms
```

These are preserved outputs from the original project. They should be interpreted together with `Comparison.Rmd` and `Comparison.html`, rather than as newly recalculated results.
