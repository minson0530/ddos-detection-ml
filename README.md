# Research Proposal: Signature-Based Detection of Subtle DDoS Attacks

## 📝 Project Overview
This proposal, developed at the **University of Toronto (Computer Science Department)**, outlines a framework to protect cloud environments from **Economic Denial of Service (EDoS)** and subtle **DDoS** attacks. These threats are particularly critical because they mimic legitimate traffic to exploit auto-scaling models, resulting in unrecoverable financial losses for cloud users. Effective detection of subtle attacks serves as a prerequisite for secure cloud management, enabling more efficient resource allocation strategies.

## 🛠️ Proposed Technical Stack
* **Languages & Libraries:** Python, Scikit-learn (Random Forest).
* **Infrastructure:** KVM-based Virtual Machines hosting web servers and databases.
* **Simulation Tools:** HTTPFlooder and LoadRunner for generating malicious and benign traffic.
* **Evaluation Dataset:** CIC-IDS2018 for testing generalization across diverse attack scenarios.

## 🔬 Proposed Methodology
The proposal introduces an **iterative machine learning pipeline** designed to classify requests and refine detection accuracy over time:

* **Multi-Layered Feature Analysis:** The model is designed to analyze features across the Network (TCP/UDP size), System (CPU/Memory usage), and Application (Web request time) layers.
* **Iterative Model Refinement:** An initial Random Forest model classifies activity and identifies **Feature Importance**. These insights are then fed into a secondary AI model to tune the primary model's weights and features for the next iteration.
* **Signature-Based Classification:** Instead of standard IP filtering, the proposal focuses on turning traffic packets into unique signatures to improve the detection rate of anomalous behavior.

## 📈 Expected Contributions
* **Improved Generalization:** The iterative approach aims to enhance the system's ability to detect novel and unseen attack signatures.
* **Proactive Defense:** By integrating request-level and resource-usage features, the model intends to outperform baseline reactive rate-limiting methods.
* **Broad Impact:** The framework is designed to extend beyond EDoS to broader cloud threats such as DeNy and Control-Plane DoS attacks.

---
*Developed for the **PRISM** (Preparation for Research through Immersion, Skills, and Mentorship) program.*

**Research Team:** Olivier Denis, Hyde Yoo, **Min Son**, Lotus Kong  
**Mentor:** Michalis Bachras


