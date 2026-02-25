# Maize Whole Genome Sequencing (WGS) → Population Genomics Pipeline

This repository demonstrates a reproducible Linux/HPC workflow for maize (Zea mays) whole genome sequencing analysis, including variant discovery and population structure assessment.

---

## Workflow Summary

FASTQ  
→ Quality Control (FastQC + MultiQC)  
→ Alignment to reference genome (BWA-MEM2)  
→ Variant Calling (bcftools mpileup + call + norm)  
→ SNP Filtering (biallelic + depth filter)  
→ Population Structure Analysis (PLINK PCA)

Pipeline executed on Linux HPC:
- 12 CPU cores
- 128 GB RAM
- Interactive OnDemand desktop session

---

## Reference Genome

Zea mays: Zm-B73-REFERENCE-NAM-5.0  
Source: Ensembl Plants  
(See `data/reference/reference_info.txt`)

---

## Demo Dataset

Public NCBI SRA runs used for pipeline validation:
- SRR13040214  
- SRR13040215  

Note: These are small demo runs to validate workflow architecture.  
The pipeline is scalable to larger multi-sample WGS datasets.

---

## Key Outputs

- PCA plot: `results/popgen_se/pca_plot.png`
- PCA eigenvectors: `results/popgen_se/pca.eigenvec`
- Alignment statistics: `results/align_merged/*.flagstat.txt`
- QC summary: `results/qc/multiqc_report.html`

---

## Tools Used

- FastQC
- MultiQC
- fastp
- BWA-MEM2
- samtools
- bcftools
- PLINK
- Python (pandas, matplotlib)

---

## Future Extensions

- Fst calculation
- Nucleotide diversity (π)
- GWAS integration
- Snakemake workflow automation
- Multi-sample population structure scaling
