# BiteNet Reproduction Study

This repository contains the reproducibility study for the paper [BiteNet: Bidirectional Temporal Encoder Network to Predict Medical Outcomes](https://arxiv.org/pdf/2009.13252). Our work is based on the original implementation provided by the authors, with modifications and re-implementation of the BiteNet model in PyTorch.

## Overview

BiteNet is a deep learning architecture designed to predict medical outcomes using electronic health records (EHR) data. The original implementation is written in TensorFlow/Keras, while our study re-implements the model in PyTorch, reproducing most of the results reported in the paper.

## Preprocessing

We borrowed the data preprocessing procedure from the original [BiteNet repository](https://github.com/Xueping/BiteNet) to process the MIMIC-III dataset. This preprocessing step extracts relevant patient data and organizes it into a structured format compatible with the BiteNet model. The processed data is saved in a file named `visit_dataset.pkl`.

To load the processed data correctly, the utility functions from the original implementation must be used. Ensure the dependencies are correctly set up to avoid errors during data loading.

## Our Contributions

The primary contributions of this repository include:
- A complete re-implementation of the BiteNet model in PyTorch.
- A Jupyter Notebook (`CSE6250_Final_Project.ipynb`) that includes the training, evaluation, and analysis of the model.
- Enhanced results in PR-AUC for the readmission prediction task, with detailed discussions of limitations and improvements for Precision@k metrics.

## File Structure

- `CSE6250_Final_Project.ipynb`: Main notebook containing the PyTorch implementation of BiteNet, training code, and result analysis.
- `visit_dataset.pkl`: Preprocessed data file generated using the original preprocessing procedure.

## Dependencies

To reproduce the results, you will need the following:
- Python 3.8+
- PyTorch 1.9+
- Torchvision
- NumPy
- Matplotlib
- scikit-learn
