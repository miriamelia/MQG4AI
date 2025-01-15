---
tags: [{Name: UnreliablePerformanceMeasurement}, {Intent: TechnicalRobustnessSafety_Risk}, {Applicability: Accuracy}, {Usage Example: EmergencyMedicine_Electrocardiogram}]
---

## Unreliable Performance Measurement (Technical Robustness and Safety_Inaccurate Measurements - Risk)
> Focus on accurate and reliable performance evaluation metrics to illustrate how implemented Quality Gates are linked with regulatory requirements through AI risk management
>> **Use case**: [Custodian functionality of multi-label classifier in an emergency setting](../../../../1_System/Application/example_ECGAlarmingGuardFunctionality_(EmergencyMedicine).md)
>> **Result**: Domain-embedded performance evaluation strategy during the model development stage based on the [Quality Gate format](../../../../../templates/Template_LeafQG.md) which includes information extraction for other related system requirements, lifecycle stages and design decisions.
>> **Related risk** [Lack of Domain Experts](../../DiversityNon-DiscriminationFairness/StakeholderParticipation/LackofDomainExpertsCollaborationMechanisms.md)

### Risk Assessment (Risk Analysis + Risk Evaluation) 

#### Risk: Unreliable performance evaluation metrics

The hazard of incorrect measurement information (as mentioned by ISO 14971 (comp. 35) for medical device risk management) can be transferred to performance evaluation metrics:
- The sequence of events includes wrong measurements that are not detected by the user (or other stakeholders) and result in the hazardous information that leads to misinterpretation based on incorrect information, which can result in harmful actions.

#### Risk evaluation

##### Severity of harm
Performance evaluation metrics comprise the foundation for further testing, design decision-making, and any situation where the model's performance is evaluated. They need to be sound, aligned with the intended real world setting of the system, and their interpretation explained. Consequently, an unreliable performance evaluation strategy poses a very high risk, since it runs through the entire project.

##### Probability of Occurence
High if misunderstanding of the (evolving) data distribution, application domain, and use case-adapted tuning objectives.

#### Risk control

Reliable performance metrics including their sound interpretation are crucial for risk mitigation. Generally, their evaluation depends on the respective use case and is prone to evolving in time, which implies an evaluation of suitable metrics with respect to the individual data set composition, and tuning objective, as well as a monitoring strategy adapted to different stakeholder views, including additional material for a more profound interpretation.


##### Example: reliable multi-Label ECG classification performance metrics compilation
The risk *unreliable performance evaluation metrics* is addressed by a comprehensive performance metrics selection strategy that addresses these questions by including relevant domain knowledge, considering the label count in the data, and is embedded within other lifecycle interdependencies.

During *Lifecycle Development*, the *Model Training*, *Evaluation*, and *Optimization* stage are addressed in an iterative manner, and related with *System Application information*, and the *Data* stage to conclude the performance evaluation strategy. Possible extensions that may extend the *Model Explanation* stage are also addressed.
Relevant information is extracted for the *Deployment* and *Maintenance* stages in relation to the label distribution in the data, which, if updated triggers the recalculation of evaluation thresholds for post-market monitoring. Further information is extracted with respect to identified stakeholders that consult the calculated metrics along the lifecycle.
The proposed evaluation strategy is intended to be generalizable across use cases, possibly excluding multi-label-specific or classification-specific Quality Gate realizations.

###### The following strategy for risk mitigation is outlined:

- Pre-requisites include an analysis of the data distribution, which is characterized by high data imbalance, and impacts the metrics' performance, in case of this example, an open-source data set was used [Physionet](../../../../2_Lifecycle/2_Development/0_DesignDecisionMaking/OpenSource_Data/QG_Physionet_(MultiLabelECG).md), and only basic preprocessing was performed.
Further, a [Domain Expert](../../../../1_System/Stakeholder/2_Consulting/DomainExpert_(ConsultingStakeholder).md) was consulted to support the interpretation of model performance in the intended real world setting.
- The [iterative design decision method](../../../../2_Lifecycle/2_Development/0_DesignDecisionMaking/Methods/QG_SelectionMethod_(DesignDecisionMaking).md) is based on a [use case-adapted label structure](../../../../2_Lifecycle/1_Data/2_Utilization/2_Preprocessing/2_Transformation/QG_LabelStructure_(MultiLabelClassificationPreprocessing).md), and the derivation of [domain-embedded per-label tuning objectives](../../../../2_Lifecycle/2_Development/2_Model_Evaluation/PerformanceMetrics/QG_Objective_(MultiLabelClassification).md) focusing on the four values of the [confusion matrix](../../../../2_Lifecycle/2_Development/2_Model_Evaluation/PerformanceMetrics/AdditionalMaterial/QG_ConfusionMatrix_(ClassificationPerformanceMetrics).md).
- The [multi-label performance metrics compilation](../../../../2_Lifecycle/2_Development/2_Model_Evaluation/PerformanceMetrics/QG_PerformanceMetricsCompilation_(MultiLabelClassification).md) is selected based on standard metrics that align with the domain, and data distribution, aiming to provide a broad overview of the model's performance from different angles. This results in the first baseline iteration, against which to compare further iterations for metrics evaluation, and optimization.
    > The vanilla-approach minimizes *loss* during model training, and transforms raw model output based on a threshold of *0.5*. The *F1-Score* is identified as the primary metric that best summarizes the real-world tuning objectives. Metrics are calculated per-label, and based on four binary-based averaging methods for the multi-label case.
- In alignment with additional material, i.e. visualizing model confidence based on the [groundtruth probability distribution](../../../../2_Lifecycle/2_Development/2_Model_Evaluation/PerformanceMetrics/AdditionalMaterial/QG_GroundtruthProbabilityDistribution_(ClassificationPerformanceMetrics).md), as well as calculated per-label metrics, the desired averaging method, i.e. macro-averaging, and minimally acceptable label count are identified.
- Finally, three additional [threshold optimization methods](../../../../2_Lifecycle/2_Development/3_Model_Optimization/PostProcessing/QG_Thresholding_(ClassificationPerformanceMetrics).md) are consulted, two of which are ranking-metrics based, and one includes domain knowledge to address data imbalance and label correlations, based on a [benefit matrix](../../../../2_Lifecycle/2_Development/3_Model_Optimization/PostProcessing/QG_BenefitMatrix_(MultiLabelClassification).md)
    > The last stages are repeated until a satisfactory metrics compilation is established that proves reliable to function as foundation for further lifecycle design decisions.

###### Overview of related QGs and information sections including whether they are generalizable guidelines or use case-specific:

- System
    - Application
        - Domain Knowledge
            - Electrocardiogram (BasicKnowledge)  (specific)
        - ECG Alarming Guard Functionality (EmergencyMedicine)  (specific)
    - Stakeholder
        - Consulting
            - Domain Expert (generalizable)

- Data
    - Data Transformation
        - QG Multi-Label Structure (specific)

- Development 
    - Design Decision Making
        - Methods
            - QG SelectionMethod (generalizable)
        - Open-source Data
            - QG Physionet (specific)
    - Evaluation
        - QG Performance Metrics Compilation (generalizable)
        - QG Objective (generalizable)
        - QG Additional Material (generalizable)
            - QG Confusion Matrix Distribution (specific)
            - QG Groundtruth-Probability Distribution  (specific)
    - Optimization
        - QG Postprocessing (generalizable)
            - QG Benefit-Matrix (specific)
            - QG Thresholding (generalizable)

- Information for Maintenance and Deployment extracted based on Leaf-QG-Layers
<br>
