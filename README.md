# Fraud-transactions-Data-Analysis

This presentation is going to be divided by the following structure:
1. Presentation
2. Data Validation and Methodology
3. Conclusions and Insights
4. Recommendations


# 1- Presentation:
In this presentation, we are going to analyze a synthetic dataset mirroring mobile money transactions. This dataset encapsulates a month's worth of diverse transaction types, providing a snapshot of financial activities. Our focal point is to uncover patterns within flagged transactions. The primary objective is to provide compliance managers with concise insights to fortify their anti-fraud strategies and enhance overall fraud detection measures.

# 2- Data Validation and Methodology:
I chose Python for the analysis of the dataset in combination with Jupyter Notebook. My choice was based on the versatility of Python for the analysis and manipulation of large amounts of data, along with the visualization capacity of Jupyter. As part of the data cleaning process, I checked for missing values and duplicates, and none were found, suggesting that the dataset had likely been cleaned up beforehand.
Inside the code, there are also comments of what I'm doing, and why I am doing it.

# 3 - Conclusions and Insights:

● The fraudulent transactions types are Transfer and Cash out.
● There are a total of 8,213 fraudulent transactions, constituting 0.12908% of the total
transactions.
● The mean transaction amount for non-fraudulent transactions is €178.20K. In
contrast, the mean transaction amount for fraudulent transactions is €1.47M, nearly 8 times higher. This significant difference suggests the potential for implementing additional verification steps for transactions exceeding €1M.
● The fraud flag only correctly identified 0.19% of the actual fraudulent transactions. This low accuracy raises concerns about its reliability and suggests the need for an improved detection mechanism.
● 28 accounts have been involved in both fraudulent and non-fraudulent transactions. Notably, 10 accounts made a non-fraudulent transaction after a fraudulent one, totaling €1.56M. This poses a high risk, and prompt account blocking is recommended once a fraudulent transaction is detected.
● No user has engaged in more than one fraudulent transaction.
● Fraudulent transactions are slightly more common on Wednesdays.
● There is no evidence indicating that fraudulent transactions occur at specific hours.
 
# 4- Recommendations:
 The actual fraud flag must be reviewed and improved, or we can face potential loss of huge amounts of money and facilitate money laundering.
As the fraudulent flag doesn't work as we need, I developed a machine learning model to predict this type of transaction.
The result of the test conducted on the model reveals an average precision score of 90%. This notable improvement in comparison to the actual fraud flag rate of 0.19% signifies enhanced accuracy and reliability in predicting fraudulent transactions. The model demonstrates a substantial capability in identifying potential fraud cases with increased precision.
Note that this model has been constructed using the information available in the dataset. Incorporating details such as the account creation date, transaction volume associated with each account, currency information, user behavior, and a history of transactions flagged as suspicious would provide a more comprehensive foundation for robust and accurate fraud detection in practical scenarios.
