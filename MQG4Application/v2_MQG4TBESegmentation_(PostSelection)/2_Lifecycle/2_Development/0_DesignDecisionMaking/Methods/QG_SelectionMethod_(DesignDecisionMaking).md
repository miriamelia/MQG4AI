---
tags: [{Name: QG_SelectionMethod}, {Intent: Reliable_DesignDecisionMaking}, {Problem: ModelComplexity_UseCaseSpecificity_Interdependencies}, {Solution: Iterative_SelectionMethod}, {Applicability: AILifecycle_DesignDecisions}, {Consequences: TestingByDesign_MultipleIterations}, {Usage Example: PerformanceMetricsCompilation_EmergencyMedicine_Electrocadriogram(ECG)}]
---

## QG Selection Method (Design Decision Making)

### 1. Interdependency Graph

#### Input Information
> What information is necessary to execute the method and generate the content?

- Identify the relevant lifecycle design decision (e.g. which performance metrics compilation)
- Identify reasonable testing strategies tailored to the individual stages of the method (pre-, intra-, post-)

- ##### Related QGs
    > Which stages are required? What pre-requisites exist so the content dimension can be applied?

    - [Lifecycle](../../../../2_Lifecycle/AI_Lifecycle.md)-QGs, specification depends on the design decision

- ##### AI System Information
    > Which AI system-specific information is relevant so the content dimension can be applied?

    - [Application and Domain Knowledge](../../../../1_System/Application/)
    - [Lifecycle](../../../../2_Lifecycle/AI_Lifecycle.md)-QGs, specification depends on the design decision

#### Output Information 
> What information is produced that is relevant to other stages and design decisions?

- Reliable design decision making through an iterative process that includes multiple views on the respective design decision, aiming to implement testing by design

- ##### Related QGs
    > Which stages are impacted and which additional information might be necessary?

    - [Lifecycle](../../../../2_Lifecycle/AI_Lifecycle.md)-QGs, specification depends on the design decision

- ##### Post-Market Monitoring Information (Maintenance Stage)
    > Is there relevant information for post-market monitoring?

    - Depends on the design decision

<br>

### 2. Quality Gate Creation (Design-Decision-Specific Dimensions)

#### Dimension 1: Content
> Which information is generated?

A method for reliable design decision making along the AI lifecycle, structured into pre-, intra-, and post-selection steps to structure important directions of thought for design decision making concept planning, and monitoring of desired results.

![](../../../../../imgs/ECGPerformanceMetrics/designdecisionmaking_method_general.png){width=600 height=}

##### Example [Multi-Label ECG classification in an emergency setting](../../../../1_System/Application/example_ECGAlarmingGuardFunctionality_(EmergencyMedicine).md):

![](../../../../../imgs/ECGPerformanceMetrics/design_decision_making_method.png){width=600 height=}

#### Dimension 2: Method
> How is the information generated? (evaluation of content)

- Identified based on a retro-spective, empirical analysis to create a reliable performance metrics selection for a fictional use case centered around [multi-Label ECG classification in an emergency setting](../../../../1_System/Application/example_ECGAlarmingGuardFunctionality_(EmergencyMedicine).md)

#### Dimension 3: Representation
> Which information should be presented to which stakeholders and when?

Relevant during project conceptualization and planning, as well as implementation of AI lifecycle design decisions, and for compliance

##### - Stakeholder AI experts
##### - Stakeholder Data scientists
##### - Stakeholder Quality manager
##### - Stakeholder ...

<br>

#### Evaluation
> What are open questions when applying the generated content?

Method needs to be tested further for other design decisions and use cases


<br>


### 3. Additional Information

#### Risk Management

- ##### Poses Risk(s)
    > Are there related risks?

- ##### Implements Risk Control(s)
    > Are there risk controls implemented?

    - contribution to addressing [unreliable performance evaluation metrics](../../../../3_RiskManagement/AI_Risks/2_TechnicalRobustnessSafety/Accuracy/UnreliablePerformanceMetrics.md) adding an iterative method that addresses lifecycle-specific interdependency information management
        - Related risk [lack of domain experts](../../../../3_RiskManagement/AI_Risks/5_DiversityNon-DiscriminationFairness/StakeholderParticipation/LackofDomainExpertsCollaborationMechanisms.md)

#### ...
