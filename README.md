# ACCT420 (Forecasting and Forensic Analytics)

This repository contains my __project__ for SMU module ACCT420 (Forecasting & Forensic Analytics).

# Project description
This project aims to model accounting manipulation or fraud in __banks__.

                                              ![image](https://github.com/user-attachments/assets/2e0bbe0a-426a-4ec7-b8c8-096163e98cec)

In this project, we work with transparently.AI, a company that provides AI-enabled accounting manipulation and fraud prediction. The problem at hand is that 40% of companies manipulate their accounts, and more than $1 trillion USD per year is lost to owners, investors, suppliers and customers due to accounting manipulation and fraud. Hence, the need for a model that could predict manipulation and fraud before it even happens.

## Methodology
Part 1 - Taxonomy research (understanding the use-case)

In this part, we look into cases of bank failures and the types of accounting manipulation/fraud that has led to these failures (eg. Lehman Brothers in 2008). Then, we compile the common features across these cases. Lastly, with the help of these common features, we come up with a list of variables that would help in modelling manipulation/fraud in banks.

Part 2 -  Modelling

Our workflow is as follows:
1. Exploratory Data Analysis
2. Data Preparation
3. Model selection (*Logistic regression, LASSO, XGBoost*)
4. Conclusions

We took insipiration (totally did not copy and paste 🤭) from the Journal of Accounting Research: "Detecting Accounting Fraud in Publicly Traded US Firms Using a Machine Learning Approach" (Bao et al., 2015) to decide on our X variables by using the same raw accounting line variables as the research. We then added financial ratios based on our domain knowledge and taxonomy research. Lastly, text analysis using *Latent Dirichlet allocation (LDA)* highlighted that auditors are also important when it comes to misstatements/fraud, hence we added 2 variables as a proxy for auditor. The Y variable is AAER, which takes 1 or 0. If 1, then there's higher likelihood of fraud, 0 otherwise. *An AAER (Accounting and Auditing Enforcement Release) is a document issued by the SEC detailing enforcement actions against violations of accounting and auditing standards*.

![image](https://github.com/Rayybird96/ACCT420_Forecasting_and_Forensic_Analytics/assets/138758608/3254c06f-a5c2-41ee-bb8f-aac38a837359)

We then perform data cleaning, feature engineering and model building using 3 classification model techniques. __Our conclusion is that *XGBoost* has the best model performance (everyone, act surprised!!!!🙄)__. Additionally, the important variables across all models are those related to long-term debt and preferred stock, hence there is scope for further research on these variables and how they potentially lead to accounting mistatements.

![image](https://github.com/Rayybird96/ACCT420_Forecasting_and_Forensic_Analytics/assets/138758608/5c6950c1-095b-49e7-b936-7909d7754f45)

While this is just a brief summary of our project, our data engineering and discovery processes were also extensive. Please refer to my R files to check out our full story!



