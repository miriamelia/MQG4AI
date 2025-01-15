---
tags: [{Name: Application}, {Intent: Overview}, {Applicability: AIAct}, {Usage Example: default_highrisk}]
---

## Application

This section provides an overview of the intended use case, it's capability, intended purpose and real world setting.
With respect to the *Lifecycle* implementation, this includes a domain knowledge collection that provides relevant information to all stakeholders, as well as ethical information regarding the application and its implementation.
This proposed structure follows AIRO, and this information is closely related with [Risk Analysis](../../3_RiskManagement/Procedure/a_Risk_Analysis/RiskAnalysis_(RiskManagement).md), and [AI Risks](../../3_RiskManagement/AI_Risks/).
Also, it needs to be [documented](../Documentation/Documentation.md)

- Based on classification for the application's Capability and Intended Purpose derive the Area of Impact.
- Locality of Use and Intended Workflow, Modality as well as AI Output specify the previous more general definition of the application.
- Human Involvement, Output Controllability, as well as Automation Level describe valuable information for risk management


#### AI System (AIRO)

- is applied within domain, e.g. (medicine), e.g. medical specialty + medical usage (ISO ISO/TR 24291) (relevant information to understand AI Output and Use within respective domain)
- is used in form of (AI System Form)
- has purpose (purpose)
- has capability (capability)


#### Relevant Information (AIRO)

##### 1. Domain

![Domain](<../../../imgs/AI Application (AIRO)/Domain.png>){width=800 height=}

Outlines the broadest definition of the system's application, which is specified with the following attributes.
In general, [Domain Knowledge](./DomainKnowledge/) provides important information for the concrete lifecycle implementation.


###### Example Domain Medicine 
→ based on ISO/TR 24291 on medical AI use cases to fill in the required information on the application

For Capability:
![Medical Specialty](<../../../imgs/AI Application (AIRO)/Medical Specialty.png>)

For Purpose:
![Medical Usage](<../../../imgs/AI Application (AIRO)/medical usage.png>)


##### 2. General overview:

AI System:

- has purpose (purpose)

###### - Purpose

![](<../../../imgs/AI Application (AIRO)/Purpose.png>){width=800 height=}


###### - Capability

AI System:

- has capability (capability):

e.g. classification, regression, anomaly detection, generation, object detection, multiple, ...

<br>

![](<../../../imgs/AI System/AI Capability.png>){width=800 height=}

###### - Area of Impact

![](<../../../imgs/AI Application (AIRO)/Area of Impact.png>){width=800 height=}

<br>

##### 3. Real-World Connection:

###### - Modality

<br> ![](<../../../imgs/AI Application (AIRO)/Modality.png>){width=600 height=}


###### - Locality of Use and Intended Workflow

![](<../../../imgs/AI Application (AIRO)/LocalityOfUse.png>){width=600 height=}

<br>

###### - AI Output

![](<../../../imgs/AI System/AI Output.png>){width=800 height=}

<br>

##### 5. [Human Agency & Oversight](../../3_RiskManagement/AI_Risks/1_HumanAgencyOversight/HumanAgencyOversight.md)

###### - Output Controllability

![Domain](<../../../imgs/AI Application (AIRO)/Output_Controllability.png>){width=800 height=}

<br>

###### - Automation Level

![Domain](<../../../imgs/AI Application (AIRO)/AutomationLevel.png>){width=800 height=}

<br>

###### - Human Involvement

![Domain](<../../../imgs/AI Application (AIRO)/HumanInvolvement.png>){width=800 height=}


<br>