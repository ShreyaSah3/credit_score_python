# credit_score_python
Hi,

# Subprime Mortgage Lending Model

This project developed a model to assist in making lending decisions for subprime mortgages, balancing profit and market share.

## Data

The dataset consisted of 3000 loan applications, each described by 30 variables. These variables included:

* Bankruptcy indicators
* Public derogatories
* Financial inquiries
* Trade lines

## Methodology

1. **Data Cleaning and Standardization:** Python was used for this stage, preparing the data for modeling.

2. **Model Building:** A Logistic Regression Classifier was initially trained using an 80/20 train-test split. While the model achieved high accuracy, it exhibited low recall due to the imbalanced nature of the dataset (more good loans than bad loans).

3. **Addressing Imbalance:** The Synthetic Minority Over-sampling Technique (SMOTE) was employed to address the class imbalance. This significantly improved recall from 44% to 71% and provided probabilities for both good (Target = 0) and bad (Target = 1) loans.

4. **Decile Analysis:** Loan applications were sorted in ascending order based on the probability of being a good loan (Target = 0). This facilitated a profit-focused analysis. The profit for each decile was calculated based on the assumptions:
    * Profit from a good loan: $100
    * Loss from a bad loan: $500

5. **Profit-Driven Recommendations:**  Two final recommendations were derived from the decile analysis:

    * **Profitability Focused:** Approve loan applications if the probability of a good loan is greater than 87.30%. This strategy maximizes profit but results in a lower market share (77.51%).

    * **Profitability & Expansion Focused:** Approve loan applications if the probability of a good loan is greater than 81.50%. This strategy accepts a slightly lower profit margin to gain a larger market share of good loans (86.75%).

## Summary

This project successfully built a model for subprime mortgage lending decisions. It effectively addressed the challenges posed by imbalanced data using SMOTE and optimized for profit through decile analysis. The final recommendations offer a trade-off between maximizing profit and expanding market share, enabling the business to select the strategy that best aligns with its objectives.  The project effectively quantifies the impact of different lending thresholds on both profitability and market penetration.
