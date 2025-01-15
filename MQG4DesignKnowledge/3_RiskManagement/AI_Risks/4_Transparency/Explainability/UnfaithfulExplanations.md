---
tags: [{Name: UnfaithfulExplanations}, {Intent: Transparency_Risk}, {Applicability: Explainability}, {Usage Example: bestPractices_TechnicalGuidelines}]
---

## Unfaithful Explanations (Transparency_Explainability - Risk)
> Derive Lifecycle-QGs based on best practices to address the risk of unfaithful explanations for Leaf-QG creation
>> **Use case**: t.b.d.
>> **Result**: Contribution to the Development [Stage - Model Explanation quality evaluation based on unsupervised metrics](../../../../2_Lifecycle/2_Development/4_Model_Explanation/Method_Evaluation/Quality/), including a technical guideline to assess the fidelity and robustness of explanations based on the [Quality Gate format](../../../../../templates/Template_LeafQG.md) which includes information extraction for other related system requirements, lifecycle stages and design decisions.

### Risk Assessment (Risk Analysis + Risk Evaluation) 

#### Risk: Unfaithful Explanations
Deep neural networks are opaque by nature.
Consequently, methods for explanation need to be applied and evaluated. These methods need to be tested for applicability.

The hazard of unfaithful explanations:
This risk arises when explanation methods fail to accurately reflect a model’s true reasoning, leading to misunderstandings of its decisions. Such explanations can misguide stakeholders, resulting in harmful actions throughout its lifecycle and eroding trust in the system based on hazardous information through unfaithful explanations.

#### Risk evaluation

##### Severity of harm
Depends on the application of the explainability technique

##### Probability of Occurence
Depends on the application of the explainability technique

#### Risk control
The following recommendations for risk mitigation are outlined:

-  Validate the explanations by proving they are not coincidental and by providing confidence metrics (e.g., cross-validation of models) for the generated model.
    - ##### Lifecycle
    Implement methods to evaluate the chosen explainability method.
    Example: [Fidelity-Robustness Score for LIME SHAP Explanations](../../../../2_Lifecycle/2_Development/4_Model_Explanation/Method_Evaluation/Quality/QG_FidelityRobustnessScore_(SHAPLIME).md)


