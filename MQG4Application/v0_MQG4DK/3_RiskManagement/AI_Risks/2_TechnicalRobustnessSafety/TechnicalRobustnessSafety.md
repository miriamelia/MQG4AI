---
tags: [{Name: TechnicalRobustnessSafety}, {Intent: Overview}, {Applicability: AIAct}, {Usage Example: default_highrisk}]
---

> Based on [ALTAI](https://digital-strategy.ec.europa.eu/en/library/ethics-guidelines-trustworthy-ai)

### Definition Technical Robustness and Safety
AI systems need to be resilient and secure. They need to be safe, ensuring a fall back plan in case something goes wrong, as well as being accurate, reliable and reproducible. That is the only way to ensure that also unintentional harm can be minimized and prevented.

#### Overview Requirements Technical Robustness and Safety: 

##### Resilience to Attack and Security 
See [Mitre Atlas](https://atlas.mitre.org/) to identify risks.

ALTAI:
> - Could the AI system have adversarial, critical or damaging effects (e.g. to human or societal safety) in case of risks or threats such as design or technical faults, defects, outages, attacks, misuse, inappropriate or malicious use?
> - Is the AI system certified for cybersecurity (e.g. the certification scheme created by the Cybersecurity Act in Europe) or is it compliant with specific security standards?
> - How exposed is the AI system to cyber-attacks?
>   - Did you assess potential forms of attacks to which the AI system could be vulnerable?
>   - Did you consider different types of vulnerabilities and potential entry points for attacks such as:
>       - Data poisoning (i.e. manipulation of training data);
>       - Model evasion (i.e. classifying the data according to the attacker's will);
>       - Model inversion (i.e. infer the model parameters)
> - Did you put measures in place to ensure the integrity, robustness and overall security of the AI system against potential attacks over its lifecycle?
> - Did you red-team/pentest the system?
> - Did you inform end-users of the duration of security coverage and updates?
>   - What length is the expected timeframe within which you provide security updates for the AI system?

##### General Safety

ALTAI:
> - Did you define risks, risk metrics and risk levels of the AI system in each specific use case?
>   - Did you put in place a process to continuously measure and assess risks?
>   - Did you inform end-users and subjects of existing or potential risks?
>> MQG4AI's design is intended to support this process through the risk management section and linking with the lifecycle
> -  Did you identify the possible threats to the AI system (design faults, technical faults, environmental threats) and the possible consequences?
>   - Did you assess the risk of possible malicious use, misuse or inappropriate use of the AI system?
>   - Did you define safety criticality levels (e.g. related to human integrity) of the possible consequences of faults or misuse of the AI system?
> - Did you assess the dependency of a critical AI system’s decisions on its stable and reliable behaviour?
>   - Did you align the reliability/testing requirements to the appropriate levels of stability and reliability?
> - Did you plan fault tolerance via, e.g. a duplicated system or another parallel system (AI-based or ‘conventional’)?
> - Did you develop a mechanism to evaluate when the AI system has been changed to merit a new review of its technical robustness and safety?

##### Accuracy
ALTAI:
> - Could a low level of accuracy of the AI system have critical, adversarial or damaging [consequences](./../../../1_System/Application/Ethics_Specific/Ethics_Specific.md)?
> - Did you put in place measures to ensure that the data (including training data) used to develop the AI system is up-to-date, of high quality, complete and representative of the environment the system will be deployed in?
> - Did you put in place a series of steps to monitor, and document the AI system’s accuracy?
>> MQG4AI's design is intended to support this process, e.g. through information extraction during development, in form of a post-market monitoring information layer of [leaf-Quality Gates](../../../../templates/Template_LeafQG.md) 
> - Did you consider whether the AI system's operation can invalidate the data or assumptions it was trained on, and how this might lead to adversarial effects?
> - Did you put processes in place to ensure that the level of accuracy of the AI system to be expected by end-users and/or subjects is properly communicated?

Additional Questions:
> - What is the [intended use](./../../../1_System/Application/Application.md#1-purpose) and [application domain](./../../../1_System/Application/Application.md#6-domain) of the system and how can this information be translated for performance evaluation metrics?
> - Which measurements and metrics are relevant for the AI system application and how are they defined in a reliable manner?
> - Are the [chosen performance evaluation metrics and thresholds](./../../../1_System/AI_System.md#ai-technique---lifecycle-implementation) a reliable orientation for further decision-making in alignment with the [intended use](./../../../1_System/Application/Application.md#1-purpose)?
> - Which information is relevant to [stakeholders](./../../../1_System/Stakeholder/Stakeholder.md) so that they correctly update, address, and interpret the applied performance metrics?
> - Did you declare the levels of accuracy and the relevant accuracy metrics in the accompanying [instructions of use](./../../../1_System/Documentation/Documentation.md#use)? 


##### Reliability, Fall back plans and Reproducibility
ALTAI:

> - Could the AI system cause critical, adversarial, or damaging consequences (e.g. pertaining to human safety) in case of low reliability and/or reproducibility?
>   - Did you put in place a well-defined process to monitor if the AI system is meeting the intended goals?
    >> MQG4AI's design is intended to support this process, e.g. through information extraction during development, in form of a post-market monitoring information layer of [leaf-Quality Gates](../../../../templates/Template_LeafQG.md) 
    >> Measuring intended goals is related with [Performance Evaluation Metrics](./../../../2_Lifecycle/2_Development/2_Model_Evaluation/PerformanceMetrics)
> - Did you test whether specific contexts or conditions need to be taken into account to ensure reproducibility?
> - Did you put in place verification and validation methods and documentation (e.g. logging) to evaluate and ensure different aspects of the AI system’s reliability and reproducibility?
     >> MQG4AI's design is intended to support this process, e.g. through lifecycle planning
>   - Did you clearly document and operationalise processes for the testing and verification of the reliability and reproducibility of the AI system?
> - Did you define tested failsafe fallback plans to address AI system errors of whatever origin and put governance procedures in place to trigger them?
> - Did you put in place a proper procedure for handling the cases where the AI system yields results with a low confidence score?
> - Is your AI system using (online) continual learning?
>   - Did you consider potential negative consequences from the AI system learning novel or unusual methods to score well on its objective function?