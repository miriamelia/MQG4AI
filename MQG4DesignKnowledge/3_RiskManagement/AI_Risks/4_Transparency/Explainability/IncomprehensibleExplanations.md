---
tags: [{Name: IncomprehensibleExplanations}, {Intent: Transparency_Risk}, {Applicability: Explainability}, {Usage Example: bestPractices_TechnicalGuidelines}]
---

## Incomprehensible Explanations to User (Transparency_Explainability - Risk)
>> **Use case**: t.b.d.
>> **Result**: Derived QGs and proposed structure for the Development [Stage - Model Explanation Interpretation for User](../../../../2_Lifecycle/2_Development/4_Model_Explanation/UserInteraction/) and [Usability Evaluation](../../../../2_Lifecycle/2_Development/4_Model_Explanation/Method_Evaluation/Usability/t.b.d.md)
>> **Related Risks**: 

### Risk Assessment (Risk Analysis + Risk Evaluation) 

#### Risk: Incomprehensible to User
Deep neural networks are opaque by nature.
Consequently, methods for explanation need to be applied and evaluated. 
These methods need to be explained to the user to ensure a trustworthy application, aiming to provide the desired *Usability*.

The hazard of incomprehensible explanations to the user:
This risk arises when the methods of explanation and their presentation are not adapted to the user's capacity of comprehension confusion and misunderstanding. Explanations that are too vague, overly complex or are not well framed may prevent the user from understanding the model's reasoning on how to apply the results in a particular context, which may reduce trust in the system.

#### Risk analysis

##### Severity of harm
Depends on the application of the explainability technique

##### Probability of Occurence
Depends on the application of the explainability technique

#### Risk evaluation
Depends on the application of the explainability technique

#### Risk control
The following recommendations for risk mitigation are outlined:

- Design a user interaction flow to ensure the correct understanding of the system's functioning, including the assertion of knowledge about the system's contextual operation and limitations. It should include a notification protocol when there are relevant updates that may imply changes in the AI system's operation.
    - ##### Lifecycle
    [User Interaction Flow](../../../../2_Lifecycle/2_Development/4_Model_Explanation/UserInteraction/Interaction_Flow/QG_InteractionFlow_(UserExplainabilityInterpretation).md)
- Develop informative interfaces, at different levels of complexity, about the explanations to facilitate user interpretation.
    - ##### Lifecycle
    [User Information Interface](../../../../2_Lifecycle/2_Development/4_Model_Explanation/UserInteraction/Information_Interface/QG_InformationInterface_(UserExplainabilityInterpretation).md)
- Evaluate the *Usability* of explanations
    - ##### Lifecycle
    [Usability Evaluation](../../../../2_Lifecycle/2_Development/4_Model_Explanation/Method_Evaluation/Usability/t.b.d.md)



