---
tags: [{Name: DataPreprocessing_(nnUnet)}, {Intent: ModelInputPreparation}, {Problem: OptimalModelPerformance}, {Solution: Optimization}, {Applicability: Segmentation}, {Consequences: EnhanceModelPerformance}, {Usage Example: PostModelSelection}]
---

## QG Data Preprocessing (nn-Unet) 

Introduced in [nnU-Net: a self-configuring method for deep learning-based biomedical image segmentation](https://www.nature.com/articles/s41592-020-01008-z)
- [Related repo](https://github.com/MIC-DKFZ/nnUNet)

### 1. Interdependency Graph

#### Input Information
> What information is necessary to execute the method and generate the content?

- ##### Related QGs
    > Which stages are required? What pre-requisites exist so the content dimension can be applied?

    [Data design input](../../1_Acquisition/QG_DataDesignInput_(TBESegmentation).md)
    [Further Data Acquisition information on Data collection](../../1_Acquisition/QG_Acquisition_(Data).md)
    [Data Utilization regarding data quality](../../2_Utilization/QG_Utilization_(Data).md)
    [Model configuration](../../../2_Development/1_Model_Configuration/QG_nnU-Net_(StateOfTheArt).md)

- ##### AI System Information
    > Which AI system-specific information is relevant so the content dimension can be applied?

    [Developer](../../../../1_System/Stakeholder/1_Active/Developer_(ActiveStakeholder).md)

#### Output Information 
> What information is produced that is relevant to other stages and design decisions?

- ##### Related QGs
    > Which stages are impacted and which additional information might be necessary?

    [Model configuration nn-Unet](../../../2_Development/1_Model_Configuration/QG_nnU-Net_(StateOfTheArt).md)
    [Optimization](../../../2_Development/3_Model_Optimization/QG_ModelOptimization_(Development).md)

- ##### Post-Market Monitoring Information (Maintenance Stage)
    > Is there relevant information for post-market monitoring?

    - triggered for new data the model encounters, and if the model is retrained

<br>

### 2. Quality Gate Creation (Design-Decision-Specific Dimensions)

#### Dimension 1: Content
> Which information is generated?

- A total of 85 labeled esophagus' shapes
- Splitting: 70% training and 30% test data
- automatic 5-fold cross validation

- [Supplementary notes on nn-Unet design principles](https://static-content.springer.com/esm/art%3A10.1038%2Fs41592-020-01008-z/MediaObjects/41592_2020_1008_MOESM1_ESM.pdf)

Automatic execution based on input data (based on plans.json):
- Z Score Normalization is applied
- Spacing (1.0, 1.0)
- Patch-size (768, 363)

Augmentation techniques:
Rotations, scaling, Gaussian noise, Gaussian blur, brightness, contrast, simulation of low resolution, gamma correction and mirroring.

#### Dimension 2: Method
> How is the information generated? 

Introduced in [nnU-Net: a self-configuring method for deep learning-based biomedical image segmentation](https://www.nature.com/articles/s41592-020-01008-z)
- [Related repo](https://github.com/MIC-DKFZ/nnUNet) 


#### Dimension 3: Representation
> How should which information should be presented to which stakeholders and when?

##### Developer

Developers need access to information during model training

<br>

#### Evaluation
> What are open questions when applying the generated information?

Possibly this configuration could be refined as part of model optimization, which includes pre-processing steps, as well as more labeled data.

<br>

### 3. Additional Information

#### Risk Management

- ##### Poses Risk(s)
    > Are there related risks?

- ##### Implements Risk Control(s)
    > Are there risk controls implemented?

#### ...
