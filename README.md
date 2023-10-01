# scQC
In single-cell analysis, quality control (QC) is crucial to ensure that the obtained data is reliable and meaningful. Here are some common thresholds and parameters used for single-cell QC:

## Number of Genes Detected per Cell:

**Threshold:** Typically, cells with a low number of detected genes may be considered low quality. A minimum threshold of detected genes is set to filter out low-quality cells.

**Reason:** Cells with too few detected genes may indicate poor capture efficiency or degraded RNA.

## Number of Unique Molecular Identifiers (UMIs) per Cell:

**Threshold:** A minimum threshold of UMIs is set to ensure that enough RNA molecules were captured and sequenced for accurate analysis.

**Reason:** Low UMI counts may indicate inefficient capture or poor RNA quality.

## Percentage of Mitochondrial Genes:

**Threshold:** Cells with a high percentage of mitochondrial genes may be considered low quality. A threshold is set to filter out cells with excessive mitochondrial gene expression.

**Reason:** Elevated mitochondrial gene expression can indicate cell stress or poor RNA quality.

## Library Size/Total UMIs per Cell:

**Threshold:** Library size normalization is important for comparing gene expression across cells. Cells with extremely low or high library size compared to the median may be flagged for further investigation.

**Reason:** Library size differences can be due to variations in cell size, RNA content, or capture efficiency.

## Doublet Detection:

**Threshold:** Computational tools are used to identify potential cell doublets, where two or more cells are sequenced together and their transcriptomes are merged.

**Reason:** Doublets can lead to incorrect cell type assignments and affect downstream analysis.

## Gene Detection Saturation:

**Threshold:** Assessing the saturation in gene detection helps determine if sequencing depth is sufficient to capture the transcriptome adequately.

**Reason:** Saturation analysis ensures that increasing sequencing efforts yield diminishing returns in terms of detected genes.

## PCR Amplification Cycles:

**Threshold:** Monitoring the number of PCR cycles during library preparation helps identify potential amplification biases. Excessive PCR cycles can introduce artifacts.

**Reason:** High PCR cycles can lead to over-amplification, skewing the representation of transcripts.

These thresholds may vary based on the specific platform, experimental design, and biological system. It's important to tailor QC metrics to the characteristics of your data and research objectives. Integrating QC into the analysis pipeline ensures high-quality, reliable results in single-cell studies.

## Some paper:
1. [Single-cell transcriptomics identifies divergent developmental lineage trajectories during human pituitary development](https://www.nature.com/articles/s41467-020-19012-4#Sec12)  
"To filter out low-quality cells and multiple cells sequenced as one cell, we selected only cells with a **gene number ≥ 2000, an initial reads number ≤ 1E7,  and a mapping ratio ≥ 20% and genes with at least one count in at least three cells** for the following analysis.  The filtered gene expression data set of transcriptional counts was analyzed using the Seurat (Version 2.3.4) package12. As most of the single cells in our data sets were **around 100,000 transcriptional counts, the scale factor was set to 100,000**. The resolution of “FindClusters” was set  as 1 for all cells and merged subclusters of MC with the same known markers (Supplementary Fig. 1d, f), 1.5 for endocrine cells and merged subclusters of Stem, Somatotrope and Gonadotrope with the same known markers (Fig. 1b, c), 0.3 for stem cells (Fig. 2c), 0.4 for gonadotropes (Fig. 7a). Main cell types were identified by the combination of known markers for each cluster."
```
1E7 = 10,000,000
```
