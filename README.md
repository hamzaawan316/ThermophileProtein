# Thermophile Protein
This repository contains code, notebooks, and scripts used to develop and evaluate supervised machine learning and deep learning models for predicting thermophilic proteins from sequence and proteomic-derived features. The goal is to provide a reproducible pipeline for feature engineering, model training, hyperparameter tuning, evaluation, and explainable AI (XAI) analysis for biological insight.

#Motivation
Thermophilic proteins are proteins that remain stable and functional at high temperatures. Predicting whether a protein is thermophilic from sequence or proteomic signals has applications in biotechnology, industrial enzyme design, and understanding protein stability. This project builds a supervised learning framework to classify proteins as thermophilic vs mesophilic (or additional temperature-related classes), compare feature-based ML with end-to-end DL on sequences, and provide interpretable feature attributions.

#Dataset
Primary sources: Uniprot/SwissProt, Thermophile-specific databases.
Labels: thermophilic proteins (binary) by experimentally-determined optimum temperature or organism growth temperature. Optionally multi-class (e.g., psychrophilic / mesophilic / thermophilic).
Availability: The dataset is currently available upon request. Please contact Hamza Shahab Awan (hamzashahabawan@gmail.com / sp24-pcs-006@cuilahore.edu.pk) for access.

#Feature engineering
We implement multiple feature sets so you can compare which signals carry thermophilicity information. Specifically, we utilize a 153-dimensional genomic/protein-derived feature representation that captures rich statistical, positional, and physicochemical information:
Super Feature Vectors
Raw Moments
Central Moments of Statistical Distributions
PRIM (Position Relative Incidence Matrix)
RPRIM (Reverse PRIM)
AAPIV (Accumulative Absolute Position Incidence Vector)
RAAPIV (Reverse Accumulative Absolute Position Incidence Vector)
Hahn Moments
These engineered descriptors, combined with sequence- and structure-based representations, enable robust supervised learning and provide interpretable insights into thermophilic vs non-thermophilic protein discrimination.

Authors:


#Availability
The processed dataset and pre-trained models will be made available upon request. Contact: Hamza Shahab Awan (hamzashahabawan@gmail.com / sp24-pcs-006@cuilahore.edu.pk).


Recommended splits: stratified train/validation/test (e.g., 70/15/15) with non-redundant sequences across sets (remove high identity using CD-HIT or MMseqs2 at 30–40% identity to avoid homology bias).
