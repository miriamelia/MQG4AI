---
tags: [{Name: }, {Intent: }, {Problem: }, {Solution: }, {Applicability: }, {Consequences: }, {Usage Example: }]
---

## QG Data Pre-processing (RCA-IUnet-Barlow Twins) 

Based on [BT-Unet: A self-supervised learning framework for biomedical image segmentation using barlow twins with U-net models](https://link.springer.com/article/10.1007/s10994-022-06219-3) 

### 1. Interdependency Graph

#### Input Information
> What information is necessary to execute the method and generate the content?

- ##### Related QGs
    > Which stages are required? What pre-requisites exist so the content dimension can be applied?

    [Data Design Input]

- ##### AI System Information
    > Which AI system-specific information is relevant so the content dimension can be applied?

#### Output Information 
> What information is produced that is relevant to other stages and design decisions?

- ##### Related QGs
    > Which stages are impacted and which additional information might be necessary?

    [Model configuration]

- ##### Post-Market Monitoring Information (Maintenance Stage)
    > Is there relevant information for post-market monitoring?

<br>

### 2. Quality Gate Creation (Design-Decision-Specific Dimensions)

#### Dimension 1: Content
> Which information is generated?

1. Self-supervised learning:
    - A total of 187 unlabeled TBE images
    - Splitting: complete data
    - All images resized to 256x256
    - Normalization: divide pixel values by 255 to avoid exploding gradients
    - Two different images are generated from an input image using image augmentation techniques: 
        - Apply resizing and cropping with random size
        - that image is flipped with a 50% chance
        - that image is rotated with a 50% chance
        - that image is solarized with a 30% chance

2. Fine-tuning  
    - A total of 85 labeled esophagus' shapes
    - Splitting: 70% training and 30% test data
    - All images resized to 256x256
    - Normalization: divide pixel values by 255
    - 5-fold cross validation

#### Dimension 2: Method
> How is the information generated? 

Based on [BT-Unet: A self-supervised learning framework for biomedical image segmentation using barlow twins with U-net models](https://link.springer.com/article/10.1007/s10994-022-06219-3) 


#### Dimension 3: Representation
> How should which information should be presented to which stakeholders and when?

##### Developer

- Developers need to access pre-processed data during model training and implement pre-processing steps

<br>

#### Evaluation
> What are open questions when applying the generated information?

Possibly this configuration could be refined as part of model optimization, which includes pre-processing steps, as well as more labeled data.
For instance, divsion by 255 should be replaced with Z-Score normalization.

<br>

### 3. Additional Information

#### Risk Management

- ##### Poses Risk(s)
    > Are there related risks?

- ##### Implements Risk Control(s)
    > Are there risk controls implemented?

#### ...
