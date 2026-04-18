# Research Proposal: Signature-Based Detection of Subtle DDoS Attacks

## 📝 Project Overview
### Research Question
How can an iterative supervised machine learning framework, combining request-level signatures and system-level telemetry, improve the detection and generalization of subtle cloud-based attacks like EDoS?

### Motivation & Impact
* **Economic Risk**: EDoS attacks exploit pay-per-use and auto-scaling models by mimicking legitimate user behavior. Without proper mitigation, these attacks can increase service costs by over 300%, creating an immense financial burden for cloud consumers.
* **Security Bottleneck**: Traditional DDoS prevention often fails to identify low-rate, subtle attacks that blend into normal traffic patterns. 
* **Optimized Allocation**: Securing the environment is a prerequisite for efficient cloud management. Robust detection allows for near-optimal resource allocation, ensuring that system capacity is preserved for legitimate users rather than being drained by malicious actors.

## 🖼️ Research Posters
<p align="center">
  <img src="Research_Poster%20Prism.webp" alt="Research Poster" width="800">
</p>

## 🔬 Proposed Methodology
The proposal introduces an **iterative machine learning pipeline** designed to classify requests and refine detection accuracy over time:

* **Multi-Layered Feature Analysis:** The model is designed to analyze features across the Network (TCP/UDP size), System (CPU/Memory usage), and Application (Web request time) layers.
* **Iterative Model Refinement:** An initial Random Forest model classifies activity and identifies **Feature Importance**. These insights are then fed into a secondary AI model to tune the primary model's weights and features for the next iteration.
* **Signature-Based Classification:** Instead of standard IP filtering, the proposal focuses on turning traffic packets into unique signatures to improve the detection rate of anomalous behavior.

## 🧪 Experimental Setup
* **Traffic Simulation**: Utilizing **HTTPFlooder** and **LoadRunner** to generate a balanced dataset of benign user behavior and malicious flood patterns.
* **Environment**: A controlled **KVM-based** virtual environment to safely monitor system telemetry without external noise.
* **Benchmarking**: Evaluation against the **CIC-IDS2018** dataset to ensure the model's signatures remain robust against established real-world attack vectors.

## 📈 Expected Contributions
* **Improved Generalization:** The iterative approach aims to enhance the system's ability to detect novel and unseen attack signatures.
* **Proactive Defense:** By integrating request-level and resource-usage features, the model intends to outperform baseline reactive rate-limiting methods.
* **Broad Impact:** The framework is designed to extend beyond EDoS to broader cloud threats such as DeNy and Control-Plane DoS attacks.

## 📚 Key References
* **Somani et al.** (2017) - *Combating DDoS attacks in the cloud: Requirements, trends, and future directions.*
* **Baig et al.** (2016) - *A game theoretic approach for resource allocation in the presence of EDoS attacks.*
* **Lavin & Ahmad** (2015) - *Evaluating real-time anomaly detection algorithms: The Numenta Anomaly Benchmark.*

---
### 👥 Team & Acknowledgments
* **Research Team**: Olivier Denis, Hyde Yoo, **Min Son**, Lotus Kong
* **Mentor**: **Michalis Bachras**, 4th year Ph.D. Candidate, University of Toronto
* **Mentorship**: Conducted under the **PRISM Program** at the University of Toronto.


