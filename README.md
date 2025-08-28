
# Temporal Analysis of Bidirectional Links Between Physical Activity and Sleep Patterns

📊 **University of Trento – Social Dynamics Lab**
📅 Academic Year: 2024/25
👤 Author: *Yishak Tadele Nigatu*


**Course Instructors**
👤 ![Professor Ivano Bison](https://www.linkedin.com/in/ivano-bison-75b7b926a/)
👤 ![Professor Giuseppe Alessandro Veltri](https://www.giuseppeveltri.eu/)

---

## 📌 Overview

![Physical Activity and Sleep](eda_figures/pa.jpg)  
[Image Source](https://www.sleepfoundation.org/physical-activity)

This project investigates the temporal dynamics between **physical activity** and **sleep patterns** using longitudinal data collected from students at the University of Trento. The dataset combines **time-diary entries, self-reported surveys, and wearable sensor data** to explore:

1. **Behavioral profiling** of activity, nutrition, and sleep.
2. **Clustering of lifestyle patterns** using unsupervised learning.
3. **Temporal modeling** of bidirectional relationships between activity and sleep using advanced statistical models.

The project forms part of the course *Social Dynamics Lab*.

---

## 📂 Repository Structure

```bash
├── data/                # Raw and preprocessed datasets (restricted access)
├── docs/                # Documentation and report files
├── eda_figures/             # Figures, tables, and model outputs
├── 1_data_preprocessing.ipynb/   # Scripts for cleaning and merging raw data
├── 2_user_profiling.ipynb      # User profiling and clustering algorithms
├── 3_data_analysis.ipynb                 #Explorative Data Analysis
├── 4_bidirectional_analysis.ipynb        # Mixed-effects models, SEM, and time-series analysis
└── README.md            # Project description and usage
```

---

## 🧰 Data Sources

The study uses multimodal longitudinal data from the *WeNet – The Internet of Us* project:

* **Time-Diary Notifications:** Self-reported activity, nutrition, and sleep entries.
* **Survey Data:** Demographics and Big Five personality traits.
* **Motion Sensors:** Step counts and physical activity intensity.

Key variables include:

* **Physical Activity:** 8 activity categories grouped into low, moderate, and high intensity.
* **Nutrition:** 20+ food categories mapped to nutrient values using the FAO Global Nutrient Conversion Table.
* **Sleep Quality:** 5-point Likert scale (interpolated where missing).
* **Individual Characteristics:** Demographics + personality traits.

---

## 🔄 Methodology

1. **Preprocessing**

   * Engagement filtering (≥60% diary response rate → 192 participants).
   * Timestamp alignment (−5h social time adjustment).
   * Conversion of food categories into daily nutrient values.
   * Encoding and aggregation of activity intensity and diversity (Shannon entropy).
   * Interpolation of missing sleep quality values.

2. **Exploratory Analysis**

   * Data quality checks, missing data patterns.
   * Descriptive statistics of demographics, nutrition, sleep, and activity.

3. **User Profiling & Clustering**

   * Creation of lifestyle profiles (activity, nutrition, sleep).
   * Unsupervised clustering (k-means, hierarchical, GMM, DBSCAN).
   * Cluster evaluation with Silhouette, Calinski-Harabasz, and Davies-Bouldin indices.

4. **Temporal Modeling**

   * Mixed-effects models for within- and between-person effects.
   * Structural Equation Models (SEM, cross-lagged panel design).
   * Analysis of autoregressive and cross-domain temporal effects.

---

## 📊 Key Findings

* **Strong autoregressive patterns** were found for sleep and activity separately.
* **No significant cross-lagged effects** → activity and sleep appear independent over time.
* **Concurrent associations**: more active students reported higher sleep quality overall.
* **Activity diversity** was a stronger predictor of engagement than activity volume.
* Clustering revealed three lifestyle groups:

  * *Cluster 0:* Low activity, inconsistent diet, lower sleep quality.
  * *Cluster 1:* Moderate activity, balanced nutrition.
  * *Cluster 2:* High activity, consistent diet, higher sleep quality.

---

## ⚠️ Limitations

* High missingness in sleep data (>98%), handled with interpolation.
* Reliance on self-reported sleep and nutrition data.
* Limited sensor coverage (128 participants with step data).
* Short study period and homogeneous sample (university students).
* Possible scaling issues in nutrient conversion.

---

## 🚀 Future Work

* Apply **multiple imputation** instead of simple interpolation for missing sleep.
* Use **Random Intercept Cross-Lagged Panel Models (RI-CLPM)** or **mlVAR** for better within-person inference.
* Validate self-reported sleep against **actigraphy-based estimates**.
* Extend study to more diverse populations and longer observation periods.

---

## ⚙️ Installation & Usage

Clone the repository:

```bash
git clone https://github.com/isaaclucky/sleep_and_physical_activity-bidirectional_behavioral_study.git
cd sleep_and_physical_activity-bidirectional_behavioral_study
```

Install dependencies:

```bash
pip install -r requirements.txt
```


## 👨‍💻 Author

**Yishak Tadele Nigatu**

* 📧 Email: [yishaktadele.nigatu@studenti.unitn.it](mailto:yishaktadele.nigatu@studenti.unitn.it)
* 📧 Personal Email: [isaaclucky88@gmail.com](mailto:isaaclucky88@gmail.com)
* 🎓 University of Trento, Italy


