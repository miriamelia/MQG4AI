---
tags: [{Name: RiskAnalysis}, {Intent: Overview},  {Applicability: AIAct}, {Usage Example: default_highrisk}]
---

#### Risk Analysis (RiskManagement)

The AI Act defines [risk](https://artificialintelligenceact.eu/article/3/) as: 
"(2) ‘risk’ means the combination of the probability of an occurrence of harm and the severity of that harm;"
Risks need to be identified in accordance with the individual [application](./../../../1_System/Application/Application.md) and [stakeholder](./../../../1_System/Stakeholder/Stakeholder.md), and [documented](./../../../1_System/Documentation/Documentation.md#risk-management-appended-based-on-the-overview-introduced-above).
In addition to [AI risks based on AI trustworthiness criteria](./../../AI_Risks), conducting risk analysis in alignment with the following terminology can support a comprehensive coverage of possible use case-specific risks.

Risk analysis includes the identification and estimation of risks.

##### AI System (AIRO)

- has risk (risk associated with the ai system)
![](../../../../../imgs/Risk%20Management%20(AIRO)/Risk.png){width=800 height=}

<br>

#### Misuse

![](../../../../../imgs/Risk%20Management%20(AIRO)/Misuse.png){width=800 height=}

Identify other possible application scenarios compared to the [intended purpose](./../../../1_System/Application/Application.md#--purpose)

<br>

#### Area Of Impact

![](../../../../../imgs/Risk%20Management%20(AIRO)/areaOfImpact_risk.png){width=800 height=}


For risks analysis, the [area of impact](./../../../1_System/Application/Application.md#--area-of-impact) is analyzed with a different focus.

<br>

#### Risk Source

![](../../../../../imgs/Risk%20Management%20(AIRO)/Risk%20Source.png){width=800 height=}

- risk source.is risk source for (risk)

Based on the [application](./../../../1_System/Application/Application.md), area of impact, misuse, and [implementation](./../../../2_Lifecycle/AI_Lifecycle.md) identify possible risk sources, which can be classified as follows:


<br>

##### - Hazard

![](../../../../../imgs/Risk%20Management%20(AIRO)/Hazard.png){width=800 height=}

→ identify sources of harm that arise from unintentional sources and exists because of exisitng conditions, the environment or system flaws, such as a biased data set

<br>

##### - Threat

![](../../../../../imgs/Risk%20Management%20(AIRO)/Threat.png){width=800 height=}

→ identify sources of harm that arise from intentional sources and stem form an active agent, such as a cyber attack

<br>

##### - Vulnearability

![](../../../../../imgs/Risk%20Management%20(AIRO)/Vulnearability.png){width=800 height=}

→ identify weaknesses or gaps in the system that can become a source for risk

<br>

#### Event

![](../../../../../imgs/Risk%20Management%20(AIRO)/Event.png){width=800 height=}

→ identify events that are triggered by risk sources and lead to potential harm, one source can result in multiple events.


<br>

Next, identify the likelihood and severity of identified risk sources and events in accordance with the individual [application](./../../../1_System/Application/Application.md) and [stakeholder](./../../../1_System/Stakeholder/Stakeholder.md).


#### Likelihood
![](../../../../../imgs/Risk%20Management%20(AIRO)/likelihood.png){width=800 height=}

→ identify the chances of an event happening

<br>

#### Severity

![](../../../../../imgs/Risk%20Management%20(AIRO)/Severity.png){width=800 height=}

consequence / impact.has severity (severity)

→ identify the severity of impact of an event happening based on consequences and impact

<br>

##### - Consequence

![](../../../../../imgs/Risk%20Management%20(AIRO)/Consequence.png){width=800 height=}

<br>

risk.has consequence (foreseeable unintended outcomes / consequences)


##### - Impact

![](../../../../../imgs/Risk%20Management%20(AIRO)/Impact.png){width=800 height=}

→ Outcome of risks that are estimated based on the previously identified sources



##### Relations

consequence.has impact

- consequence.has impact (discriminatory impact of system)
- consequence.has impact (harmful impacts of the risk)
- has impact on area
  - impact.has impact on area (Area of impact)
- has impact on AI subject
  - impact.has impact on AI subject (AI subject)