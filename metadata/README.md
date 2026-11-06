# Reconstructed metadata documentation

The original R Markdown notebooks and rendered HTML files are preserved unchanged. This directory contains metadata documentation added later to make the archived project easier to audit.

## File in this folder

### `rna_fastq_runs.tsv`

This tab-separated table maps every GSE194116 SRA run to the corresponding experiment, GEO sample, patient, tissue, raw-count column, and preserved FastQC/MultiQC status.

| Column | Meaning |
|---|---|
| `run_accession` | SRA run accession (`SRR*`) identifying one paired-end sequencing run. |
| `sra_experiment` | SRA experiment accession (`SRX*`) linked to the run. |
| `geo_sample` | GEO sample accession (`GSM*`). |
| `sample_id` | Human-readable project label such as `ESCC-1` or `Normal-1`. |
| `patient_id` | Patient identifier used to connect the ESCC and adjacent-normal pair. |
| `tissue_type` | `ESCC` tumor or `NORMAL` adjacent tissue. |
| `count_column` | Matching column name in `GSE194116_Raw_gene_counts_matrix.txt`. The deposited tumor columns use the original `ECA-*` naming. |
| `included_in_2024_multiqc` | Whether FastQC output for the run appears in the preserved `multiqc_report.html`. |

The table contains 12 runs representing six matched patients. Eleven runs appear in the preserved MultiQC report. `SRR17686677`, corresponding to `GSM5828367` / `ESCC-5` / patient `271121`, is the only missing run.

## Related reconstructed file at repository root

The notebooks read a root-level file named `phenotype_data.txt` for GSE157807 methylation samples. The original local copy was not present in the archived project folder. Its replacement was reconstructed from:

- the phenotype table printed in `Methylation_analysis.html`;
- the embedded `pData()` output;
- the ten GSM accessions and original IDAT filenames.

The recovered file preserves the `ca-` tumor and `con-` normal patient prefixes expected by the original notebooks. It corrects obvious prose-table typos by following the executed notebook output and actual IDAT filenames. The recovered file is documentation/supporting input added during GitHub packaging; it is not presented as an untouched original artifact.
