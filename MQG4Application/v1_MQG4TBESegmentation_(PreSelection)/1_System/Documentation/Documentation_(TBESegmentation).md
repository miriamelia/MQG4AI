---
tags: [{Name: Documentation}, {Intent: Overview}, {Applicability: AIAct}, {Usage Example: default_highrisk}]
---

## Documentation (AIRO)

This section provides an overview of required documentation, and MQG4AI is intended to provide the required information, which needs to be extracted and transformed into document-format.
The [Lifecycle implementation](../../2_Lifecycle/AI_Lifecycle.md), as well as [AI risks](../../3_RiskManagement/AI_Risks) define relevant information to fill documentation such as the instructions of use, or post-market monitoring information, for instance.

![](../../../../imgs/Document.png){width=800 height=}

An [overview how to organize AI Act conform documentation in form of AI cards](https://link.springer.com/chapter/10.1007/978-3-031-68024-3_3):

![](<../../../../imgs/AI System/Documentation.png>){width=800 height=}

#### Data - t.b.d.

- Data.has documentation (data requirements (e.g. IEEE standard on medical data quality - datasheet))
- Data.has documentation (characteristics of data - e.g. distribution, ... datasheet)
- InputData.has documentation (specification - data sheet)

#### Overall System - t.b.d.

AI System:

- has documentation (blueprint) \
  (internal layout of the product which is system is part of) (generally applicable - indicates a document related to an entity)
- has documentation (system design specification)
- has documentation (system architecture)
- has documentation (EU declaration of conformity)

#### Execution Environment

AI System:

- has execution environment (AI Hardware)
> Nvidia Quadro P6000 GPU system
- has component (tool)
> PyTorch version 2.4 and Python version 3.10


#### Post-Market Monitoring - t.b.d. Template contributes information

AI System:

- has documentation (description of post-market monitoring system)
- has post-market monitoring system (post-market monitoring system)

#### Risk Management (appended based on the overview introduced above) - t.b.d. Template contributes information

AI System:

- has documentation (description of risk management system)
- has post-market monitoring system (risk management system)

#### Testing - t.b.d.

AI System:

- has documentation (test log)
- has documentation (test report)

#### Use

AI System:

- has documentation (instruction of use):
  - levels of accuracy and the relevant accuracy metrics (not relevant to the user in this case)


![](../../../../imgs/Achalasia/UserManual.png){width=1000 height=}
  
- has documentation (installation instruction)

#### Install the Software

Run `EsophagusVisualizationSetup.exe` and follow the installation instructions.  
Additionally the model for the xray segmentation 'ModelAchalasia' [Zenodo website](https://zenodo.org/records/13980656?preview=1&token=eyJhbGciOiJIUzUxMiJ9.eyJpZCI6IjA3MGI0MjI0LWEyN2ItNDlkNC05YjgxLTBkZThlNzgzNTljYSIsImRhdGEiOnt9LCJyYW5kb20iOiI4N2U4MmUxOTc3YTk2NTYxMDFmMjdiNzMyMjQzYWRiMCJ9.ISNr53t3UU1rBfBdi6Iyo8qznD_iIQSOMYUj6afUhyQqGPQlrKrNkVhttZcLL-Vc1brNMbboOo1KlUMVxBc4bg) has to be downloaded and be saved in the C: folder. 
**Note**: You might need to temporarily disable your antivirus software during the installation process.  
Afterward, add EsophagusVisualization to your antivirus whitelist.
