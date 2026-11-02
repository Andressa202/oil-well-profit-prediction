# 🛢️ Oil Well Profit Prediction | Machine Learning & Risk Analysis

### Optimizing Oil Field Investment Decisions with Linear Regression and Bootstrap Simulation

**Python • Pandas • NumPy • Scikit-learn • Linear Regression • Bootstrapping • Risk Analysis**

## 📌 Project Overview

Selecting the right location for oil well development is a major financial decision. Companies must consider not only the expected volume of oil reserves but also potential profitability and investment risks.

This project was developed for **OilyGiant**, a fictional oil extraction company, to identify the most promising region for developing new oil wells.

Using geological data from three regions, the project applies Linear Regression to predict oil reserve volumes and bootstrap simulation to estimate potential profits, confidence intervals, and financial risks.

**Business Goal:** Select the region offering the best balance between expected profitability and financial risk.

## 🎯 Project Objectives

- Explore geological data from three potential oil-producing regions.
- Train Linear Regression models to predict oil reserves.
- Evaluate model accuracy using Root Mean Squared Error (RMSE).
- Calculate the minimum production volume required to break even.
- Select the most promising wells based on predicted reserves.
- Estimate investment profitability.
- Apply bootstrap simulation to quantify financial uncertainty.
- Recommend the most suitable region for investment.

## 🛠️ Technologies Used

| Technology | Application |
|---|---|
| Python | Data processing and modeling |
| Pandas | Data manipulation and analysis |
| NumPy | Numerical operations and simulation |
| Scikit-learn | Linear Regression and model evaluation |
| Jupyter Notebook | Analysis and documentation |

## 📂 Dataset Description

Three datasets represent geological information from different regions.

| Dataset | Description |
|---|---|
| `geo_data_0.csv` | Geological data for Region 0 |
| `geo_data_1.csv` | Geological data for Region 1 |
| `geo_data_2.csv` | Geological data for Region 2 |

Each dataset includes:

- `id` — Unique oil well identifier
- `f0`, `f1`, `f2` — Geological characteristics
- `product` — Oil reserve volume, measured in thousands of barrels

The initial inspection found no missing values or duplicate records.

## 🔄 Project Methodology

### 1. Data Preparation

The geological datasets were loaded and inspected to verify their structure, completeness, and consistency.

The three geological features were selected as predictors, while `product` was used as the target variable.

### 2. Model Training

A separate Linear Regression model was trained for each region.

Each dataset was divided into:

- 75% training data
- 25% validation data

A fixed random state was used to support reproducibility.

### 3. Model Evaluation

Model performance was evaluated using RMSE and average predicted oil reserve volume.

| Region | Average Predicted Reserves | RMSE |
|---|---:|---:|
| Region 0 | 92.40 | 37.76 |
| **Region 1** | **68.71** | **0.89** |
| Region 2 | 94.77 | 40.15 |

*Reserve volumes and RMSE are expressed in thousands of barrels.*

**Key Finding:** Region 1 achieved the lowest RMSE, indicating substantially more accurate predictions in the validation dataset.

Although Region 1 did not have the highest average predicted reserves, its model demonstrated the strongest predictive performance.

## 💰 Investment Conditions

The company established the following investment parameters:

| Parameter | Value |
|---|---:|
| Development budget | $100 million |
| Wells explored per sample | 500 |
| Wells selected for development | 200 |
| Revenue per thousand barrels | $4,500 |
| Maximum acceptable loss risk | 2.5% |

### Break-Even Analysis

The minimum average reserve volume required per developed well was calculated as:

\[
\frac{100,000,000}{200 \times 4,500}
\approx 111.11
\]

Each selected well must therefore produce approximately **111.11 thousand barrels** on average to cover the investment cost.

This calculation highlights the importance of selecting wells with the greatest predicted production potential.

## 📊 Profit Calculation

A profit calculation function was developed to:

1. Rank wells by predicted reserve volume.
2. Select the 200 wells with the highest predictions.
3. Retrieve the corresponding actual reserve volumes.
4. Calculate revenue from the selected wells.
5. Subtract the initial development budget.

This approach evaluates the financial implications of model-based well selection.

## 🎲 Bootstrap Risk Analysis

Bootstrap simulation was used to estimate the uncertainty associated with investment outcomes.

The procedure included:

- 1,000 bootstrap iterations per region.
- Sampling 500 wells with replacement.
- Selecting the 200 most promising wells in each sample.
- Calculating profit for every iteration.
- Estimating mean profit, a 95% confidence interval, and the probability of financial loss.

## 📈 Investment Results

| Region | Mean Profit | 95% Confidence Interval | Loss Risk |
|---|---:|---|---:|
| Region 0 | $6.06M | $0.10M to $12.46M | 2.5% |
| **Region 1** | **$6.65M** | **$1.81M to $12.06M** | **0.2%** |
| Region 2 | $5.85M | -$0.01M to $12.12M | 2.6% |

### Region 0

Region 0 demonstrated positive expected profitability, but its estimated loss risk reached the company's maximum acceptable threshold.

### Region 1 — Recommended

Region 1 achieved the highest estimated mean profit and the lowest probability of financial loss.

Its estimated loss risk of just **0.2%** was substantially below the company's 2.5% threshold.

### Region 2

Region 2 presented the lowest expected mean profit and a loss probability of 2.6%, exceeding the maximum acceptable risk.

## 🏆 Final Recommendation

**Region 1 is the recommended location for oil well development.**

The decision is supported by three factors:

- Highest estimated average profit: **$6.65 million**
- Lowest estimated loss risk: **0.2%**
- Best predictive accuracy: **RMSE of 0.89**

The results demonstrate that investment decisions should consider predictive reliability, expected returns, and financial uncertainty rather than relying solely on average production estimates.

## 💡 Key Skills Demonstrated

- Supervised Machine Learning
- Regression Modeling
- Train/Validation Splitting
- Predictive Model Evaluation
- Financial Profit Calculation
- Bootstrap Simulation
- Confidence Interval Estimation
- Risk Assessment
- Data-Driven Decision Making

## ⚠️ Limitations

- The analysis is based on historical geological data.
- Financial estimates depend on the project's fixed budget and revenue assumptions.
- Bootstrap results represent estimated uncertainty under the sampling procedure.
- Actual production outcomes may differ from model predictions.
- Additional operational, environmental, and geological considerations would be necessary before a real investment decision.

## 🚀 How to Run the Project

1. Clone or download the repository.
2. Install the required Python libraries.
3. Place the three CSV datasets in a local `data/` directory.
4. Update the dataset paths in the notebook.
5. Open the notebook in Jupyter Notebook or JupyterLab.
6. Execute the cells sequentially.

### Install Dependencies

```bash
pip install pandas numpy scikit-learn notebook
```

## 📈 Conclusion

This project demonstrates how machine learning and statistical simulation can support financial decision-making in the energy industry.

By combining Linear Regression with bootstrap-based profit estimation, the analysis identified Region 1 as the most attractive investment opportunity.

The project showcases practical skills in **predictive modeling, statistical analysis, risk assessment, and business-oriented data science**.

## 👩‍💻 Author

**Andressa Miranda**

Computer Science | Data Analytics | Python | Machine Learning

[GitHub Profile](https://github.com/Andressa202)

*Developed as part of the TripleTen Data Science program.*

