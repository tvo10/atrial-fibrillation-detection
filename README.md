# Atrial Fibrillation Detection 
![cover_photo](./img/AFib-Animation.gif)

# Capstone Project II
1.	[Background](#1-background)
2.	[Data Sources](#2-data-sources)
3.  [Data Wrangling](#3-data-wrangling)
4.  [EDA](#4-eda)
5.  [Feature Engineering](#5-feature-engineering)
6.  [Modeling](#6-modeling)
7.	[Reports](#7-reports)

## 1. Background
Atrial fibrillation (AF) is an irregular and often rapid heart rate that can increase your risk of strokes, heart failure and other heart-related complications. AF symptoms often include heart palpitations, shortness of breath and weakness. AF is also independently associated with a significantly greater risk of mortality. For instance, AF patients have a 46% greater risk of mortality than patients without AF and the rate of mortality is 40% among new patients diagnosed with AF. Around 15-30% of patients are asymptomatic, which is of concern as AF is a major risk factor for stroke. As AF progresses, patients are more likely to experience greater impairments in their quality of life, such as increased pain and discomfort. Early detection and appropriate management reduce stroke risk by two-thirds. As a result, early detection of AF is important to ensure prompt and adequate management which not only aims to control symptoms but to avoid later complications.

### Problem Statement
How to help patients and physicians detect Atrial Fibrillation (AF) in an early stage and provide treatment promptly as needed to reduce 10% of patients who are at high risk of having a stroke, a heart attack, and even a heart failure caused by AF by the end of 2021?

## 2. Data Sources
- **coorteeqsrafva.csv:** This is a subset of the PTB-XL, a large publicly available electrocardiography dataset, found on [Kaggle](https://www.kaggle.com/arjunascagnetto/ptbxl-atrial-fibrillation-detection), which consists of 6428 rows and 30 columns. 
- **ecgeq-500hzsrfava.npy:** This numpy file is a 3D array, which contains 6428 layers, 5000 rows, and 12 columns. 12 columns represent for 12 leads. An ECG lead is a graphical description of the electrical activity of the heart and it is created by analysing several electrodes.


## 3. Data Wrangling
[Data Wrangling](https://github.com/tvo10/atrial-fibrillation-detection/blob/main/01_afib_detection_data_wrangling.ipynb)

## 4. EDA
### Which gender usually has a higher risk of getting AF?
<p>
    <img src="https://github.com/tvo10/atrial-fibrillation-detection/blob/main/img/rhythm_by_sex.PNG" />
</p>
<p><b>➣ Female patients are at higher risk of getting AF than male patients.</b></p>

### Which age-group is associated with higher risk of having AF than others?
<p>
  <img src="https://github.com/tvo10/atrial-fibrillation-detection/blob/main/img/rhythm_by_age.PNG" />
</p>
<p><b>➣ Patients who are 70 to 89 years old have a higher risk of having AF than others.</b></p>
            
### What is the common weight of patients who have AF?
<p>
  <img src="https://github.com/tvo10/atrial-fibrillation-detection/blob/main/img/rhythm_by_weight.PNG" />
</p>
<p><b>➣ Patients who have AF are usually less than 60 kg, or 60 to 79 kg.</b></p>

### What is the common height of patients who have AF?
<p>
  <img src="https://github.com/tvo10/atrial-fibrillation-detection/blob/main/img/rhythm_by_height.PNG" />
</p>
<p><b>➣ Patients who have AF are usually from 1.50 m to 1.79 m.</b></p>

### What is the most common heart's electrical axis associated with AF patients?
<p>
  <img src="https://github.com/tvo10/atrial-fibrillation-detection/blob/main/img/rhythm_by_heart_axis.PNG" />
</p>
<p><b>➣ Most AF patients have normal heart's electrical axis.</b></p>

### Normal ECG
<p>
  <img src="https://github.com/tvo10/atrial-fibrillation-detection/blob/main/img/normal_ecg.PNG" />
</p>

### Atrial Fibrillation ECG
<p>
  <img src="https://github.com/tvo10/atrial-fibrillation-detection/blob/main/img/atrial_fibrillation_ecg.PNG" />
</p>

### Other Arrhythmia ECG
<p>
  <img src="https://github.com/tvo10/atrial-fibrillation-detection/blob/main/img/other_arrhythmia_ecg.PNG" />
</p>

For more details: 
[Exploratory Data Analysis](https://github.com/tvo10/atrial-fibrillation-detection/blob/main/02_afib_detection_eda.ipynb)

## 5. Feature Engineering
Since this project is all about the pattern recognition. We would like to detect Atrial Fibrillation cases using the 12 leads in the numpy file along with some of the features in the csv file. Without using the 12 leads, detecting AF cases only using height, weight, age, etc. is not persuading the cardiology physicians. Therefore, we generated a dataset that includes all the features from the numpy file and 14 features from the csv file. However, to reduce the size of the dataset that makes it easier to train the model, we only keep 700 rows instead of 5000 rows from the numpy file. The final dataset has a total of 4,319,176 observations and 26 variables. Since the final dataset is almost 600 MB, we cannot upload it to GitHub, but you can get a copy of it [here](https://drive.google.com/file/d/12UfgiaV4-YbcUhtRzPv1kS_AO3L1oMcE/view?usp=sharing).

- **Features:** `I`, `II`, `III`, `aVF`, `aVR`, `aVL`, `V1`, `V2`, `V3`, `V4`, `V5`, `V6`, `age`, `sex`, `height`, `weight`, `nurse`, `site`, `device`, `heart_axis`, `validated_by`, `second_opinion`, `validated_by_human`, `pacemaker`, `strat_fold`
- **Label:** `ritmi`

## 6. Modeling
We applied the Random Forest algorithm, then tuned the model with GridSearchCV and got almost 0.99 for the accuracy score.
<p>
<img src = "https://github.com/tvo10/atrial-fibrillation-detection/blob/main/img/modeling.PNG" />
</p>

For more details: 
[Modeling](https://github.com/tvo10/atrial-fibrillation-detection/blob/main/04_afib_detection_modeling.ipynb)

## 7. Reports
1. [Capstone Project II Final Report](https://github.com/tvo10/atrial-fibrillation-detection/blob/main/afib_detection_report.pdf)
2. [Capstone Project II Final Presentation](https://docs.google.com/presentation/d/1hBh9Pb7svQN0gg5JdP9LnS4gQ1PKYUQXwtJT0ZPAKVg/edit?usp=sharing)
