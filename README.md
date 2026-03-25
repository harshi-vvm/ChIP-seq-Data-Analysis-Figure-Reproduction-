# ChIP-seq-Data-Analysis-Figure-Reproduction

This repository contains a step-by-step workflow to reproduce **Figure 1** from the following paper:

> **Paper:** [Genome-wide association between YAP/TAZ/TEAD and AP-1 at enhancers drives oncogenic growth](https://pmc.ncbi.nlm.nih.gov/articles/PMC6186417/)  
> **GEO Dataset:** [GSE66083](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE66083)
---
---
## Folder Details

### `pre-processing/`

Contains all upstream data processing steps, starting from raw FASTQ files through to peak calling and bigwig generation. The steps covered include:

1. **Download FASTQ files** from GEO (accession [GSE66083](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE66083))
2. **Align to the hg38 genome** — read alignment using standard ChIP-seq tools
3. **Generate bigwig files** — for visualization in genome browsers
4. **Call peaks** — identify enriched regions from aligned reads

---

### `analysis/`

Contains R Markdown (`.Rmd`) and rendered HTML files for all downstream analysis and figure reproduction. Each file corresponds to a specific panel from Figure 1 of the paper:

| File | Description |
|------|-------------|
| `figure_a_b_c.Rmd` / `.html` | Re-create Fig 1 panels a, b, c |
| `figure_d_f.Rmd` / `.html` | Re-create Fig 1 panels d, f |
| `figure_g_h.Rmd` / `.html` | Re-create Fig 1 panels g, h |
| `figure_i_j.Rmd` / `.html` | Re-create Fig 1 panels i, j |

---

## How to Reproduce

1. Clone this repository:
```bash
   git clone https://github.com/harshi-vvm/ChIP-seq-Data-Analysis-Figure-Reproduction.git
   cd ChIP-seq-Data-Analysis-Figure-Reproduction
```

2. Follow the pre-processing steps in the `pre-processing/` folder in order — starting from raw FASTQ files through to peak calling and bigwig generation.

3. Once pre-processing is complete, open the `.Rmd` files in the `analysis/` folder in RStudio and knit them to reproduce each figure panel.

## Requirements

- R (≥ 4.0) and RStudio
- Standard ChIP-seq tools: `bowtie2`, `samtools`, `deeptools`, `MACS2`
- R packages as specified in each `.Rmd` file

## License

See [LICENSE](https://crazyhottommy.github.io/reproduce_genomics_paper_figures/license.html) for details.
