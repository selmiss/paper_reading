# Title 
Uncertainty-Aware Optimal Transport for Semantically Coherent  Out-of-Distribution Detection
> Author: Fan Lu, Kai Zhu, Wei Zhai   Publisher: CVPR From: University of Science and Technology of China
## Background
OE loss function:

<img width="491" alt="image" src="https://github.com/user-attachments/assets/3a6bf0f9-04da-45ea-b879-ab853dd6863a" />

MCD（Maximum Classifier Discrepancy）:

Minimize the difference between 2 classifiers in ID data and maximize it in OOD data.

2 problems: OOD data is hard to distinguish; Overfit on OOD data; Fit on low-level features.
## TL;DR
- They propose an Uncertainty-Aware Optimal Transport (OT) scheme for SCOOD (Semantically Coherent Out-of-Distribution Detection).
- Core Idea: Assign pseudo-labels to unlabeled ID samples using an Energy-Based Transport (ET) mechanism that leverages energy scores as a measure of semantic consistency.
- Their method significantly reduces label noise and improves OOD detection performance, outperforming prior approaches by 27.69% and 34.4% on FPR@95%.
## Innovation
- Uncertainty-Aware Optimal Transport

Introduces energy-based transport (ET) to guide pseudo-labeling using energy scores instead of distance-based clustering.
Reduces the impact of covariate shifts that traditional clustering methods suffer from.

- Inter-Cluster Extension Strategy
  
Enhances feature representation to increase separation between ID and OOD clusters.
Uses contrastive learning to reduce intra-class variance and increase inter-class distance.

- T-Energy Score for OOD Detection

A refined energy-based OOD detection score, helping the model distinguish ID/OOD more effectively at test time.
Improves detection consistency across different datasets.

## Datasets/tasks

CIFAR-10 SCOOD Benchmark

CIFAR-100 SCOOD Benchmark

## Noteworthy Results

## Inspiration
Improved Safety in Autonomous Systems:
More accurate rejection of unknown inputs in self-driving cars and robotics.

Medical Image Analysis:
Helps detect rare or unknown diseases by better recognizing anomalies.

Security & Fraud Detection:
Can improve intrusion detection and fraud detection systems.
