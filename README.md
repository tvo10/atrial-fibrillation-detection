# Atrial Fibrillation Detection 
![cover_photo](./img/AFib-Animation.gif)

# Capstone Project II
1.	[Problem Statement](#1-problem-statement)
2.	[Data Sources](#2-data-sources)
3.	[Reports](#3-reports)
4.  [Data Wrangling](#4-data-wrangling)
5.  [EDA](#5-eda)
6.  [Modeling](#6-modeling)
7.  [Model Evaluation](#7-model-evaluation)
<br/><br/>

## 1. Problem Statement:
How to help patients and physicians detect Atrial Fibrillation (AF) in an early stage and provide treatment promptly as needed to reduce 10% of patients who are at high risk of having a stroke, a heart attack, and even a heart failure caused by AF by the end of 2021?

### 1.1. Background:
Atrial fibrillation (AF) is an irregular and often rapid heart rate that can increase your risk of strokes, heart failure and other heart-related complications. AF symptoms often include heart palpitations, shortness of breath and weakness. AF is also independently associated with a significantly greater risk of mortality. For instance, AF patients have a 46% greater risk of mortality than patients without AF and the rate of mortality is 40% among new patients diagnosed with AF. Around 15-30% of patients are asymptomatic, which is of concern as AF is a major risk factor for stroke. As AF progresses, patients are more likely to experience greater impairments in their quality of life, such as increased pain and discomfort. Early detection and appropriate management reduce stroke risk by two-thirds. As a result, early detection of AF is important to ensure prompt and adequate management which not only aims to control symptoms but to avoid later complications.

## 2. Data Sources:
- coorteeqsrafva.csv: This is a subset of the PTB-XL, a large publicly available electrocardiography dataset, found on [Kaggle](https://www.kaggle.com/arjunascagnetto/ptbxl-atrial-fibrillation-detection), which consists of 6428 rows and 30 columns. 
- ecgeq-500hzsrfava.npy: This numpy file is a 3D array, which contains 6428 layers, 5000 rows, and 12 columns. 12 columns represent for 12 leads. An ECG lead is a graphical description of the electrical activity of the heart and it is created by analysing several electrodes.

## 3. Reports:
1. [Capstone Project II Final Report](https://github.com/tvo10/atrial-fibrillation-detection/blob/main/afib_detection_report.pdf)
4. [Capstone Project II Final Presentation](https://docs.google.com/presentation/d/1hBh9Pb7svQN0gg5JdP9LnS4gQ1PKYUQXwtJT0ZPAKVg/edit#slide=id.gdbd7bf2743_0_47)

## 4. Data Wrangling
[Data Wrangling](https://github.com/tvo10/atrial-fibrillation-detection/blob/main/01_afib_detection_data_wrangling.ipynb)

## 5 EDA:
### 5.1 Which gender usually has a higher risk of getting AF?
<p>
    <img src="https://github.com/tvo10/atrial-fibrillation-detection/blob/master/img/rhythm_by_sex.png" />
</p>
<p>Female patients are at higher risk of getting AF than male patients.</p>

### 5.2 Which age-group is associated with higher risk of having AF than others?
<p>
  <img src="https://github.com/tvo10/atrial-fibrillation-detection/blob/master/img/rhythm_by_age.png" />
</p>
<p>Patients who are 70 to 89 years old have a higher risk of having AF than others.</p>
            
### 5.3 What is the common weight of patients who have AF?
<p>
  <img src="https://github.com/tvo10/atrial-fibrillation-detection/blob/master/img/rhythm_by_weight.png" />
</p>
<p>Patients who have AF are usually less than 60 kg, or 60 to 79 kg.</p>

### 5.4 What is the common height of patients who have AF?
<p>
  <img src="https://github.com/tvo10/atrial-fibrillation-detection/blob/master/img/rhythm_by_height.png" />
</p>
<p>Patients who have AF are usually from 1.50 m to 1.79 m.</p>

### 5.5 What is the most common heart's electrical axis associated with AF patients?
<p>
  <img src="https://github.com/tvo10/atrial-fibrillation-detection/blob/master/img/rhythm_by_heart_axis.png" />
</p>
<p>Most AF patients have normal heart's electrical axis.</p>

### 5.6 Normal ECG
<p>
  <img src="https://github.com/tvo10/atrial-fibrillation-detection/blob/master/img/normal_ecg.png" />
</p>

### 5.7 Atrial Fibrillation ECG
<p>
  <img src="https://github.com/tvo10/atrial-fibrillation-detection/blob/master/img/atrial_fibrillation_ecg.png" />
</p>

### 5.8 Other Arrhythmia ECG
<p>
  <img src="https://github.com/tvo10/atrial-fibrillation-detection/blob/master/img/other_arrhythmia_ecg.png" />
</p>

More details of EDA:
[Exploratory Data Analysis](https://github.com/tvo10/atrial-fibrillation-detection/blob/main/02_afib_detection_eda.ipynb)

## 6. Modeling
<p>
<img src = "https://github.com/tvo10/atrial-fibrillation-detection/blob/master/img/modeling.png" />
</p>

For more details: 
[Modeling](https://github.com/tvo10/atrial-fibrillation-detection/blob/main/04_afib_detection_modeling.ipynb)
