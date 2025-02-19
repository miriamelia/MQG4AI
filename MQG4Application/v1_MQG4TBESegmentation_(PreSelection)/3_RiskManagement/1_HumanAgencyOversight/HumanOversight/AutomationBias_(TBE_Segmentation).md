---
tags: [{Name: AutomationBias}, {Intent: HumanAgencyOversight_Risk}, {Applicability: HuamnOversight}, {Usage Example: TBESegmentation}]
---

## Automation bias
>> **Use case**:  [TBE Segmentation Achalasia](../../../1_System/Application/TBE_Segmentation.md)
>> **Result**: Awareness creation among the physician in charge who interacts with the software
>> **Related Risks**: 
>> - May be caused by [Inaccurate Esophagus Segmentation](../../2_TechnicalRobustnessSafety/Accuracy/InaccurateModelOutput_(TBE_Segmentation).md)

### Risk Assessment (Risk Analysis + Risk Evaluation) 

#### Risk: 

> The physician in charge who interacts with the segmentation model blindly trusts the generated mask, without corrective adjustments when necessary

#### Risk Analysis

##### Severity of harm

> Negatively impacts the accuracy of the generated 3D reconstruction which impacts medical research and one day patient well-being

##### Probability of Occurence

> Depends on [physician interacting with the software](../../../../1_System/Stakeholder/3_Passive/Physician_(PassiveStakeholder).md)

#### Risk Evaluation

> This is an acceptable risk, in combination with risk control of creating awarenss, since the  [physician interacting with the software](../../../../1_System/Stakeholder/3_Passive/Physician_(PassiveStakeholder).md) is trained regarding the recognition of the esophagus in TBE images and the probability is high that they will adjust the correct shape

#### Risk control

> Create awareness that the segmentation model may not perform correctly, and its application may be skipped if desired by the  [physician interacting with the software](../../../../1_System/Stakeholder/3_Passive/Physician_(PassiveStakeholder).md) through documentation

###### Overview of related QGs and information sections:

- System
    - Documentation: 
        - [user manual](../../../1_System/Documentation/Documentation_(TBESegmentation).md)