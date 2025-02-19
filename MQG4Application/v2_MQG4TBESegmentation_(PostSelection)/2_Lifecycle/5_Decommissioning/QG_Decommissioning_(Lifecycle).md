---
tags: [{Name: QG_Decommissioning_(Lifecycle)}, {Intent: Overview}, {Applicability: GenericAILifecycle}, {Usage Example: default_highrisk}]
---


# QG Decommissioning (Lifecycle)

Curerently, we are at the beginning of integrating AI with the real world, and the *Decommissioning* stage is not focus of our current contribution. It needs to be refined with further empirical experience, including dependencies with other lifecycle processes. Overall, this section describes all necessary process steps to retrieve the intelligent system from its intended environment. This includes reversing the previously established technical and human-level workflow. 

### Overview Sub-QGs
Exemplary overview of process steps, based on ISO/IEC FDIS 5338:2023(E) on *Information Technology -- Artifical Intelligence -- AI system lifecycle processes*, and ISO/IEC 22989:2022 on *Information technology — Artificial intelligence — Artificial intelligence concepts and terminology*

- The disposal process \cite[33]{ISO5338AIlifecycle} aims "[...] to end the existence of a system element or system for a specified intended use, appropriately handle replaced or retired elements, and to properly attend to identified critical disposal needs [...]" (ISO 5338, 33)
    - The disposal of data is highlighted, as it comprises a "[...] new kind of disposal activity [...]" (ISO 5338, 33) 
    Especially, the role of "[...] security or privacy risks [...]" (ISO 5338, 33) is critical when terminating data application.#

- ISO 22989 has a slightly different perspective, focusing when disposal processes are necessary, which is summarized as *retirement* (ISO 22989, 40) 
    - In addition to decommissioning and discarding of the AI system (including the data) when the intended purpose no longer prevails (ISO 22989, 40), 
    - they differentiate replacement with a more suitable approach of the AI system, or components (ISO 22989, 40). 
- This view emphasizes the relation to maintenance and model updates. While we include a different approach with model updates during maintenance within MQG4AI, more leaning towards ISO 5338. 
- Therefore, maintenance, when executing model updates, may trigger decommissioning processes, while ISO 22989 assigns the creation of a new algorithm, when "[...] repairs and updates are not good enough to meet new requirements [...]" (ISO 22989, 40) within the retirement stage (ISO 22989, 40).