# Methylation PDF figures

These one-page PDFs were generated automatically from unnamed chunks in `Methylation_Analysis.Rmd`.

| File | Plot and interpretation |
|---|---|
| `unnamed-chunk-14-1.pdf` | Beta-value MDS plot based on the 1,000 most variable methylation positions. Samples are labelled by the original `ca-*` ESCC and `con-*` normal patient identifiers. It is used to inspect sample relationships and tissue-group separation. |
| `unnamed-chunk-19-1.pdf` | Density distributions of raw red and green channel log2 intensities. This checks channel-level signal distributions before preprocessing. |
| `unnamed-chunk-19-2.pdf` | Density distributions of raw methylated and unmethylated log2 intensities. This compares the two methylation signal components before preprocessing. |
| `unnamed-chunk-19-3.pdf` | Per-sample distributions of the log2 sum of methylated and unmethylated intensities. This is a raw total-signal QC view. |
| `unnamed-chunk-19-4.pdf` | Combined raw methylated/unmethylated intensity distributions for all ten samples. It provides another view of between-sample signal consistency. |
| `unnamed-chunk-19-5.pdf` | Raw beta-value distributions for all ten methylation samples. The expected peaks near unmethylated and highly methylated values are visible. |
| `unnamed-chunk-19-6.pdf` | Raw M-value distributions for all ten samples. M-values are the scale used for the downstream limma differential-methylation model. |

The authoritative context for every plot is the surrounding text and code in `Methylation_Analysis.Rmd` and its rendered HTML report.
