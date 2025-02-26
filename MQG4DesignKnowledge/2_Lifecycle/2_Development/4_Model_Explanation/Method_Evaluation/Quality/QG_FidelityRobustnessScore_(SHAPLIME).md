---
tags: [{Name: QG_FidelityRobustnessScore}, {Intent: ExplanationMethod_ApplicabilityEvaluation}, {Problem: UnfaithfulExplanations}, {Solution: ExplanationEvaluationMetrics}, {Applicability: SHAPLIME_Explanations}, {Consequences: FidelityRobustnessScore}, {Usage Example: none}]
---

## QG FidelityRobustnessScore (SHAP LIME) 

> Based on paper [On the transferability of local model‐agnostic explanations of machine learning models to unseen data](https://www.researchgate.net/publication/381757544_On_the_transferability_of_local_model-agnostic_explanations_of_machine_learning_models_to_unseen_data)


### 1. Interdependency Graph

#### Input Information
> What information is necessary to execute the method and generate the content?

- LIME/SHAP must be used to explain the machine learning (ML) task (Is LIME/SHAP applied?) 
- The ML model should allow the generation of LIME/SHAP explanations  
- If the underlying model does not perform well, probably the quality of generated explanations is impacted
- If the used data is of low quality, the model performance and explanations quality can be impacted
- A reasonable number of generated explanations to evaluate
In statistics, the greater a population is, the less it is affected by atypical data (and the more representative it is of the population): so the greater the amount of explanations, the better to calculate the score.


- ##### Related QGs
    > Which stages are required? What pre-requisites exist so the content dimension can be applied?

    - [Data](../../../../1_Data/QG_Data_(Lifecycle).md)
        - [Data quality and preprocessing](../../../../1_Data/2_Utilization/QG_Utilization_(Data).md)
    - [Model configuration](../../../1_Model_Configuration/)
        - [Model](../../../1_Model_Configuration/QG_ModelConfiguration_(Development).md)
    - [Model evaluation](../../../2_Model_Evaluation/QG_ModelEvaluation_(Development).md)
        - [Performance Metrics](../../../2_Model_Evaluation/PerformanceMetrics/)
    - [Model explanation configuration](../..)
        - [Explainability method configuration and generated explanations](../../Method_Configuration/QG_MethodConfiguration_(ExplanationDevelopment).md)

       
- ##### AI System Information
    > Which AI system-specific information is relevant so the content dimension can be applied?

    - none

#### Output Information 
> What information is produced that is relevant to other stages and design decisions?

A use case- and model-agnostic approach to evaluate LIME/SHAP explanations, answering the question: Are LIME/SHAP explanations appropriate for explaining the ML task? (on a scale from 0 to 1)

> **Interpretation of the Robustness-Fidelity Score**
> - A score of 0 indicates that LIME/SHAP explanations are not appropriate for the task, and should not be trusted.
> - A score of 1 indicates that LIME/SHAP explanations are perfect for the task.
> - Any score in between can suggest that explanations are either appropriate or not. 
> > Rule of thumb everything above 0.8 is good, and above 0.9 is pretty good, if the score is lower, it is advisable to regenerate the explanations for the ML task, possibly altering the model, data, or feature importance method used.

- ##### Related QGs
    > Which stages are impacted and which additional information might be necessary?

    - [Model explanation](../..)
        - [Explainability method configuration and generated explanations](../../Method_Configuration/QG_MethodConfiguration_(ExplanationDevelopment).md)
    - [Deployment](../../../../3_Deployment/QG_Deployment_(Lifecycle).md)
    - [Maintenance](../../../../4_Maintenance/QG_Maintenance_(Lifecycle).md)

- ##### Post-Market Monitoring Information (Maintenance Stage)
    > Is there relevant information for post-market monitoring?

    - The metric is measured during the development of the model and provides useful insights for active stakeholders to improve it. 
    - If the score obtained is acceptable, the metric does not need to be monitored over time, as an acceptable score means that explanations are robust to future examples (over time). It is not necessary to continuously monitor the score to assess generated explanations during model deployment, as the score has been calculated with the expectation that the data may vary slightly in this scenario. 
    - However, it would be sensible to remeasure the score if the model is retrained on entirely new data, as significant changes in the data distribution could affect the reliability of the explanations.

<br>

### 2. Quality Gate Creation (Design-Decision-Specific Dimensions)

#### Dimension 1: Content
> Which information is generated?

To assess if LIME/SHAP explanations are appropriate for a ML task, their fidelity to the underlying ML task and their robustness to changes in distribution are measured. 
- Fidelity measures that explanations accurately reflect the underlying decision-making process, capturing the model’s internal logic behind its prediction. 
- Robustness, on the other hand, assesses whether explanations for similar inputs are also similar, ensuring that small variations in the input distribution do not lead to drastically different explanations. 
- Both metrics are essential to ensure that explanations are appropriate: focusing solely on fidelity could result in explanations that are faithful but unstable across examples, while solely on robustness may yield consistent explanations that are not representative of the ML task.

A score for each metric is calculated, and combined to obtain a final score. 

1. **Fidelity** is measured by a set of sanity checks (model randomization and data randomization checks). Explanations can either pass or fail the checks, so fidelity can be either 0 or 1.

> Assumption: The method to test explanation fidelity assumes that every time we split a dataset into train and test samples, the samples that fall into either subset are different (from the samples that fall into the same subset every other time). Mathematically, the chances of that happening are 1 in every n (n is the number of total samples), if there are no repeated samples. In every other case, it would be greater.

2. **Robustness** is measured by calculating the similarity of explanations that are generated from data of slightly different distribution. Robustness has a value between 0 and 1.

> Assumption: If explanations are robust to different test sets, they are also robust to distribution changes in the test set (as the only way the distribution of the test set can change is if the test set changes).  Further, explanations have passed the fidelity checks, and the mean of the generated explanations is representative of the explanations

3. The final score is calculated by multiplying the fidelity and robustness score.


#### Dimension 2: Method
> How is the information generated?

As part of the pre-configuration stage of the design decision which model explanations to apply, if SHAP and LIME explanations are considered, when applying this [design decision-making method](../../../0_DesignDecisionMaking/Methods/QG_SelectionMethod_(DesignDecisionMaking).md).

- **Robustness evaluation: to changes in data distribution**
The used method calculates the similarity between explanations generated from models trained and tested on slightly different data splits, where each split introduces small variations in the data distribution. 
> The resulting NDCG score to quantify the similarity between these explanations, is the score obtained for this test.

- **Fidelity evaluation: Sanity Checks**
Sanity checks are randomization tests that assess whether the explanations are genuinely informative about the model and data, and therefore faithful to the ML task. 

> - The data randomization test compares explanations generated from a model trained on original data (base scenario) against those generated from a model trained on data with randomized class labels. 
> - The model parameter randomization test compares explanations generated under the base scenario against those generated from a randomly initialized model. 
> - Feature importance explanations can be considered similar if their feature importance rank is similar. However, since less important features contribute less to the model’s overall behavior it is especially important to ensure that the feature importance rank is similar for the most important features. Therefore, we use the **Normalized Discounted Cumulative Gain (NDCG) metric** to quantify the similarity between explanations, as it prioritizes the correct ranking of higher-importance features.
> > In both tests, if the NDCG score from explanations generated under the base scenario is significantly different (statistically) from that under both altered scenarios, both tests are passed (with a score of 1) and explanations can be considered faithful. In any other scenario, a score of 0 is obtained.

- **FidelityRobustnessScore: merge information through multiplication**
introduce scenarios - this final metric will be 0 if fidelity is 0, otherwise if model fidelity exists, the score mirrors the explanation's robustness evaluation to changes in the data distribution

#### Dimension 3: Representation
> Which information should be presented to which stakeholders and when?

- AI Experts (active): to reconsider AI model or architecture used, XAI technique
- Data scientists (active): to reconsider data sources, quality, processing
- Domain experts (consulting): to validate explanations subjectively (if their knowledge disagrees with the explanations, then AI Experts and Data scientists should reconsider)
- AI Users (passive): reliability of explanations received, if any
- AI provider (passive): desirability of model
- Regulators (passive)

<br>

#### Evaluation
> What are open questions when applying the generated content?

- *Why were the score metrics chosen?* Fidelity and robustness metrics were selected based on their frequent reference in the literature and their applicability across various types of explanations. 
- *How well tested is the design decision-making method?* The score is tested on SVM, MLP, and XGBoost models across two different datasets. 
- *What is the core assumption?* The method's key premise is that the model-agnostic SHAP and LIME methods generate feature importance explanations, which emphasize the significance of each feature in model predictions. As a result, the calculated score focuses on the similarity of feature importance ranks, as less important features are assumed to be less informative about the model. The similarity of explanations (measured by the NDCG score) is defined in terms of both the similarity of feature ranks (order of features by importance) and the actual feature importance values.
- *How significant is the impact of the domain?* The focus on feature importance ensures that the method remains independent of specific domains or use cases, enabling broad applicability. 

<br>


### 3. Additional Information

#### Risk Management

- ##### Poses Risk(s)
    > Are there related risks?

- ##### Implements Risk Control(s)
    > Are there risk controls implemented?

    Provides a method to assess Robustness and Fidelty of Model Explanations including a quantifiable score to address [Unfaithful Explanation](../../../../../3_RiskManagement/AI_Risks/4_Transparency/Explainability/UnfaithfulExplanations.md)




