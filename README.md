# Lysosomal Enzyme Sequence Analysis: ACP5

## Student Information

- **Name:** Junavhel Jane B. Olaguir
- **Course:** BS Biology
- **Year and Section:** 3rd Year – [Insert Section]
- **Subject:** Cell and Molecular Biology Laboratory
- **Activity:** Exploring Lysosomal Enzymes Using NCBI and R

## 1. Introduction

This activity focuses on the sequence analysis of the human **ACP5** gene, which encodes tartrate-resistant acid phosphatase type 5 (TRAP). The protein sequence was retrieved from the National Center for Biotechnology Information (NCBI) and analyzed using RStudio.

The analysis aimed to determine the protein's length, examine its amino acid composition, and identify potential N-glycosylation motifs. The results were saved as CSV files and visualized using graphs generated with the `ggplot2` package.

## 2. Selected Gene and Protein Information

- **Gene symbol:** ACP5
- **Enzyme name:** Tartrate-resistant acid phosphatase type 5
- **Organism:** *Homo sapiens* (human)
- **NCBI RefSeq protein accession:** NP_001602.1
- **Protein length:** 325 amino acids
- **NCBI Protein record:** [NP_001602.1](https://www.ncbi.nlm.nih.gov/protein/NP_001602.1)
- **NCBI Gene record:** [ACP5 (Gene ID: 54)](https://www.ncbi.nlm.nih.gov/gene/54)
- **Date retrieved and analyzed:** October 19, 2026

### Normal Function of ACP5

ACP5 encodes an iron-containing enzyme that catalyzes the hydrolysis of phosphate monoesters, releasing an alcohol and inorganic phosphate. It is also known as tartrate-resistant acid phosphatase (TRAP).

The enzyme is associated with lysosomal functions and bone remodeling. In osteoclasts, TRAP participates in the regulation of osteopontin, a protein involved in bone resorption. Therefore, ACP5 contributes to normal bone metabolism and has functions related to immune cells.

## 3. Methods

The analysis was performed using RStudio and the following R packages:

- `rentrez` – retrieved the protein sequence from NCBI.
- `ggplot2` – generated the visualizations.

The RefSeq accession NP_001602.1 was used to download the human ACP5 protein sequence in FASTA format. The R script then calculated the protein length and the counts and percentages of the 20 standard amino acids.

Potential N-glycosylation motifs were identified by searching for the sequence pattern N-X-S or N-X-T, where X represents any standard amino acid except proline (P). The results were saved in CSV files, and two figures were generated to visualize the amino acid composition and the positions of the potential motifs.

## 4. Results and Discussion

### 4.1 Protein Length and Summary

The downloaded ACP5 protein sequence contains **325 amino acids**. The sequence analysis detected **two potential N-glycosylation motifs**.

| Parameter | Result |
|---|---|
| Gene | ACP5 |
| NCBI protein accession | NP_001602.1 |
| Protein length | 325 amino acids |
| Number of potential N-glycosylation motifs | 2 |

### 4.2 Amino Acid Composition

![ACP5 amino acid composition](figures/ACP5_amino_acid_composition.png)

**Figure 1. Amino acid composition of the human ACP5 protein.** The graph shows the number of occurrences of each standard amino acid in the 325-amino-acid sequence.

Leucine (L) was the most abundant amino acid, with 35 residues (10.77% of the sequence). Alanine (A) was the second most abundant, with 28 residues (8.62%). Glycine (G) and valine (V) each occurred 23 times (7.08%).

Cysteine (C) was the least abundant amino acid, with only 3 residues (0.92%). Methionine (M) and tryptophan (W) each occurred 6 times (1.85%).

These results describe the amino acid composition of the downloaded protein precursor. Although amino acid composition provides information about the sequence, it does not independently establish the protein's three-dimensional structure or enzymatic activity.

### 4.3 Potential N-Glycosylation Motifs

![ACP5 potential N-glycosylation motifs](figures/ACP5_potential_N_glycosylation.png)

**Figure 2. Positions of potential N-glycosylation motifs in the human ACP5 protein.** The orange points indicate the positions of the detected motifs along the protein sequence.

The analysis identified two potential N-glycosylation motifs:

| Position | Motif | Pattern |
|---:|---|---|
| 116 | NVS | N-X-S |
| 147 | NVS | N-X-S |

Both motifs follow the required N-X-S/T pattern, and the middle amino acid, valine (V), is not proline. Therefore, both sequences qualify as potential N-glycosylation motifs.

However, the presence of these motifs does not confirm that the protein is actually glycosylated at these positions. Experimental evidence would be needed to establish glycosylation. Sequence analysis also cannot establish whether these motifs carry a mannose-6-phosphate (M6P) tag.

## 5. Answers to the Guide Questions

### 1. What does your enzyme normally break down inside lysosomes?

ACP5 encodes an acid phosphatase that removes phosphate groups from phosphate monoesters through hydrolysis, producing an alcohol and inorganic phosphate. Rather than degrading an entire protein into smaller peptides, it performs a specific chemical reaction on suitable phosphate-containing substrates. It is also involved in lysosomal functions and processes associated with bone resorption.

### 2. What is the total length of your protein, and which amino acids are most common?

The ACP5 protein precursor analyzed in this activity contains 325 amino acids. Leucine (L) was the most abundant amino acid, occurring 35 times or 10.77% of the sequence. It was followed by alanine (A), with 28 residues (8.62%), and glycine (G) and valine (V), with 23 residues each (7.08%).

### 3. How many potential N-glycosylation motifs did you find? Where are they located?

Two potential N-glycosylation motifs were identified in the ACP5 sequence. Both have the sequence NVS and are located at positions 116 and 147. They satisfy the N-X-S/T motif rule because the middle amino acid is not proline. These are predicted motifs and are not direct evidence of actual glycosylation.

### 4. Why can glycosylation matter for lysosomal proteins? Does finding a motif prove the protein is glycosylated?

Glycosylation can contribute to protein folding, stability, and proper trafficking through the cell. For many lysosomal enzymes, carbohydrate modifications also participate in processes that help direct proteins to lysosomes. However, identifying an N-X-S/T motif only indicates a possible site of N-linked glycosylation. It does not prove that a carbohydrate chain is attached at that position. Additional biochemical or experimental evidence is needed to confirm glycosylation.

### 5. What could happen in the cell if your enzyme did not work properly?

If ACP5 did not function properly, phosphate-related reactions and processes involving the enzyme could be disrupted. Altered ACP5 activity is associated with abnormal bone remodeling and certain immune-related disorders. Depending on the nature and extent of the defect, these changes could affect normal cellular functions and tissue homeostasis.

## 6. Conclusion

The sequence analysis of human ACP5 identified a protein precursor containing 325 amino acids. Leucine was the most abundant amino acid, accounting for 10.77% of the sequence, while cysteine was the least abundant at 0.92%.

Two potential N-glycosylation motifs, both NVS, were identified at amino acid positions 116 and 147. These results demonstrate how sequence retrieval and basic bioinformatics tools can be used to characterize a protein's length, composition, and potential modification sites.

However, the analysis is limited to sequence-based predictions. It does not directly measure enzyme activity, establish the presence of attached carbohydrate groups, or confirm mannose-6-phosphate tagging.

## 7. Files Included in This Repository

```text
lysosomal-enzyme-ACP5/
├── lysosomal_enzyme_analysis.R
├── README.md
├── data/
│   └── ACP5.fasta
├── results/
│   ├── ACP5_summary.csv
│   ├── ACP5_amino_acid_counts.csv
│   └── ACP5_motif_positions.csv
└── figures/
    ├── ACP5_amino_acid_composition.png
    └── ACP5_potential_N_glycosylation.png
```

### Output Files

- `ACP5.fasta` – downloaded human ACP5 protein sequence.
- `ACP5_summary.csv` – protein length and number of potential N-glycosylation motifs.
- `ACP5_amino_acid_counts.csv` – counts and percentages of the 20 standard amino acids.
- `ACP5_motif_positions.csv` – positions and sequences of the detected potential motifs.
- `ACP5_amino_acid_composition.png` – bar graph showing amino acid composition.
- `ACP5_potential_N_glycosylation.png` – graph showing the positions of potential N-glycosylation motifs.

## 8. References

1. National Center for Biotechnology Information (NCBI). (n.d.). *Tartrate-resistant acid phosphatase type 5 precursor [Homo sapiens]*. RefSeq Protein: NP_001602.1. https://www.ncbi.nlm.nih.gov/protein/NP_001602.1

2. National Center for Biotechnology Information (NCBI). (n.d.). *ACP5 acid phosphatase 5, tartrate resistant [Homo sapiens]*. NCBI Gene: Gene ID 54. https://www.ncbi.nlm.nih.gov/gene/54

3. MedlinePlus Genetics. (n.d.). *ACP5 gene*. U.S. National Library of Medicine. https://medlineplus.gov/genetics/gene/acp5/
