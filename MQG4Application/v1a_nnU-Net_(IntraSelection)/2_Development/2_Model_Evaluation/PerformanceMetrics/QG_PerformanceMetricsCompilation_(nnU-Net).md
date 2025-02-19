---
tags: [{Name: }, {Intent: }, {Problem: }, {Solution: }, {Applicability: }, {Consequences: }, {Usage Example: }]
---

## QG Performance Metrics Selection (TBE Segmentation) 

- Based on [Towards a guideline for evaluation metrics in medical image segmentation](https://bmcresnotes.biomedcentral.com/articles/10.1186/s13104-022-06096-y)

### 1. Interdependency Graph

#### Input Information
> What information is necessary to execute the method and generate the content?

- ##### Related QGs
    > Which stages are required? What pre-requisites exist so the content dimension can be applied?

    [Data Preprocessing]
    [Model Configuration]

- ##### AI System Information
    > Which AI system-specific information is relevant so the content dimension can be applied?

    [Developer]

#### Output Information 
> What information is produced that is relevant to other stages and design decisions?

- ##### Related QGs
    > Which stages are impacted and which additional information might be necessary?

    [Model Configuration]
    [Optimization] if this configuration is selected

- ##### Post-Market Monitoring Information (Maintenance Stage)
    > Is there relevant information for post-market monitoring?

    - The metrics are relevant when the model is retrained and more annotated data, possibly multi-label, is generated. This event may be triggered by [feedback](../../../4_Maintenance/Support/QG_FeedbackLoops_(TBE_Segmentation).md) on a noticable decline in model performance by the [physician who interacts with the software](../../../../1_System/Stakeholder/3_Passive/Physician_(PassiveStakeholder).md) (e.g. model drift, data drift may occur)

<br>

### 2. Quality Gate Creation (Design-Decision-Specific Dimensions)

#### Dimension 1: Content
> Which information is generated?

A combination of metrics is selected, interpreted in combination with the segmentation output. All metrics range from 0-1 and should be maximized.

- Dice Score / F1-Score as primary metric (harmonic mean of sensitivity and precision)
> 0.8637
- Intersection over Union (IoU) / Jaccard Score (also an F-measure-based metric that stronger penalized over- and undersegmentation)
> 0.7719
- Sensitivity / Recall / True Positive Rate (how well does the model detect the segmented esophagus)
> 0.8307
- Specificity / True Negative Rate (how well does the model predict the background) - highlights functionality - usually expected close to 1 due to high imbalance regarding more pixels belonging to the background than the region of interest
> 0.9723

![nnU-Net-output](../../../../../imgs/Achalasia/nn-Unet.png){width=300 height=}
> nnU-Net output on the test set (left: raw data, middle: labeled mask, right: model output)

The metrics align well with the segmentation output.

#### Dimension 2: Method
> How is the information generated? 

- Medical images are characterized by high data imabalance: the region of interest (ROI) is comparably less prevalent with respect to the amount of background pixels
- Therefore, true positives (TP) and true negatives (TN) should not be weighted equally

#### Dimension 3: Representation
> How should which information should be presented to which stakeholders and when?

##### Developer

- Interpret the model's overall segmentation performance in combination with the individually generated output masks on test data

<br>

#### Evaluation
> What are open questions when applying the generated information?

- State of the Art nnU-Net is the best performing model with the current state of labeled data
- Other metrics such as Cohen's kappa, or the average hausdorff distance can be appended 

- The results of the segmentation model indicate strong performance across key metrics, corresponding to the visual results
- Overall, these results point to a well-performing model with balanced detection capabilities, while fine-grained esophagus' shapes need to be adjusted by the physician interacting with the model.

<br>

### 3. Additional Information

#### Risk Management

- ##### Poses Risk(s)
    > Are there related risks?

- ##### Implements Risk Control(s)
    > Are there risk controls implemented?

#### ...
