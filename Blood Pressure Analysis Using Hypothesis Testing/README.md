# Blood Pressure Statistical Analysis Using T-Tests

This repository contains a complete statistical analysis project that explores the use of one-sample and two-sample t-tests (Welch’s t-test) to analyze blood pressure data. The dataset comprises health records of approximately 200 individuals, including attributes such as gender, age, systolic and diastolic blood pressure, and diabetic status.

## Theory

**One-Sample t-Test**  
The one-sample t-test is used to determine whether the mean of a single sample significantly differs from a known or hypothesized population mean. This is appropriate when the population standard deviation is unknown and the sample size is small.

**Formula:**  
`t = (x̄ - μ) / (s / √n)`  
Where:  
- x̄ = sample mean  
- μ = population mean  
- s = sample standard deviation  
- n = sample size

**Two-Sample t-Test (Welch’s t-Test)**  
This test compares the means of two independent groups, particularly when variances are unequal. It is more reliable in real-world scenarios where equal variance cannot be assumed.

**Formula:**  
`t = (x̄₁ - x̄₂) / √(s₁²/n₁ + s₂²/n₂)`  
Where:  
- x̄₁, x̄₂ = sample means  
- s₁², s₂² = sample variances  
- n₁, n₂ = sample sizes

## Objective

1. To determine whether the average blood pressure (systolic and diastolic) in the sample significantly differs from the standard clinical values of 120/80 mmHg using a one-sample t-test.
2. To assess whether diabetic individuals have significantly different blood pressure than non-diabetic individuals using a two-sample Welch’s t-test.

## Tools and Environment

- **Programming Language:** Python
- **Environment:** Google Colaboratory (Colab)
- **Libraries Used:**
  - `pandas` – for data manipulation
  - `numpy` – for numerical computation
  - `scipy.stats` – for conducting t-tests
  - `matplotlib`, `seaborn` – for data visualization

## Data

The dataset was synthetically generated using ChatGPT and contains data for around 200 individuals. Each record includes:
- Gender
- Age
- Systolic Blood Pressure
- Diastolic Blood Pressure
- Diabetic Status (Yes/No)

## Methodology

1. **Data Import and Setup:** The CSV file was loaded using pandas. Initial exploration included checking the structure and verifying data consistency.
2. **One-Sample t-Test:** Applied to test if average systolic and diastolic pressures deviate from 120 and 80 mmHg, respectively.
3. **Two-Sample t-Test (Welch’s):** Conducted to evaluate differences in blood pressure between diabetic and non-diabetic groups.
4. **Visualization:** Graphs (bar plots with error bars) were generated to illustrate the distribution and test outcomes.

## Results

**One-Sample t-Test:**
- **Systolic BP:**  
  - Mean = 124.35 mmHg  
  - t-statistic = 5.23  
  - p-value = 0.0000  
  - Conclusion: Significantly higher than standard value.

- **Diastolic BP:**  
  - Mean = 81.99 mmHg  
  - t-statistic = 2.73  
  - p-value = 0.0071  
  - Conclusion: Significantly higher than standard value.

**Two-Sample t-Test (Welch’s):**
- **Systolic BP (Diabetic vs Non-Diabetic):**  
  - Mean (Diabetic) = 127.48 mmHg  
  - Mean (Non-Diabetic) = 121.17 mmHg  
  - t-statistic = 3.76  
  - p-value = 0.0002  
  - Conclusion: Diabetics have significantly higher systolic BP.

- **Diastolic BP (Diabetic vs Non-Diabetic):**  
  - Mean (Diabetic) = 84.33 mmHg  
  - Mean (Non-Diabetic) = 80.52 mmHg  
  - t-statistic = 2.48  
  - p-value = 0.0139  
  - Conclusion: Diastolic BP is significantly higher among diabetics.

## Description

This project evaluates how blood pressure values vary from clinical standards and between health conditions using hypothesis testing techniques. It demonstrates a practical application of t-tests in healthcare data analytics, using both statistical reasoning and data visualization.

## Conclusion

The analysis confirmed that:
- The average blood pressure in the synthetic sample is significantly higher than the standard values (120/80 mmHg).
- Diabetic individuals consistently show higher systolic and diastolic pressures compared to non-diabetics.

**Gap:**  
This study uses synthetic data and only considers diabetes as a factor affecting blood pressure. Other real-world variables such as BMI, medication, smoking habits, and lifestyle were not included.

**Future Work:**
- Incorporate real medical records from broader demographics.
- Include additional factors (e.g., cholesterol, BMI).
- Apply multivariate statistical models or machine learning classifiers.

## References

[1] SciPy Developers, “scipy.stats.ttest_1samp and ttest_ind — Statistical functions,” SciPy Documentation, [Online]. Available: https://docs.scipy.org/doc/scipy/.  
[2] Google, “Google Colaboratory: A cloud-based Jupyter notebook environment,” Google Research, [Online]. Available: https://colab.research.google.com/.  
[3] OpenAI, “ChatGPT: Language model used for dataset generation and explanation,” OpenAI Platform, [Online]. Available: https://chat.openai.com/.  
[4] W. McKinney, “Data structures for statistical computing in Python,” in Proceedings of the 9th Python in Science Conference, Austin, TX, 2010, pp. 51–56.  
[5] M. Waskom, “Seaborn: Statistical data visualization,” Seaborn Documentation, [Online]. Available: https://seaborn.pydata.org/.  
[6] World Health Organization, “Blood pressure standards,” WHO, [Online]. Available: https://www.who.int/.  

