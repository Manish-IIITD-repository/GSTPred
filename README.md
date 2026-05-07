# GSTPred: Prediction of Glutathione S-Transferase Proteins

Welcome to the official documentation for **GSTPred**, a specialized computational tool developed for the prediction and functional annotation of Glutathione S-transferase (GST) proteins[cite: 1900]. [cite_start]GSTs are a ubiquitous enzyme superfamily essential for detoxification, stress survival, and drug resistance in both prokaryotes and eukaryotes.

**Web Server:** (https://webs.iiitd.edu.in/raghava/gstpred/) 

---

## Citation

Nitish Kumar Mishra, Manish Kumar and G.P.S. Raghava (2007).
**Support Vector Machine Based Prediction of Glutathione S-Transferase Proteins.**
*Protein & Peptide Letters*, 14(6), 575-580.10.2174/092986607780990046

---

## About the Platform

[cite_start]GSTPred was developed to overcome the limitations of traditional similarity-based searching (like BLAST or FASTA), which often fail to identify novel proteins that lack significant sequence similarity to known databases.The platform utilizes Support Vector Machines (SVM) to classify proteins based on global sequence features, specifically amino acid composition and local order.

The platform is designed to:
* **Annotate Genomes**: Provide high-speed functional assignment for uncharacterized protein products in the post-genomic era.
* **Support Drug Discovery**: Identify targets for asthma, cancer, and HIV, where GSTs play a central role in drug metabolism.
* **Analyze Resistance**: Help researchers understand anti-cancer drug resistance related to the overexpression of specific GST classes, such as GST π.

---

## Key Features

### Predictive Modeling
* **Machine Learning**: Built using the `SVM_light` package with a Radial Basis Function (RBF) kernel, which proved superior to linear and polynomial kernels for this task.
* **High Performance**: 
    * **Amino Acid Composition**: Achieved 91.59% accuracy.
    * **Dipeptide Composition**: Achieved 95.79% accuracy.
    * **Tripeptide Composition**: Achieved a maximum accuracy of **97.66%**, outperforming traditional HMM-based profile searching (96.26%).
* **Validation**: Evaluated using a rigorous five-fold cross-validation technique on a non-redundant dataset.

### Integrated Features
* **Compositional Analysis**: Encapsulates 20-dimensional (amino acid), 400-dimensional (dipeptide), and 8000-dimensional (tripeptide) vectors to capture both frequency and local sequence order.
* **N-terminal Analysis**: Incorporates findings that the N-terminal of GSTs is rich in Tyr, Ser, and Gly, which are essential for active site interactions with Glutathione (GSH).

---

## Overview of Model Development

The training dataset consisted of 107 experimentally annotated GST proteins and 107 non-GST proteins, filtered using CD-HIT to ensure no two proteins shared more than 90% sequence identity.

| Approach | Threshold | Sensitivity | Specificity | Accuracy | MCC |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Mono-peptide** | 0.2 | 91.59% | 91.59% | 91.59% | 0.83 |
| **Di-peptide** | 0.0 | 96.26% | 95.33% | 95.79% | 0.92 |
| **Tri-peptide** | -0.2 | **97.20%** | **98.13%** | **97.66%** | **0.95** |

---

## Applications

* **Cancer Research**: Identifying GST π as a prominent marker for cancer and studying its role in drug resistance and apoptosis.
* **Immunology**: Investigating how GST levels indirectly regulate cellular immune responses by controlling GSH levels, which determine Th1 or Th2 response patterns.
* **Broad-Spectrum Use**: Finding GST proteins across diverse organisms including prokaryotes and eukaryotes (animals, plants, and fungi).

---

## Contact & Support

**Prof. G.P.S. Raghava** Bioinformatics Center, Institute of Microbial Technology (IMTECH), Chandigarh, India  
**Email**: raghava@imtech.res.in 
**Tel**: +91-172-2690557 

---

## Acknowledgement

[cite_start]The authors are thankful to the Council of Scientific and Industrial Research (CSIR) and the Department of Biotechnology (DBT), Government of India, for financial support[cite: 2233].
