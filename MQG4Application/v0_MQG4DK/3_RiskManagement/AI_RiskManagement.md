---
tags: [{Name: RiskManagement}, {Intent: Overview},  {Applicability: AIAct}, {Usage Example: default_highrisk}]
---


## Risk Management

A risk management system (RMS) section is included in MQG4AI to link risks with [AI Lifecycle](./../2_Lifecycle/AI_Lifecycle.md) implementation, and [AI System](./../1_System/AI_System.md) information, based on the procedure risk analysis (identification and estimation of risks and their sources), risk evaluation (with respect to pre-defined risk acceptance criteria), and risk control (implemented measures to mitigate likelihood and/or severity of risks). 
The EU AI Act defines requirements for a [RMS in Article 9](https://artificialintelligenceact.eu/article/9/), highlighting its continuous and iterative character, as well as the importance of testing procedures, which is envisioned to be addressed through MQG4AI interaction scenarios by design.

We propose a risk classification for AI risks, that are identified and structured based on AI trustworthiness criteria according to [ALTAI](https://digital-strategy.ec.europa.eu/en/library/ethics-guidelines-trustworthy-ai), as promoted by the [NIST AI Risk Management Framework](https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf). Further, we aim to outline a workflow how to assign known AI risks so that they are considered during indiviual AI projects.
The overall process is envisioned to be aligned with the [ALTAI requirements for risk management](./AI_Risks/7_Accountability/Accountability.md) to address risk related to the risk management process, and for [General Safety](./AI_Risks/2_TechnicalRobustnessSafety/TechnicalRobustnessSafety.md#general-safety) requirements for all identified risks in the context of the specific use case.

> - The MQG4AI-template is envisioned to contribute to risk mitigation through lifecycle planning and information formatting and linking.
> - [Procedure](./Procedure) for an overview of related components, as proposed by AIRO.
> - Towards a collection of [Known AI Risks](./AI_Risks) to support risk analysis organized according to Trustworthy AI criteria, and an exemplary illustration how to link risk controls with implementation for MQG4AI application scenarios. 

We believe the proposed structure is generic enough to be aligned with existing and novel AI risks.
For instance, the [AI Risk Repository](https://airisk.mit.edu/), or [Mitre Atlas](https://atlas.mitre.org/) focusing on [AI security and threats](./AI_Risks/2_TechnicalRobustnessSafety/TechnicalRobustnessSafety.md#resilience-to-attack-and-security), offer a solid starting point for risk analysis. 

#### General Requirements

##### Continuous and iterative character (AIRO)

Continuous, overall Risk Evaluation (including residual risk that may stay/occurr after a risk control is implemented)
> when is the system release-proof?

→ identify acceptance criteria
→ continuously update review
→ include post-production activities

<br>

##### Oveview Conventional Risk Management Process

The proposed risk management procedure is based on AIRO, which incorporates general risk management and ISO 31000 family (AIRO)
It also aligns with ISO 14971 Risk Management for Medical Devices for [risk analysis](./Procedure/a_Risk_Analysis/RiskAnalysis_(RiskManagement).md), [risk evaluation](./Procedure/b_Risk_Evaluation/RiskEvaluation_(RiskManagement).md), and [risk control](./Procedure/c_Risk_Control/RiskControl_(RiskManagement).md): 

![](../../imgs/Risk%20Management%20(AIRO)/Risk%20Management%20ISO%2014971.png)


