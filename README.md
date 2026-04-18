# Signature-Based Detection of Subtle DDoS Attacks on Cloud

## 🚀 Project Overview
[cite_start]This research focuses on enhancing cloud security by detecting subtle **Economic Denial of Service (EDoS)** and **DDoS** attacks[cite: 5]. [cite_start]By utilizing an iterative machine learning approach, the framework refines its detection capabilities through the analysis of both request-level signatures and virtual machine (VM) telemetry[cite: 36, 45].

* [cite_start]**Research Question**: How can iterative supervised machine learning improve the generalization of detection for subtle cloud-based attacks like EDoS? [cite: 5, 7]
* [cite_start]**Motivation**: EDoS attacks mimic legitimate users to exploit auto-scaling models, causing irreversible financial damage to cloud consumers[cite: 12, 31, 34].
* **Institution**: University of Toronto, Computer Science Department.
* [cite_start]**Team**: Olivier Denis, Hyde Yoo, **Son Min**, and Lotus Kong[cite: 2].

## 🛠 Technical Methodology
The project employs a multi-stage pipeline to classify traffic and refine model accuracy:

1.  [cite_start]**Data Generation**: Benign and malicious traffic are simulated using **HTTPFlooder** and **LoadRunner** within a **KVM-based** virtual environment[cite: 46, 47, 73].
2.  [cite_start]**Feature Extraction**: The system extracts a diverse set of features[cite: 76, 78]:
    * [cite_start]**Network-Level**: TCP/UDP transfer sizes and IP packet sizes[cite: 79].
    * [cite_start]**System-Level**: CPU usage and memory requests from the VM[cite: 79].
    * [cite_start]**Application-Level**: Web server time and request types[cite: 79].
3.  **Iterative Model Refinement**: 
    * [cite_start]An initial **Random Forest** model (built with `scikit-learn`) classifies requests[cite: 78, 81].
    * [cite_start]**Feature Importance** is analyzed and passed to a secondary AI model[cite: 82].
    * [cite_start]The secondary model tunes the features and weights for the next iteration to optimize performance[cite: 83].

## 📊 Key Results & Evaluation
* [cite_start]**Performance Metrics**: The model is evaluated based on **Precision**, **Recall**, and **F1-score**[cite: 88].
* [cite_start]**Benchmarking**: The proposed model is compared against baseline methods, including rate-limiting and standard signature-based traffic classification[cite: 91].
* [cite_start]**Generalization**: Testing on the **CIC-IDS2018 dataset** ensures the model remains effective against novel attack signatures beyond the initial training set[cite: 95].

## 📖 Related Works
* [cite_start]**Abbasi et al.**: Suggested EDoS detection using virtual machine context[cite: 64, 97].
* [cite_start]**Dimolianis et al.**: Proposed signature analysis for traffic legitimacy[cite: 60, 106].
* [cite_start]**Baig et al.**: Implemented reactive rate-limiting based on past user activity[cite: 49, 101].

## 🎓 Acknowledgements
This research was conducted as part of the **PRISM** (Preparation for Research through Immersion, Skills, and Mentorship) program at the **University of Toronto**.
