# Artificial Intelligence (AI) - Risk Management - [EU-AIAct] requirements

## Purpose of the Document

This document only extracts **the requirements on risk management included in the [EU-AIAct]**.

## Foreword

This document is part of a [set of methodological documents](https://github.com/matthieu-grall/ai), under continuous improvement, designed to help organizations manage AI-related risks, and which can be useful together or separately.
The [reference documents](https://github.com/matthieu-grall/ai/blob/main/fr/IA%20-%20Gestion%20des%20risques%20-%20Documents%20de%20r%C3%A9f%C3%A9rence.md) are used in brackets within the document body.

It is placed under the following **license**:
_[Creative Commons Attribution 4.0 International License][cc-by]_.

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg

The main **contributors** are as follows:
- Matthieu GRALL.

The document **versions** are as follows:
| <center>Version</center> | <center>Action</center> | <center>Editor</center> |
| --- | --- | --- |
| 21/04/2026 (v0.1) | Create a synthesis on requirements of [EU-AIAct] on risk management | Matthieu GRALL |

## Introduction

This document can be used by companies who need to know what are their obligations.
They can filter the list of requirements depending on their role and specific circumstances (AI system type, stage in life cycle, etc.).

## Requirements on risk management

The following table provides an extract of the [EU-AIAct]'s requirements on risk management and, for each of them, adds the role responsible for its implementation and precisions on the applicability:

| **Exact reference** | **Topic** | **Requirement (summary)** | **Responsible** | **Application** |
| --- | --- | --- | --- | --- |
| Article 9(1) | Risk Management System | Establish, implement, document, and maintain a risk‑management system throughout the lifecycle. | Provider | Applies to all high‑risk AI systems. |
| Article 9(2) | Risk Management System | Identify and analyse known and foreseeable risks to health, safety, and fundamental rights. | Provider | Mandatory for all high‑risk systems. |
| Article 9(3) | Risk Management System | Test and evaluate risk‑mitigation measures before placing the system on the market. | Provider | Applies pre‑market and during updates. |
| Article 9(4) | Risk Management System | Apply a hierarchy of risk controls: eliminate risks, implement safeguards, provide warnings. | Provider | Applies when risks cannot be fully eliminated. |
| Article 9(5) | Risk Management System | Ensure the RMS is a continuous, iterative process updated throughout the lifecycle. | Provider | Applies during development, deployment, monitoring, and post‑market phases. |
| Article 10(2) | Data Governance | Assess and mitigate risks arising from training, validation, and testing data, including bias. | Provider | Applies when data quality affects safety or fundamental rights. |
| Article 10(3) | Data Governance | Ensure datasets are relevant, representative, free of errors, and appropriate for intended purpose. | Provider | Applies to all high‑risk systems using data‑driven models. |
| Article 14(1) | Human Oversight | Design human oversight to prevent or minimise risks to health, safety, and fundamental rights. | Provider | Applies to all high‑risk systems. |
| Article 14(4) | Human Oversight | Ensure human overseers can interpret outputs, detect anomalies, and intervene to reduce risks. | Provider / Deployer | Applies where human oversight is required by design. |
| Article 15(1) | Robustness & Cybersecurity | Ensure the system is robust, resilient to errors, faults, and malicious attacks. | Provider | Applies to all high‑risk systems. |
| Article 15(3) | Cybersecurity | Implement cybersecurity controls proportionate to risks, including protection against data poisoning and model manipulation. | Provider | Applies especially to ML‑based systems exposed to adversarial threats. |
| Article 16(1)(a) | Conformity Assessment | Ensure compliance with Articles 9–15, including all risk‑related requirements. | Provider | Applies before placing the system on the market. |
| Article 16(5) | Post‑Market Monitoring | Implement a post‑market monitoring system to collect, document, and analyse performance and risks. | Provider | Applies after deployment; continuous obligation. |
| Article 26(1) | Deployment Risk Controls | Use the system according to instructions and ensure human oversight is effectively implemented. | Deployer | Applies to all deployers of high‑risk systems. |
| Article 26(2) | Input Data Risk | Ensure input data is relevant and appropriate to avoid risk amplification. | Deployer | Applies when deployers supply input data. |
| Article 27(1) | FRIA | Conduct a Fundamental Rights Impact Assessment before deploying a high‑risk AI system. | Deployer (public sector + certain private entities) | Applies to public authorities and private entities performing tasks of public interest. |
| Article 27(2) | FRIA | FRIA must identify affected groups, risks, mitigation measures, and monitoring mechanisms. | Deployer | Applies before deployment; must be updated if system changes. |
| Annex III | High‑Risk Classification | Determines whether RMS and FRIA obligations apply by defining high‑risk categories. | Provider / Deployer | Applies only to systems listed in Annex III or under Annex I product safety legislation. |
| Annex IV | Technical Documentation | Must include risk‑management documentation, testing results, and mitigation strategies. | Provider | Applies to all high‑risk systems undergoing conformity assessment. |