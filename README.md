# Rain Prediction using Bayesian Networks

## Project Overview
This project investigates the use of **Bayesian Networks** for predicting whether it will rain tomorrow. The key motivation is to explore the impact of incorporating **domain knowledge** into the design of AI models, particularly when there is limited training data available. The study demonstrates how leveraging domain expertise can yield robust models with reduced data requirements.

### Objectives
1. **Primary Goal**: Develop and evaluate Bayesian Networks for weather prediction tasks, focusing on predicting rainfall.
2. **Secondary Goal**: Test the hypothesis that **increasing domain knowledge** while reducing training data can still result in high-performing models.

## What Was Done
1. **Data Preparation**:
   - The dataset was preprocessed using **Pandas** to handle missing values and discretize continuous features.
   - Data imbalance was addressed by undersampling the majority class using **scikit-learn**.

2. **Baseline Model**:
   - A **Decision Tree Classifier** was trained and fine-tuned to establish a performance benchmark.

3. **Bayesian Network Architectures**:
   - Three different Bayesian Network models were developed using **pgmpy**:
     - **Model 1**: Features treated as independent.
     - **Model 2**: Incorporates intuitive structure for better understanding.
     - **Model 3**: Uses enhanced domain knowledge with fewer features (7 instead of 11) to test the trade-off between data reduction and performance.

4. **Performance Evaluation**:
   - Models were evaluated based on **accuracy** and **training time** to measure the effectiveness of using domain knowledge.

## Installation
All the necesary software to run the program is listed in the **requirements.txt** file. 
To install the dependencies:
```bash
pip install -r requirements.txt
```

## Results
The experiments yielded promising results:

- The **Decision Tree Classifier** achieved an accuracy of **76.5%**.
- **Second Bayesian Network** (11 features) achieved **75.5% accuracy**, with a training time of **0.16 seconds**.
- **Third Bayesian Network** (7 features, reduced data) achieved **74% accuracy**, with a training time of **0.08 seconds**.

### Key Findings
- Reducing the number of features by **35%** (from 11 to 7) resulted in only a **1.5% drop in accuracy**.
- Training time for the reduced-data model was **halved**, demonstrating the efficiency of incorporating domain knowledge into model design.

## Dataset
The dataset used for this project can be found on Kaggle:  
[Weather Dataset - Rattle Package](https://www.kaggle.com/datasets/jsphyg/weather-dataset-rattle-package/data)

## Conclusion
This project successfully demonstrates the potential of using **domain knowledge** to design efficient models with reduced data. The findings highlight the effectiveness of **Bayesian Networks** in weather prediction tasks, offering insights into trade-offs between model complexity, data availability, and performance.
A comprehensive project report detailing the methodology, results, and analysis is included in the repository. Refer to **`Clotan Paul report.pdf`** for an in-depth understanding.

