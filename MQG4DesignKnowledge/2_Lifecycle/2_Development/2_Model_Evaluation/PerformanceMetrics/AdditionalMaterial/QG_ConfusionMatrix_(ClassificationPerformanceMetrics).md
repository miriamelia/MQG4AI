---
tags: [{Name: QG_ConfusionMatrix}, {Intent: AdditionalMaterial}, {Problem: DataImbalance_UnreliablePerformanceEvaluation}, {Solution: ErrorQuantification}, {Applicability: ClassificationPerformanceMetrics_Thresholding}, {Consequences: PerformanceVisualization}, {Usage Example: none}]
---

## QG Confusion Matrix (Classification Performance Metrics) 

### 1. Interdependency Graph

#### Input Information
> What information is necessary to execute the method and generate the content?

Additional material is intended to shed light on the performance evaluation strategy of classification models. The confusion matrix helps to quantify the types of errors the model makes through contrasting the classifier's predictions (transformed raw model output based on a threshold) on the test set with the respective groundtruth.

- ##### Related QGs
    > Which stages are required? What pre-requisites exist so the content dimension can be applied?

    - [Data](../../../../1_Data/QG_Data_(Lifecycle).md)
        - [Groundtruth](../../../../1_Data/2_Utilization/QG_Utilization_(Data).md)
    - [Model Output](../../../2_Model_Evaluation/QG_ModelEvaluation_(Development).md)
        - [Model predictions](../../../../1_Data/QG_Data_(Lifecycle).md)
    - [Model optimization](../../../3_Model_Optimization/QG_ModelOptimization_(Development).md)
        - [Thresholding](../../../3_Model_Optimization/PostProcessing/QG_Thresholding_(ClassificationPerformanceMetrics).md)

- ##### AI System-specific Information
    > Which AI system-specific information is relevant so the content dimension can be applied?


#### Output Information 
> What information is produced that is relevant to other stages and design decisions?

The confusion matrix classifies model predictions into four values that are the foundation for classification performance evaluation.

- ##### Related QGs
    > Which stages are impacted and which additional information might be necessary?

    - [Model evaluation](../../../2_Model_Evaluation/QG_ModelEvaluation_(Development).md)
        - [Classification performance metrics](../QG_PerformanceMetricsCompilation_(Classification).md)
    - [Model optimization](../../../3_Model_Optimization/QG_ModelOptimization_(Development).md)
        - [Thresholding](../../../3_Model_Optimization/PostProcessing/QG_Thresholding_(ClassificationPerformanceMetrics).md)
    - [Maintenance](../../../../4_Maintenance/QG_Maintenance_(Lifecycle).md)

- ##### Post-Market Monitoring Information (Maintenance Stage)
    > Is there relevant information for post-market monitoring?

    - Monitor ongoing performance

<br>

### 2. Quality Gate Creation (Design-Decision-Specific Dimensions)

#### Dimension 1: Content
> Which information is generated?

To fill the confusion matrix, the raw model output is transformed based on a pre-defined threshold. The default value is *0.5*, and in case of imbalances data, this value should be optimized.

- In binary classification the *Positive* and *Negative* class are defined in accordance with the respective use case.
- In multi-label classification, the *Positive* describes the presence of a label, and *Negative* the absence of a label

 The four values of the confusion matrix:
 - True Positive (TP): model prediction and groundtruth are both *Positive*
 - False Positive (FP): groundtruth is *Negative*, while the model predicted a *Positive*
 - True Negative (TN): model prediction and groundtruth are both *Negative*
 - False Negative (FN): groundtruth is *Positive*, while the model predicted a *Negative*


#### Dimension 2: Method
> How is the information generated?

The confusion matrix is embedded with the performance metrics compilation and evaluation strategy, and contributes to additional material.

#### Dimension 3: Representation
> Which information should be presented to which stakeholders and when?

The confusion matrix supports stakeholders to interpret classification performance evaluation metrics that are based on a threshold.

##### - Stakeholder Developer
- continuous model evaluation

##### - Stakeholder Quality Manager
- conformity assessment

<br>

#### Evaluation
> What are open questions when applying the generated content?

<br>


### 3. Additional Information

#### Risk Management

- ##### Poses Risk(s)
    > Are there related risks?

- ##### Implements Risk Control(s)
    > Are there risk controls implemented?

    - Contribution to addressing [unreliable performance evaluation metrics](../../../../../3_RiskManagement/AI_Risks/2_TechnicalRobustnessSafety/Accuracy/UnreliablePerformanceMetrics.md) the model's performance and errors in relation to a pre-defined threshold

#### ...
