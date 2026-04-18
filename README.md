# Signature-Based Detection of Subtle DDoS Attacks

## Project Overview

### Research Question
The primary goal of this research is to determine how an iterative supervised machine learning framework—utilizing both request-level signatures and system-level telemetry—can improve the detection and generalization of subtle cloud-based attacks like EDoS.

### Motivation
Cloud environments often struggle with Economic Denial of Service (EDoS) attacks, which exploit auto-scaling features by mimicking legitimate traffic patterns. These attacks are particularly damaging because they can increase service costs by over 300%, creating significant financial strain for cloud consumers. 

Traditional DDoS mitigation tools frequently overlook these low-rate attacks because they blend into normal traffic. Establishing a robust detection layer is a fundamental requirement for secure cloud management. By securing the environment first, we enable near-optimal resource allocation strategies that ensure system capacity serves legitimate users rather than malicious actors.

## Research Poster
<p align="center">
  <img src="Research_Poster%20Prism.webp" alt="Research Poster" width="800">
</p>

## Proposed Methodology
The proposed framework utilizes an iterative machine learning pipeline to refine detection accuracy through several stages:

* **Multi-Layered Feature Analysis**: We analyze data across the network (TCP/UDP size), system (CPU and memory utilization), and application layers (web request time and types).
* **Iterative Model Refinement**: An initial Random Forest model classifies traffic and identifies the most relevant features. This feedback is then used by a secondary model to adjust weights and feature selection for the next detection cycle.
* **Signature-Based Classification**: Rather than simple IP-based filtering, the system generates unique signatures from traffic packets to identify malicious patterns that mimic benign behavior.

## Experimental Setup
* **Traffic Simulation**: We use HTTPFlooder and LoadRunner to generate datasets containing both benign user behavior and malicious flood patterns.
* **Environment**: A controlled KVM-based virtual environment is used to monitor system telemetry alongside web server logs.
* **Benchmarking**: The model is evaluated against the CIC-IDS2018 dataset to test its resilience against real-world attack vectors.

## Expected Contributions
* **Improved Generalization**: The iterative approach allows the system to detect novel attack signatures that traditional reactive methods miss.
* **Proactive Security**: Integrating resource-usage telemetry provides a more robust defense against subtle threats like DeNy and Control-Plane DoS attacks.

---

### Team & Mentorship
* **Research Team**: Olivier Denis, Hyde Yoo, **Son Min**, Lotus Kong
* **Mentor**: **Michalis Bachras**, 4th year Ph.D. Candidate, University of Toronto
* **Program**: Conducted as part of the **PRISM** program at the University of Toronto.

