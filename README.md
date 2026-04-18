# Iterative ML-Based DDoS Detection in Cloud Systems

## Overview
This project investigates detecting subtle DDoS and EDoS attacks in cloud environments using a signature-based machine learning approach with iterative model refinement.

## Motivation
Traditional DDoS detection methods struggle with low-rate and economically-driven attacks (EDoS) that closely resemble legitimate traffic.  
This project aims to improve detection accuracy by combining request-level signatures with virtual machine (VM) resource metrics.

## Key Idea
Instead of using a static model, this project:
- Extracts features from both **network traffic** and **VM behavior**
- Trains a supervised ML model to classify requests
- Uses **feature importance** to iteratively refine the model
- Improves performance over multiple training cycles

## Methodology

### Data Simulation
- Virtual environment using KVM
- Generated benign and malicious traffic:
  - HTTPFlooder
  - LoadRunner

### Feature Extraction
- **Network-level**
  - TCP/UDP size
  - Packet size
- **System-level**
  - CPU usage
  - Memory usage
- **Application-level**
  - Request type
  - Web response time

### Model
- Supervised learning (Random Forest – scikit-learn)
- Binary classification: *Malicious vs Benign*

### Iterative Refinement
- Analyze feature importance
- Adjust feature set and model weights
- Retrain model across multiple iterations

## Evaluation
- Metrics:
  - Precision
  - Recall
  - F1-score
- Compared with:
  - VM-based ML models
  - Signature-based detection
  - Rate-limiting approaches

## Generalization
Tested on external dataset:
- CIC-IDS2018 (real-world DDoS scenarios)

## Results
*(Update this section when you have results)*
- Expected: improved detection of low-rate and stealthy attacks
- Better generalization across different DDoS types

## Tech Stack
- Python
- scikit-learn
- KVM (virtual machines)

## Repository Structure
