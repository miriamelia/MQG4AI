---
tags: [{Name: WasteOfComputingResources}, {Intent: TAI-criteria}, {Applicability: Specific TAI Criteria Section}, {Usage Example: TBESegmentation}]
---

## Waste of Computing Resources

>> **Use case**: [TBE Segmentation Achalasia](../../../1_System/Application/TBE_Segmentation.md)
>> **Result**: Segmentation model performance as high as possible
>> **Related risk** 
>> - May be caused by [inaccurate model output](../../2_TechnicalRobustnessSafety/Accuracy/InaccurateModelOutput_(TBE_Segmentation).md)
>> - May be enforced by [lack of communication channels](../../5_DiversityNon-DiscriminationFairness/StakeholderParticipation/LackofCollaborationMechanisms_(TBE_Segmentation).md)


### Risk Assessment (Risk Analysis + Risk Evaluation) 

#### Risk: *Waste of computing resources*

If the model does not perform sufficiently, the physician in charge may not apply it and thus the model was trained and developed in vain, wasting computing resources.

#### Risk analysis

##### Severity of harm

Loss of computing resources 

##### Probability of Occurence

- depends on physicians and model performance

#### Risk evaluation

- Acceptability in accordance with physicians who interact with the model - they need to continuously approve performance
- can be mitigated through model updates until the physicians are satisfied 
- and as soon as the physicians recognize a decline in performance impacting applicability

#### Risk control

Enhance model performance and establish communication channels so that the physicians interacting with the model can feedback whether model application is reasonable.


###### Overview of related QGs and information sections:

- Maintenance:
    - Support: Feedback Loops
    - Update: New Data

- Development:
    - Configuration: select fitting architecture to start (Here, the intra-selection example is located)
    - Optimization: next, based on the previously selected model configuration, apply further optimization, e.g. preprocessing and other parameters for the training pipeline