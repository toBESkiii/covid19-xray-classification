COVID-19 Detection from Chest X-Rays

A deep learning system for automated COVID-19 detection and classification from chest X-ray images, implementing and benchmarking three CNN architectures in MATLAB on a dataset of 21,165 medical images.


The Problem

COVID-19 diagnosis from chest X-rays requires skilled radiologists and is time-consuming at scale. Automated deep learning systems can support clinical decision-making, reduce diagnostic workload on healthcare professionals, and improve access to timely diagnosis — particularly in under-resourced settings.

This project investigates which CNN architecture delivers the most reliable multi-class classification performance on a large, real-world medical imaging dataset.


Dataset

COVID-19 Radiography Database


Total images: 21,165 chest X-rays
Classes: 4

COVID-19
Normal
Lung Opacity
Viral Pneumonia






How It Works

Pipeline Overview

Raw X-Ray Images → Preprocessing → Model Training → Evaluation → Best Architecture

Stage 1 — Preprocessing


Resizing all images to a consistent input dimension
Normalisation to standardise pixel value ranges
Data augmentation (rotation, flipping, zoom) to improve generalisation and address class imbalance


Stage 2 — Model Architecture

Three CNN architectures were designed, implemented and evaluated:

ModelDescriptionCustom CNNBuilt from scratch — designed to establish a baseline without pretrained weightsResNet-50Deep residual network using transfer learning from ImageNet weightsEfficientNetCompound scaling architecture using transfer learning for improved efficiency

Stage 3 — Training & Evaluation


Structured train/validation/test data split
Each model trained, validated and tested independently
Performance evaluated using:

Accuracy
Precision
Recall
F1-Score
Confusion Matrix Analysis






Tech Stack

CategoryToolsLanguageMATLABArchitecturesCustom CNN, ResNet-50, EfficientNetTechniquesTransfer Learning, Data Augmentation, Image PreprocessingDatasetCOVID-19 Radiography DatabaseEvaluationAccuracy, Precision, Recall, F1-Score, Confusion Matrix


Project Structure

covid19-xray-classification/
│
├── README.md
├── src/                  ← MATLAB scripts and live scripts
└── results/              ← Confusion matrices and performance charts


Key Findings


Transfer learning architectures (ResNet-50 and EfficientNet) outperformed the custom CNN baseline
Data augmentation significantly improved model generalisation on the imbalanced dataset
Confusion matrix analysis revealed class-specific performance differences across COVID-19, Normal, Lung Opacity and Viral Pneumonia
Results demonstrate the potential of deep learning as a scalable, reliable support tool for COVID-19 radiograph diagnosis



What I Learned


How to design and benchmark multiple deep learning architectures on the same dataset
The importance of preprocessing pipelines and data augmentation in medical imaging
How transfer learning accelerates performance on domain-specific classification tasks
Why multi-metric evaluation (precision, recall, F1) matters more than accuracy alone in medical AI
