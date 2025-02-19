---
tags: [{Name: RawModelOutput_(nnUnet)}, {Intent: SmoothWorkflow}, {Problem: FormatMismatch}, {Solution: OutputTransformation}, {Applicability: Segmentation}, {Consequences: SmoothSoftwareWorkflow}, {Usage Example: PostModelSelection}]
---

## QG Raw Model Output (nn-Unet) 


### 1. Interdependency Graph

#### Input Information
> What information is necessary to execute the method and generate the content?

- ##### Related QGs
    > Which stages are required? What pre-requisites exist so the content dimension can be applied?

    [Model configuration nn-Unet](../../../2_Development/1_Model_Configuration/QG_nnU-Net_(StateOfTheArt).md)

- ##### AI System Information
    > Which AI system-specific information is relevant so the content dimension can be applied?

    [Application *EsophagusVisualization*](../../../../1_System/Application/TBE_Segmentation.md)

#### Output Information 
> What information is produced that is relevant to other stages and design decisions?

- ##### Related QGs
    > Which stages are impacted and which additional information might be necessary?

- ##### Post-Market Monitoring Information (Maintenance Stage)
    > Is there relevant information for post-market monitoring?

    Data transformation needs to be integrated in software  [Application *EsophagusVisualization*](../../../../1_System/Application/TBE_Segmentation.md)

<br>

### 2. Quality Gate Creation (Design-Decision-Specific Dimensions)

#### Dimension 1: Content
> Which information is generated?

- Binary Mask, as predicted by the model is prepared to be incorporated within the medical software
- The software is designed to process outlines in the form of polygons, therefore, the binary mask is converted using an OpenCV library function
- And, the image is resized to its original form, which is saved before model input


#### Dimension 2: Method
> How is the information generated? 

- Embedded within the medical software *EsophagusVisualization*

#### Dimension 3: Representation
> How should which information should be presented to which stakeholders and when?

##### Developer

Documentation of workflow

<br>

#### Evaluation
> What are open questions when applying the generated information?


<br>

### 3. Additional Information

#### Risk Management

- ##### Poses Risk(s)
    > Are there related risks?

- ##### Implements Risk Control(s)
    > Are there risk controls implemented?

#### ...
