---
tags: [{Name: AISystem}, {Intent: Overview}, {Applicability: AIAct}, {Usage Example: default_highrisk}]
---

## AI System: Timed Barium Esophagogran (TBE) Segmentation

The proposed draft to structure relevant AI System information is based on [AIRO](https://delaramglp.github.io/airo/) (which is currently a work in progress).


![AI System](<../../../imgs/AI System/AI System.png>){width=800 height=}


### Overview

- has licence: t.b.d.
- has version: v1
- has component (pre-trained system): no

#### [Application](Application/TBE_Segmentation.md)
- TBE Segmentation within a medical software for the [rare disease achalasia](./Application/DomainKnowledge/Achalasia.md)

#### [Compliance](Compliance/Compliance_(TBESegmentation).md)
- t.b.d.

#### [Documentation](Documentation/Documentation_(TBESegmentation).md)
- t.b.d.

#### [Stakeholder](Stakeholder/Stakeholder_(TBESegmentation).md)
- Active:
    - [Developer](./Stakeholder/1_Active/Developer_(ActiveStakeholder).md)
- Consulting:
    - [Physician](./Stakeholder/2_Consulting/Physician_(ConsultingStakeholder).md)
- Passive:
    - [Physician](./Stakeholder/3_Passive/Physician_(PassiveStakeholder).md)
    - [Patient](./Stakeholder/3_Passive/Patient_(PassiveStakeholder).md)

#### [AI Technique - Lifecycle Implementation](../2_Lifecycle/AI_Lifecycle.md)
- has lifecycle phase
    - Focus on Development
- uses technique
    - Model segmentation
- has training / testing / validation data
    - [Data preprocessing]()
- has input
    - TBE raw data and labeled masks [Design Input]()
- produces output
    - predicts esophagus segmentation in TBE image

#### [Risk Management](../3_RiskManagement/AI_RiskManagement_(TBE_Segmentation).md)
- has automation level
    - [human-in-the-loop](../3_RiskManagement/1_HumanAgencyOversight/HumanAgencyOversight_(TBE_Segmentation).md)
- has control over AI output
    - [human-in-the-loop](../3_RiskManagement/1_HumanAgencyOversight/HumanAgencyOversight_(TBE_Segmentation).md)
- has human involvement
    - [human-in-the-loop - automation bias](../3_RiskManagement/1_HumanAgencyOversight/HumanOversight/AutomationBias_(TBE_Segmentation).md)