# 690U_Final_Project

# Enzyme Function Prediction from Protein Sequences

This project evaluates enzyme commission (EC) classification from protein sequences using the DGEB EC classification benchmark. We compare logistic regression models with handcrafted sequence features against a homology-based BLAST baseline.

## How to Run

All notebooks were run in **Google Colab**. A CPU runtime is enough. No GPU is required.

## Project Overview

The goal of this project is to answer the following question:

**Which simple handcrafted sequence representation works best for EC prediction, and how does the best logistic regression model compare with a homology-based BLAST baseline?**

We tested four methods:

1. Logistic Regression with amino acid frequency features
2. Logistic Regression with dipeptide frequency features
3. Logistic Regression with 3-mer count features
4. BLAST Top-1 homology-based baseline

The final results showed that the 3-mer logistic regression model performed best among the handcrafted feature models, while BLAST achieved much stronger performance overall.

## Final Results

| Method | Accuracy | Macro F1 | Weighted F1 |
|---|---:|---:|---:|
| Amino acid frequency + Logistic Regression | 0.0938 | 0.0605 | 0.0605 |
| Dipeptide frequency + Logistic Regression | 0.1641 | 0.1187 | 0.1187 |
| 3-mer count + Logistic Regression | 0.1875 | 0.1477 | 0.1477 |
| BLAST Top-1 homology baseline | 0.9718 | 0.9537 | 0.9671 |

## Repository Structure

```text
.
├── README.md
├── amino_acid_freq.ipynb
├── dipeptide_freq.ipynb
├── 3_mers.ipynb
└── homology_based_baseline.ipynb

