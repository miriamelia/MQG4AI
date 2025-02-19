---
tags: [{Name: InaccurateEsophagusSegmentation}, {Intent: TechnicalRobustnessSafety_Risk}, {Applicability: Accuracy}, {Usage Example: TBESegmentationAchalasia}]
---

## Inaccurate Esophagus Segmentation
>> **Use case**: [TBE Segmentation Achalasia](../../../1_System/Application/TBE_Segmentation.md)
>> **Result**: Feedback loops for physicians interacting with the software during maintenance
>> **Related risk** 
>> - Enforced by [Lack of domain experts](../../5_DiversityNon-DiscriminationFairness/StakeholderParticipation/LackofDomainExperts_(TBE_Segmentation).md) and [lack of collaboration mechanisms](../../5_DiversityNon-DiscriminationFairness/StakeholderParticipation/LackofCollaborationMechanisms_(TBE_Segmentation).md)
>> - May lead to [automation bias](../../1_HumanAgencyOversight/HumanOversight/AutomationBias_(TBE_Segmentation).md) and [waste of computing resources](../../6_SocietalEnvironmentalWellbeing/EnvironmentalWellbeing/WasteOfComputingResources_(TBE_Segmentation).md)

### Risk Assessment (Risk Analysis + Risk Evaluation) 

#### Risk: 

The risk *inaccurate esophagus segmentation* leads to the medical user possibly not using the segmentation model within the software, or having to adjust the segmented output more thoroughly, resulting in a more time-consuming 3D-reconstruction workflow.

This may result from multiple sources:
- insufficient labeled data during model development
- insufficient labeled data quality 
- unfitting model configuration
- data / model drift during model maintenance

> For risks based on misuse when integrating the inaccuracte esophagus segmentation within the 3D-reconstruction refer to [automation bias](../../1_HumanAgencyOversight/HumanOversight/AutomationBias_(TBE_Segmentation).md)

#### Risk analysis

##### Severity of harm
- 3D-reconstruction workflow is not optimized and physician interacting with the software may not apply the TBE segmentation model, resulting in a waste of resources

##### Probability of Occurence
- High, especially at the beginning of the project

#### Risk evaluation
- Acceptable in combination with measures as described under risk control - otherwise the model would probably not be applied and its implementation a waste of resources

#### Risk control

- collect more annotated data and retrain the model
- optimize the configured model including preprocessing during data utilization
- establish feedback mechanisms so that the treating physician may communicate an observed decline in model performance


###### Overview of related QGs and information sections:

- System:
    - Stakeholder: consulting physician provides information on interaction with model output
    - Documentation: user manual that introduces how to apply feedback loops, and educates on the risk of automation bias

- Lifecycle:
    - Data:
        - Acquisition: more high-quality labeled data
        - Utilization: select (and update) fitting preprocessing approach that optimizes model output

    - Development:
        - Configuration: select fitting architecture to start (Here, the intra-selection example is located)
        - Optimization: next, based on the previously selected model configuration, apply further optimization, e.g. preprocessing and other parameters for the training pipeline

     - Maintenance:
        - Support: Feedback Loops
        - Update: New Data

