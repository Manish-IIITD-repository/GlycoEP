# GDoQ: Web Server for GlmU Inhibitor Prediction

Welcome to the official repository and documentation overview for **GDOQ**, an open-source platform designed for predicting the inhibitory activity ($IC_{50}$) of chemical compounds against the bacterial target **GlmU protein**[cite: 3]. GlmU is a bifunctional enzyme essential for the survival of pathogens like *Mycobacterium tuberculosis*, making it a critical target for developing new drugs to fight antibiotic resistance[cite: 3].

**Web Server:** [(https://webs.iiitd.edu.in/raghava/gdoq/)]

---

## Citation

Singla, D., Anurag, M., Dash, D., & Raghava, G. P. S. (2011). 
**A web server for predicting inhibitors against bacterial target GlmU protein.** 
*BMC Pharmacology*, 11, 5. 
[https://doi.org/10.1186/1471-2210-11-5](https://doi.org/10.1186/1471-2210-11-5)

---

## About the Platform

GDOQ was developed to assist researchers in identifying novel inhibitors for the GlmU protein, particularly in the context of drug-resistant tuberculosis. The platform utilizes Quantitative Structure-Activity Relationship (**QSAR**) models and **docking** techniques to predict the effectiveness of potential drug candidates.

The platform's models are built on:
*   **Experimental Data**: A training set of 84 diverse GlmU inhibitors retrieved from PubChem BioAssay (AID 1376).
*   **Structural Modeling**: Site-specific docking against the $GlmU_{ecoli}$ crystal structure (PDB ID: 2O16).
*   **Comprehensive Descriptors**: Integration of docking energies, topological descriptors, and physiological descriptors.

---

## Key Features

### Predictive Modeling
*   **Hybrid QSAR Models**: Combines molecular descriptors from software like V-life, Web-Cdk, and Dragon with docking energy descriptors.
*   **High Performance**: Achieved a maximum correlation of $r=0.83$ ($r^2=0.70$) between predicted and actual $pIC_{50}$ values using hybrid models.
*   **Validation**: Models were optimized using Support Vector Machines (SVM), Multiple Linear Regression (MLR), and SMOreg.

### Built-in Tools
*   **Molecule Submission**: Users can draw structures using a JME editor, paste molecules in mol/mol2 format, or upload files directly.
*   **Interactive Results**: Predicts $IC_{50}$ values and provides interactive visualizations of the bound ligand within the GlmU protein.
*   **Lipinski Analysis**: Evaluates compounds based on the Lipinski rule of five to ensure drug-likeness.

### Data Resources
*   **Screened Libraries**: Contains lists of predicted potential GlmU inhibitors from anti-infective and substrate-similar compound libraries.
*   **Conservation Mapping**: Multiple sequence alignment highlighting conserved active site residues across different bacterial species[cite: 3].

---

## Overview of Model Development

GDOQ utilizes three primary types of descriptors to ensure accuracy[cite: 3]:
1.  **Docking Energy Descriptors**: Includes free energy, VdW + Hbond + desolv Energy, and electrostatic energy from AutoDock.
2.  **Molecular Descriptors**: Calculated using V-Life MDS 2.0 (1576 descriptors) and Web-Cdk (178 descriptors).
3.  **Hybrid Descriptors**: Integration of the above to encapsulate more chemical and biological information.

---

## Applications

*   **Drug Discovery**: Narrowing down time and cost by screening chemical libraries for potential tuberculosis treatments.
*   **Target Characterization**: Understanding protein-ligand interactions at the C-terminal domain of GlmU.
*   **Open Source Bioinformatics**: Promoting the use of freely available software in computer-aided drug discovery.

---

## Contact & Authors

Developed under the Open Source Drug Discovery (OSDD) initiative

Prof. Dr. Gajendra PS Raghava

raghava@iiitd.ac.in

---

## License

This platform and its associated research are distributed under the **Creative Commons Attribution License (CC BY 2.0)**.
