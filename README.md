# credit_score_python
hi
This project aimed to build a model for making lending decisions on subprime mortgages, balancing profit and market share.  The data consisted of 30 variables (including bankruptcy indicators, public derogatories, financial inquiries, and trade lines) and 3000 rows.

Methodology:

Data Cleaning and Standardization: Python was used for this step, preparing the data for modeling.
Model Building: A Logistic Regression Classifier was initially trained (80% train, 20% test split). While the model achieved high accuracy, it suffered from low recall due to the imbalanced nature of the dataset (more good loans than bad loans).
Addressing Imbalance: The Synthetic Minority Over-sampling Technique (SMOTE) was employed to address the class imbalance, significantly improving recall from 44% to 71%. This provided probabilities for both good (0) and bad (1) loans.
Decile Analysis: Loan applications were sorted by the probability of being a good loan (Target = 0) in ascending order. This allowed for a profit-focused analysis. The profit for each decile was calculated based on the assumed profit of $100 for a good loan and a loss of $500 for a bad loan.
Profit-Driven Recommendations: Two final recommendations were made based on the decile analysis:
Profitability Focused: Approve loans if the probability of a good loan is greater than 87.30%. This strategy maximizes profit but results in a lower market share (77.51%).
Profitability & Expansion Focused: Approve loans if the probability of a good loan is greater than 81.50%. This strategy accepts a slightly lower profit margin to gain a larger market share of good loans (86.75%).

Summary:

The project successfully built a model for subprime mortgage lending decisions.  It addressed the challenges of imbalanced data and optimized for profit by using SMOTE and decile analysis.  The final recommendations provide a trade-off between maximizing profit and expanding market share, allowing the business to choose the strategy that best aligns with its goals.  The project effectively quantifies the impact of different lending thresholds on both profitability and market penetration.





