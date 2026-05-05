# 690U_Final_Project

# Enzyme Function Prediction from Protein Sequences

This project evaluates enzyme commission (EC) classification from protein sequences using the DGEB EC classification benchmark. We compare logistic regression models with handcrafted sequence features against a homology-based BLAST baseline.

## How to Run

All notebooks were run in **Google Colab**. A CPU runtime is enough. No GPU is required.

## Project Overview

The goal of this project is to answer the following question:

# Enzyme Function Prediction from Protein Sequences

This project studies enzyme commission (EC) classification from protein sequences using the DGEB EC classification benchmark. The main goal is to compare simple handcrafted sequence representations, pretrained protein embeddings, and a classical homology-based method for enzyme function prediction.

## Research Question

**Which sequence representation works best for EC prediction, and how do handcrafted logistic regression models and ESM-2 embedding-based logistic regression compare with a homology-based BLAST baseline?**

We tested five methods:

1. Logistic Regression with amino acid frequency features
2. Logistic Regression with dipeptide frequency features
3. Logistic Regression with 3-mer count features
4. DGEB ESM-2 protein sequence embeddings baseline
5. BLAST Top-1 homology-based baseline

The final results showed that the 3-mer logistic regression model performed best among the handcrafted feature models. The ESM-2 embedding baseline performed substantially better than all handcrafted representations, while BLAST achieved the strongest performance overall on covered test samples.

## Final Results

| Method | Accuracy | Macro F1 | Weighted F1 |
|---|---:|---:|---:|
| Amino acid frequency + Logistic Regression | 0.0938 | 0.0605 | 0.0605 |
| Dipeptide frequency + Logistic Regression | 0.1641 | 0.1187 | 0.1187 |
| 3-mer count + Logistic Regression | 0.1875 | 0.1477 | 0.1477 |
| DGEB baseline | 0.4453 | 0.3937 | 0.3937 |
| BLAST Top-1 homology baseline | 0.9718 | 0.9537 | 0.9671 |

Note: The BLAST result is reported on covered test samples *ONLY* with valid sequence-similarity hits under the selected E-value threshold.

## Repository Structure

```text
.
├── README.md
├── amino_acid_frequency_logistic_regression.ipynb
├── dipeptide_frequency_logistic_regression.ipynb
├── kmer_logistic_regression.ipynb
├── dgeb_baseline.ipynb
└── blast_homology_baseline.ipynb



