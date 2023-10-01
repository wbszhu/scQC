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

These thresholds may vary based on the specific platform, experimental design, and biological system. It's important to tailor QC metrics to the characteristics of your data and research objectives. Integrating QC into the analysis pipeline ensures high-quality, reliable results in single-cell studies
