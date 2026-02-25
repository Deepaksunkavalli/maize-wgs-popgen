# Maize WGS → Variant Calling → Population Genomics (HPC Demo)

End-to-end Linux/HPC workflow:
- QC: FastQC (+ MultiQC)
- Trimming: fastp
- Alignment: BWA-MEM2
- Variant calling: bcftools (mpileup/call/norm)
- PopGen: SNP filtering + PCA (PLINK)

## Reference
Zea mays Zm-B73-REFERENCE-NAM-5.0 (Ensembl Plants). See `data/reference/reference_info.txt`.

## Demo Data
Public NCBI SRA runs used to validate the pipeline:
- SRR13040214
- SRR13040215

## Key outputs
- PCA plot: `results/popgen_se/pca_plot.png`
- PCA eigenvectors: `results/popgen_se/pca.eigenvec`
- Alignment stats: `results/align_merged/*.flagstat.txt`

> Note: demo runs are small; larger multi-sample WGS datasets can be plugged in for real biological inference.
