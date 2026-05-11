# GlycoEP: In silico Platform for Prediction of Glycosites

Welcome to the official repository and documentation overview for **GlycoEP**, an open-access web server designed for the accurate prediction of N-, O-, and C-linked glycosites in eukaryotic protein sequences. Glycosylation is a critical post-translational modification involved in protein folding, cell-cell interactions, and host-pathogen recognition. GlycoEP was developed to provide biologists with a more robust tool for identifying these sites using high-quality, non-redundant datasets.

**Web Server:** [(https://webs.iiitd.edu.in/raghava/glycoep/suppli.html)]

---

## Citation

Chauhan JS, Rao A, Raghava GPS (2013).
**In silico Platform for Prediction of N-, O- and C-Glycosites in Eukaryotic Protein Sequences.**
*PLoS ONE* 8(6): e67008.
[https://doi.org/10.1371/journal.pone.0067008](https://doi.org/10.1371/journal.pone.0067008)

Zenodo:-(https://doi.org/10.5281/zenodo.20063245)

---

## About the Platform

GlycoEP addresses the limitations of existing glycosylation prediction tools by utilizing larger, more stringently filtered datasets and advanced machine-learning techniques[cite: 1]. The platform supports the prediction of three major types of eukaryotic glycosylation:

*   **N-linked**: Attachment to the Nitrogen atom of Asparagine (Asn) in the $Asn-X-Ser/Thr$ sequon.
*   **O-linked**: Attachment to Serine (Ser) or Threonine (Thr) residues.
*   **C-linked**: Attachment to the first Tryptophan (Trp) in motifs like $W-X-X-W$.

The server offers two tiers of prediction models:
1.  **Standard Models**: Developed from non-redundant proteins where no two sequences share more than **40% similarity**.
2.  **Advanced Models**: Developed from highly non-redundant pattern datasets where no two glycosite patterns share more than **60% similarity**, ensuring more robust and biologically meaningful predictions.

---

## Key Features

### Predictive Modeling
*   **Machine Learning**: Support Vector Machine (SVM) was identified as the optimum tool for these models, utilizing the RBF kernel.
*   **High Accuracy**: Advanced SVM models achieved accuracies of **84.26%** for N-linked, **86.87%** for O-linked, and **91.43%** for C-linked glycosites.
*   **Feature Integration**: Models incorporate Binary Profiles of Patterns (BPP), Composition Profiles (CPP), and PSSM profiles (PPP).

### Structural Information
*   **Secondary Structure**: Incorporates three-state structure information (Coil, Helix, Strand) obtained via PSIPRED.
*   **Surface Accessibility**: Includes Predicted Accessible Surface Area (ASA) values, which significantly improve O-glycosite prediction.

### Built-in Tools
*   **Sequon Scanner**: A dedicated tool to scan input protein sequences for both universal and rare N-linked glycosylation motifs.
*   **Multiple Submissions**: The server allows users to submit multiple sequences simultaneously for high-throughput analysis.

---

## Overview of Model Development

GlycoEP models were trained and evaluated using a 5-fold cross-validation procedure. The datasets were derived from the SWISS-PROT database (June 2011 release), focusing exclusively on experimentally verified eukaryotic glycoproteins. Overlapping patterns of **21 residues** were generated for each potential glycosite to capture the local sequence context.

| Feature | N-linked | O-linked | C-linked |
| :--- | :--- | :--- | :--- |
| **Primary Motif** | $Asn-X-Ser/Thr$ | Ser/Thr (no consensus) | $W-X-X-W/C/F$ |
| **Advanced Accuracy** | 84.24% | 86.87% | 91.43% |
| **MCC (Advanced)** | 0.54 | 0.20 | 0.78 |

---

## Applications

*   **Proteomics**: Characterization and annotation of glycosites in eukaryotic proteins.
*   **Therapeutics**: Analysis of human therapeutic glycoproteins, which constitute over 70% of current protein-based drugs.
*   **Biological Research**: Investigating the role of glycans in protein folding, cell signaling, and host-pathogen interactions.

---


## Contact & Authors

Developed under the Open Source Drug Discovery (OSDD) initiative

Prof. Dr. Gajendra PS Raghava

raghava@iiitd.ac.in

---

## License

This platform and its associated research are distributed under the **Creative Commons Attribution License (CC BY 2.0)**.
