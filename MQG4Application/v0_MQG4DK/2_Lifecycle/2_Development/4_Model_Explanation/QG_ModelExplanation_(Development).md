---
tags: [{Name: QG_ModelExplanation_(Development)}, {Intent: Overview}, {Applicability: GenericAILifecycle}, {Usage Example: default_highrisk}]
---




# QG Model Explanation (Development)

This section addresses information how to achieve model explainability. 
Overall, the proposed structure is alignable with the concepts introduced in the [IEEE Guide for an Architectural Framework for Explainable Artificial Intelligence](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=10659410).

Horizontal interdependencies that are relvant for explanation method optimization are related to the [Model Configuration](./../1_Model_Configuration/QG_ModelConfiguration_(Development).md), and [Data quality, pre-processing steps and raw/transformed model output](./../../1_Data/2_Utilization/QG_Utilization_(Data).md). 

Among others, they shape Input- and Output Information of the Interdependency Graph in the [Leaf-QG template](../../../../templates/Template_LeafQG.md) for design decisions.

Optimization is conceptually monitored by MQG4A-template versions that illustrate different combinations of implementation approaches and how they relate with results.

### Overview Sub-QGs

![](../../../../../imgs/Lifecycle/QGExplanation.png)

> This is only a proposition based on our contribution of this MQG4AI-template. Identified leaf-QGs are marked grey. The appneded proposed leaf-QG contribution for explanation evaluation is colorized in blue, including the related configuration setting.
