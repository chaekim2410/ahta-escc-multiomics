# A. Data overview and quality control

This folder describes the project inputs, sample metadata, paired design, and sequencing quality summary.

## Data

- `GSE194116_Raw_gene_counts_matrix.txt`: published RNA-seq gene-count matrix. Rows are genes and columns are samples.
- `GSE194116_series_matrix.txt`: GEO sample metadata for the RNA experiment.
- `phenotype_data.txt`: methylation sample phenotype table, including patient ID and tissue type.
- `metadata/rna_fastq_runs.tsv`: SRR, GSM, patient, tissue, and count-column mapping.
- `idat/GSE157807_RAW/`: the 20 original red/green IDAT files used by the methylation notebook.

The methylation experiment contains five ESCC and five matched normal samples from GSE157807. The RNA experiment contains six ESCC and six matched normal samples from GSE194116. Tumor and normal samples are paired within patient.

## FastQC and MultiQC

`fastqc/multiqc_report.html` is the preserved summary of FastQC results for 11 of 12 RNA-seq runs. It checks read quality, GC content, duplicated reads, sequence length, and adapter-related signals. `SRR17686677` is not present in the preserved report. This is a sequencing QC report, not a differential-expression result.

The original FASTQ files are not present in the desktop project or this repository. The SRR mapping and the available FastQC summary are included; the RNA analysis itself starts from the published count matrix.

## Notebook

`Data_Overview_Chaeyoung_Kim.Rmd` and its HTML report show the original data inspection steps. The overview notebook loads several teaching/example packages; the main downstream analyses are in folders B and C.

## Key data/QC result

The metadata defines matched tumor-normal pairs for the methylation and RNA analyses. The preserved MultiQC report contains FastQC output for **11 of 12** RNA-seq runs; `SRR17686677` is the missing run.
