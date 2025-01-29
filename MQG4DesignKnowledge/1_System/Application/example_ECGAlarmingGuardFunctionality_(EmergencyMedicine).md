---
tags: [{Name: Electrocardiogram_(ECG)_AlarmingGuardFunctionality}, {Intent: FictionalUseCase}, {Applicability: EmergencyMedicine}, {Usage Example: MultiLabelClassificationPerformanceMetrics}]
---

## Electrocardiogram (ECG) Alarming Guard Functionality *Custodian* (Use in Emergency Medicine)

### Purpose
We aim to improve patient welfare:
- The system is intended to help identify patients with cardiological complaints as early as possible, since time often is a critical factor from a clinical perspective.

### Capability
Multi-label classification of 12-Lead ECGs

### Area of Impact
The cooperation between medical personnel and the intelligent system is expected to generally improve critical diagnosis.

### Environment of Use
The fictional real-world setting is an intelligent system that is used in emergency medicine (e.g. ambulances and general practitioner's practices), where the medical personnel is not specialized in ECGs and patients at risk could appear. 

### Intended Workflow
t.b.d.

### Domain
Emergency Medicine

#### Model Output

From a medical, treatment-oriented viewpoint, the abnormalities included are:
- one form of atrial fibrillation
- atrial flutter
- (paroxysmal) ventricular and supraventricular tachycardia
- AV block II and III
- general myocardial infarction signs - all stages and other ischemia (multiple labels)
- ST elevation and depression
- pericarditis (not in data set)
- long QT syndrome
- Other refers to all remaining pathological ECG labels. Most of these labels do not allow for a specific therapy without further examinations. Thus, if one of these labels is displayed in an ECG, the patient will most likely be transferred to a hospital.

Explanation:
- Some labels are entirely independent of one another and can coexist. Evaluating these combinations is nonsensical for our use case with an alarming guard functionality, and comparing T-negative with AV block or axis, for instance is clinically illogical
> Overall, the applied tendency leans towards the comparison of labels that are mutually exclusive.

- From a medical viewpoint ECG diagnosis alone often do not determine whether a and if so which therapy (medication or electrical) follows, but rather the severity of the diagnosis (ventricular tachycardia can cause heart rates from 120 to 240), as well as the patient's clinical condition (asymptomatic to unconscious). 
- As a result, frequently only the combination of multiple labels leads to a diagnosis and consequently to a therapy. For an alarming guard functionality, it appears more reasonable to only compare labels that represent specific diagnoses. Not all pathological, but unspecific labels automatically lead to therapy. 
> In that case, a comparison would be meaningless, or the data set would have to provide an appropriate evaluation label for the respective diagnosis as a combination of multiple labels. 
> Consequently, if a label is missing (or misdiagnosed), it does not automatically result in an incorrect diagnosis. 