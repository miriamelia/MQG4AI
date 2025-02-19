---
tags: [{Name: LackofCollaborationMechanisms}, {Intent: DiversityNon-DiscriminationFairness}, {Applicability: StakeholderParticipation}, {Usage Example: TBESegmentation}]
---

## Lack of a Domain Experts and Collaboration mechanisms
> Focus Domain Experts during Development - feedback loops
>> **Use case**:  [TBE Segmentation Achalasia](../../../1_System/Application/TBE_Segmentation.md)
>> **Result**: Establish feedback loops with medical domain experts
>> **Related Risks**: 
>> - May cause [Inaccurate Esophagus Segmentation](../../2_TechnicalRobustnessSafety/Accuracy/InaccurateModelOutput_(TBE_Segmentation).md)

### Risk Assessment (Risk Analysis + Risk Evaluation) 

#### Risk: *Collaboration mechanisms*

During system operation no communication channels are established and the physician interacting with the segmented esophagus shape can not feedback if he/she recognizes a decline in model performance, which might result in not applying the model.

#### Risk analysis

##### Severity of harm

The physician may not apply the model if he/she can not feedback on model utility.

##### Probability of Occurence

Depends on model performance

#### Risk evaluation

Acceptable if risk controls are implemented

#### Risk control

Establish feedback loops

###### Overview of related QGs and information sections:

- Maintenance:
    - Support:  Feedback Loops