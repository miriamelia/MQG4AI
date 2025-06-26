---
tags: [{Name: HumanAgencyOversight}, {Intent: Overview}, {Applicability: AIAct}, {Usage Example: default_highrisk}]
---

> Based on [ALTAI](https://digital-strategy.ec.europa.eu/en/library/ethics-guidelines-trustworthy-ai)

### Definition Human Agency and Oversight
AI systems should empower human beings, allowing them to make informed decisions and fostering their fundamental rights. At the same time, proper oversight mechanisms need to be ensured, which can be achieved through human-in-the-loop, human-on-the-loop, and human-in-command approaches.

#### Overview Requirements Human Agency and Oversight


##### Human Agency and Autonomy
ALTAI:
> - Is the AI system designed to interact, guide or take decisions by human end-users that affect humans or society?

Yes, it proposes a segmentation of the esophagus's shape in the TBE image

>   - Could the AI system generate confusion for some or all end-users or subjects on whether a decision, content, advice or outcome is the result of an algorithmic decision?

No, the segmented shape is obviously recognizable

>   - Are end-users or other subjects adequately made aware that a decision, content, advice or outcome is the result of an algorithmic decision?

Yes, the physician interacting with the software is aware of the AI and can manually select/deselect intelligent segmentation

> - Could the AI system generate confusion for some or all end-users or subjects on whether they are interacting with a human or AI system?

No, the segmented shape is obviously recognizable

>   - Are end-users or subjects informed that they are interacting with an AI system?

Yes, the physician interacting with the software is aware of the AI and can manually select/deselect intelligent segmentation

> - Could the AI system affect human autonomy by generating over-reliance by end-users?

Possibly, needs to be tested, but probability this might happen is estimated very low

>   - Did you put in place procedures to avoid that end-users over-rely on the AI system?

No, the probability that the physician accepts wronly selected shapes is estimated very low

> - Could the AI system affect human autonomy by interfering with the end-user’s decision-making process in any other unintended and undesirable way?

No, the only decision impacted is whether the segmented shape of the esophagus is accepted as foundation for the 3D-reconstruction

>   - Did you put in place any procedure to avoid that the AI system inadvertently affects human autonomy?

No, this is not deemed necessary for this particular AI application

> - Does the AI system simulate social interaction with or between end-users or subjects?

No

> - Does the AI system risk creating human attachment, stimulating addictive behaviour, or manipulating user behaviour? Depending on which risks are possible or likely, please answer the questions below:

No, this is not deemed necessary for this particular AI application

>   - Did you take measures to deal with possible negative consequences for end-users or subjects in case they develop a disproportionate attachment to the AI System?

No, this is not deemed necessary for this particular AI application

>   - Did you take measures to minimise the risk of addiction?

No, this is not deemed necessary for this particular AI application

>   - Did you take measures to mitigate the risk of manipulation?

No, this is not deemed necessary for this particular AI application

##### Human Oversight
ALTAI:
> - Please determine whether the AI system (choose as many as appropriate):
>   - Is a self-learning or autonomous system;

No

>   - Is overseen by a Human-in-the-Loop; 
    (capability for human intervention in every decision cycle of the system)

Yes, the [physician using the application](../../1_System/Stakeholder/3_Passive/Physician_(PassiveStakeholder).md)

>   - Is overseen by a Human-on-the-Loop; 
    (capability for human intervention during the design cycle of the system and monitoring the system’s operation)

Yes

>   - Is overseen by a Human-in-Command. 
    (capability to oversee the overall activity of the AI system (including its broader economic, societal, legal and ethical impact) and the ability to decide when and how to use the AI system in any particular situation)

Yes, the [physician using the application](../../1_System/Stakeholder/3_Passive/Physician_(PassiveStakeholder).md) may decide whether to apply the segmentation model

> - Have the humans (human-in-the-loop, human-on-the-loop, human-in-command) been given specific training on how to exercise oversight?

Yes, they were made aware, see [automation bias](./HumanOversight/AutomationBias_(TBE_Segmentation).md)

> - Did you establish any detection and response mechanisms for undesirable adverse effects of the AI system for the end-user or subject?

No, this is not deemed necessary for this particular AI application

> - Did you ensure a ‘stop button’ or procedure to safely abort an operation when needed?

Yes, the physician in charge may select whether to use the segmentation model

> - Did you take any specific oversight and control measures to reflect the self-learning or autonomous nature of the AI system?

No, the system does not continue to learn autonomously