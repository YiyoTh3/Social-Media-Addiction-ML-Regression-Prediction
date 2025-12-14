# Social Media Addiction Severity Prediction (Supervised Regression)

## Project Overview

The objective of this project is to apply advanced supervised learning techniques (Regression) to predict the numerical severity of social media addiction (`Addicted_Score`) among a student demographic. The work focuses on constructing a highly accurate predictive model and subsequently performing rigorous feature analysis to determine the factors most strongly correlated with higher addiction scores.

## Methodology and Technical Execution

### Technologies Used

* **Language:** Python
* **Environment:** Jupyter Notebook / Google Colab
* **Core Libraries:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn

### Validation Strategy

The model's stability and predictive reliability were ensured through the application of **5 Fold Cross Validation**. This rigorous validation confirms the model’s performance is consistent across varied subsets of the dataset.

## Analysis and Key Findings

The regression analysis yielded a robust predictive model, leading to several specific conclusions regarding the components of the Addicted Score.

### Defining Feature Correlation

A deeper inspection of the feature importance revealed a near perfect inverse correlation (0.9451) between the `Mental_Health_Score` and the `Addicted_Score`.

**Implication:** Within this specific dataset, the predictive model is recognizing that the `Addicted_Score` is heavily, if not mathematically, derived from, the `Mental_Health_Score`. This signifies that `Mental_Health_Score` is the key defining feature of the addiction severity metric itself.

### Secondary Influencers

While the score is dominated by the mental health component, the model identified secondary factors with measurable, though lower, predictive importance. These include:

* `Conflicts_Over_Social_Media`
* `Usage_to_Sleep_Ratio`

### Model Reliability

The **Residual Plot** analysis confirmed the absence of any systematic pattern in the errors, thus validating the overall reliability and suitability of the regression model across the score range.

## Future Research and Actionable Insights

The primary implication is that any intervention based solely on the current Addicted Score must recognize its intrinsic dependence on the mental health component.

To derive new, actionable insights independent of this mental health baseline, future analyses should be structured to:

1.  Explore the relationship between the secondary factors and the addiction score's **residual variance** (the part of the score not explained by the `Mental_Health_Score`).
2.  Develop separate predictive models specifically focused on isolating the effect of usage habits on self reported well being.

## Project Setup

To clone and execute this analysis locally, use the following commands:

```bash
git clone [Your Repository URL Here]
cd Social-Media-Addiction-Analysis-Python
# Assuming requirements.txt is generated, or libraries are installed
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
jupyter notebook Social_Media_Addiction_R.ipynb
