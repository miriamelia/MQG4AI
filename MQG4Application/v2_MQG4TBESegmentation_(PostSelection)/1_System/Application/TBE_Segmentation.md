---
tags: [{Name: TBE_Segmentation_Application}, {Intent: Overview}, {Applicability: AIAct}, {Usage Example: default_highrisk}]
---

## TBE_Segmentation within a Medcial Software *EsophagusVisualization* for the Rare Disease Achalasia (= Application)


- The segmentation model is applied within a medical software to enhance the 3D-reconstruction workflow to generate a novel data type, i.e. a multi-modal 3D-reconstruction of the esophagus tailored to the rare disease Achalasia
- The AI model is used in form of TBE-image segmentation
- [Information on Achalasia, a rare disease of the esophagus](./DomainKnowledge/Achalasia.md) 
- More information on the overall project:
    - [Overview](https://www.researchgate.net/publication/372490765_PRECISION_MEDICINE_FOR_ACHALASIA_DIAGNOSIS_A_MULTI-MODAL_AND_INTERDISCIPLINARY_APPROACH_FOR_TRAINING_DATA_GENERATION)

![Software](<../../../../imgs/Achalasia/AchalasiaSW.png>){width=800 height=}
> Multi-modal input based on which the 3D-reconstruction is generated

![SoftwareWF](<../../../../imgs/Achalasia/achalasiaWF.png>){width=800 height=}
> Human-in-the-loop workflow: the 3D-reconstruction is generated based on medical user input to map the data together

![SoftwareAlgorithm](<../../../../imgs/Achalasia/AlgorithmAchalasia.png>){width=800 height=}
> The Mapping-algorithm that generates the 3D-reconstruction

![SoftwareOutlook](<../../../../imgs/Achalasia/achalasia_dataset.png>){width=800 height=}
> Outlook: Data set creation based on medical data and the generated 3D-reconstructions, aiming to learn a GenAI model that generates 3D-reconstructions in real-time during endoscopy

#### Relevant Information on the AI System "TBE Segmentation" (AIRO)

##### 1. Domain

![Domain](<../../../../imgs/AI Application (AIRO)/Domain.png>){width=800 height=}

> Medicine - Medical Specialty: Medical research on the Rare Disease Achalasia of the Esophagus

##### 2. General overview:

AI System:

###### - Purpose

- has purpose (purpose)
> Enhance and accelerate 3D-reconstruction workflow within the medical software *EsophagusVisualization* (Prototype)

![](<../../../../imgs/AI Application (AIRO)/Purpose.png>){width=800 height=}

<br>

###### - Capability

AI System:

- has capability (capability):
> TBE-image segmentation

![](<../../../../imgs/AI System/AI Capability.png>){width=800 height=}

###### - Area of Impact

![](<../../../../imgs/AI Application (AIRO)/Area of Impact.png>){width=800 height=}

> Medical research on Achalasia patients (outlook: diagnosis and monitoring of treatment success)

<br>

##### 3. Real-World Connection:

###### - Modality

<br> ![](<../../../../imgs/AI Application (AIRO)/Modality.png>){width=600 height=}

> embedded within the medical software *EsophagusVisualization* (Prototype)


###### - Locality of Use and Intended Workflow

![](<../../../../imgs/AI Application (AIRO)/LocalityOfUse.png>){width=600 height=}

> Hospital, Center for Achalasia patients

<br>

###### - AI Output

![](<../../../../imgs/AI System/AI Output.png>){width=800 height=}

> TBE-image segmentation of the esophagus

<br>

##### 5. [Human Agency & Oversight](../../3_RiskManagement/AI_Risks/1_HumanAgencyOversight/HumanAgencyOversight_(TBE_Segmentation).md)

###### - Output Controllability

![Domain](<../../../../imgs/AI Application (AIRO)/Output_Controllability.png>){width=800 height=}

> High, the physician in charge can manually choose whether to apply the segmentation model and adjust the segmented shape

<br>

###### - Automation Level

![Domain](<../../../../imgs/AI Application (AIRO)/AutomationLevel.png>){width=800 height=}

> No degree of automation, human-in-the-loop approach

<br>

###### - Human Involvement

![Domain](<../../../../imgs/AI Application (AIRO)/HumanInvolvement.png>){width=800 height=}

> High, human-in-the-loop approach


<br>