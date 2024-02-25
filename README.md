### Credit Card Fraud Detection (Summarized)
![Credit Card Fraud detection](https://github.com/md-sadik-hossen/Credit-Card-Fraud-Detection/blob/main/images_ccfd/frauddetection.jpg)
### Objectives
In this project, the aim is to utilize machine learning models to predict occurrences of fraudulent credit card transactions.<br>
**1. Detecting Fraudulent Transactions**<br>
The main goal is to classify transactions accurately as either authentic or fraudulent. Utilizing data encompassing transaction time, amount, and transformed features V1 to V28, various classification models are employed. To achieve this, we'll test and compare different model-building techniques, evaluating their performance through various metrics.<br>
**2. Exploring Transaction Patterns** <br>
(i). Consecutive Frauds: Do fraudsters tend to strike multiple times in a short period?  By analyzing transaction sequences, we can uncover potential patterns of follow-up scams and strengthen our defenses. <br>
(ii). Amount Matters: Are fraudulent transactions typically larger than legitimate ones? We'll compare the typical amounts of authentic and fraudulent transactions, seeking any significant differences that might raise red flags.<br>
(iii). Fraudulent Peak Periods: Do fraud rates climb during specific times of day or days of the week? Can we identify peak transaction periods with a higher risk of fraudulent activity?<br>
(iv). Fraud in High-Volume Times: When overall transaction volume spikes, does the number of fraudulent transactions proportionally increase, is it simply due to an overall increase in transactions, or are there other hidden factors at play?<br>
(v). High-Fraud Time Points: Why do certain moments stand out for unusually high fraud rates? Is it purely due to a high volume of transactions, or could other factors be influencing this surge?
<br>
### Problem Statement
**Security Awareness:** Many banks is retaining high-profit customers, but banking fraud poses a substantial threat, leading to financial losses and eroding trust. A bank informs users of an expiring card and requests verification. Users should avoid sharing sensitive details as fraud cases in digital transactions are on the rise.<br>
**Growing Digital Transactions:** Despite a 51% growth in digital transactions, concerns persist due to a substantial increase in fraudulent activities, with 52,304 cases reported in FY 2019.
While making online purchases, regularly monitor account statements for any suspicious transactions and report them to the bank immediately.<br>
**Manual System:** Slow, clunky manual reviews choke banks' efficiency, leading to costly chargebacks, frustrated customers, and missed legitimate transactions. This reactive approach leaves everyone vulnerable.

### Credit Card Fraud and Its Impact:
**Financial Protection:**  With an increasing need to detect fraudulent transactions, machine learning models play a crucial role. Understanding model selection, tuning, and handling class imbalances are essential skills for data scientists.
Banks can utilize machine learning algorithms to analyze transaction patterns, flag unusual activities and prevent potential fraud. Protect profits, safeguard customers, and thrive in the age of digital payments.<br>
**Preserving Trust:** Detection models play a crucial role in preserving trust between customers and banks. By promptly identifying and addressing fraudulent activities, banks demonstrate their commitment to security, ensuring customers feel secure in their financial transactions.<br>
**Operational Efficiency:** Implementing a robust fraud detection model enhances operational efficiency by automating the identification process. For example, a machine learning model can analyze vast datasets more rapidly than manual reviews, minimizing the time and resources required to detect fraudulent transactions.<br>
**Regulatory Compliance:** Financial institutions must comply with regulations and standards to ensure a secure and trustworthy banking environment. A credit card fraud detection model helps banks adhere to these requirements, avoiding legal issues and reputational damage. For instance, if a bank fails to detect and prevent fraudulent activities, it may face regulatory penalties and lose customer trust.

### Common Method of Credit Card Fraud:
Magnetic Mimicry: Skimming steals card data for shady swaps.<br>
Counterfeit Cabal: Fake cards join the plastic party, uninvited.<br>
Lost & Found Lies: Stolen cards fuel fraudulent feasts.<br>
Telephonic Trickery: Sweet-talking scammers swipe cash by extracting information.<br>
Others: Tampered cards & Identity theft play a deceitful game.

### Steps of this Project:
**1.**	Perform Exploratory Data Analysis (EDA) for an initial overview of the dataset, focusing on feature distribution, class imbalances, and overall data characteristics. <br>
**2.**	Conduct Data Preprocessing, addressing missing values, and applying normalization or standardization to prepare data for model training.<br>
**3.**	Train various fraud detection models, including XGB Classifier, Light GBM Classifier, Gradient Boosting Classifier, Ada Boost Classifier, Random Forest Classifier, Logistic Regression, Support Vector Machine (SVM), Decision Tree Classifier, Hist Gradient Boosting Classifier.<br>
**4.**	Evaluate model performance using metrics such as AUC-ROC, precision, recall, F1-Score, and visualizations like ROC curves and confusion matrices.<br>
**5.**	Select the most suitable model for credit card fraud detection based on comprehensive evaluation metrics.

### Distribution of Time for Normal & Fraudulent Transactions

![Time for Normal & Fraudulent Transactions](https://github.com/md-sadik-hossen/Credit-Card-Fraud-Detection/blob/main/images_ccfd/1.01%20Distribution%20of%20Time%20for%20normal%20and%20Fraudulent%20Transactions.png)

**This complete transaction occurs over two days.**
Most of the fraudulent transactions appear to have occurred between the time intervals of 9 hours to 28 hours after a certain event, with another cluster observed between 36 hours and 46 hours thereafter. <br>
These time frames suggest potential patterns or anomalies in the timing of fraudulent activities, which could be further investigated for insights into the nature of the fraudulent behavior or to enhance fraud detection algorithms.

### Distribution of Numerical Attributes

![Credit Card Fraud detection](https://github.com/md-sadik-hossen/Credit-Card-Fraud-Detection/blob/main/images_ccfd/1.2%20Distribution%20of%20numerical%20attributes.png)

Many variables exhibit outliers, as evidenced by the presence of skewness in the data distribution. To address this issue, we filter the DataFrame based on outlier detection techniques, such as the interquartile range (IQR) method or z-score method, to remove or mitigate the impact of outliers on the analysis and modeling process.


### Comparison of Models Using Original Data Scaling

![Credit Card Fraud detection](https://github.com/md-sadik-hossen/Credit-Card-Fraud-Detection/blob/main/images_ccfd/1.3%20Comparison%20of%20models%20with%20scale%20in%20Orjinal%20Data.JPG)
#### Top 2 model based on Recall score, F1 score and Precision score: XGB Classifier, Random Forest Classifier.<br>
The comparative analysis reveals that XGB Classifier and Random Forest Classifier outperform other models in terms of accuracy, recall, F1 score, and precision, showcasing robust performance on both test and train data. Conversely, Ada Boost Classifier, SVM, Logistic Regression, and Decision Tree Classifier exhibit slightly lower recall and F1 scores, indicating potential issues with correctly identifying positive cases. Hist Gradient Boosting Classifier, Light GBM Classifier, and Gradient Boosting Classifier demonstrate suboptimal performance, especially in recall and precision, suggesting the need for further optimization or exploration of alternative models. To enhance overall model performance, focusing on hyperparameter tuning for boosting algorithms like XGB and Random Forest, and considering ensemble techniques could be beneficial. Additionally, addressing class imbalance and exploring feature engineering may improve the performance of models with lower recall and precision.

### Comparison of Models Using df_filter Data Scaling

![Credit Card Fraud detection](https://github.com/md-sadik-hossen/Credit-Card-Fraud-Detection/blob/main/images_ccfd/1.4%20%20Comparison%20of%20the%20models%20with%20scaling%20in%20df_filter.JPG)

#### Top 2 model based on Recall score, F1 score and Precision score: XGB Classifier, Random Forest Classifier.<br>
These results depict enhanced performance across various classifiers compared to the previous outcomes. Notably, Random Forest, AdaBoost, and Gradient Boosting classifiers exhibit improved accuracy, recall, F1, and precision scores, suggesting better fraud detection capabilities. <br>
Conversely, while SVM and Logistic Regression maintain high accuracy, their recall, F1, and precision scores demonstrate slight declines, implying potential challenges in correctly identifying fraudulent transactions. The decision to employ Random Forest, AdaBoost, or Gradient Boosting classifiers could be advantageous for accurate fraud detection, considering their balanced performance metrics.

### Comparison of Models with Scaling in df_filter with Smote and Scale

![Credit Card Fraud detection](https://github.com/md-sadik-hossen/Credit-Card-Fraud-Detection/blob/main/images_ccfd/1.5%20Comparison%20of%20the%20models%20with%20scaling%20in%20df_filter%20with%20Smote%20and%20Scale.JPG)

#### Top 2 model based on Recall score, F1 score and Precision score: XGB Classifier, Random Forest Classifier. <br>
SMOTE adjustments in model performance show consistent or slightly improved accuracy, recall, precision, and F1 scores across most classifiers compared to the previous results. Specifically, classifiers like Hist Gradient Boosting, XGB, Light GBM, and Random Forest demonstrate robust performance with high scores across all metrics, indicating their effectiveness in accurately detecting fraudulent transactions. <br>
However, classifiers like Gradient Boosting, Ada Boost, and SVM exhibit slightly lower scores but still maintain reasonable performance levels. Notably, Logistic Regression shows a decline in performance compared to the previous results, suggesting potential areas for further optimization or exploration of alternative methods.

### Comparison of the Models with Scaling in df_filter Using ADASYN

![Credit Card Fraud detection](https://github.com/md-sadik-hossen/Credit-Card-Fraud-Detection/blob/main/images_ccfd/1.6%20Comparison%20of%20the%20models%20with%20scaling%20in%20df_filter%20using%20ADASYN.JPG)

#### Top 2 model based on Recall score, F1 score and Precision score: XGB Classifier, Random Forest Classifier. <br>
ADASYN showcases marginal to moderate shifts in model performance metrics compared to the previous iteration. Models like Hist Gradient Boosting, Light GBM, XGB, and RandomForest retain their high accuracy and recall scores, indicating consistent fraud detection capabilities. <br>
Notably, SVM demonstrates a slight decrease in accuracy and recall, suggesting potential areas for optimization or alternative model selection. Similarly, Logistic Regression exhibits a noticeable decline in all metrics, highlighting the need for revisiting feature engineering or considering more sophisticated algorithms. 

### Summary & Conclusion:
- **ML Models:** XGB Classifier, Random Forest Classifier, SVC, Decision Tree Classifier, Light GBM Classifier, Gradient Boosting Classifier, Ada Boost Classifier, Logistic Regression, Hist Gradient Boosting Classifier.
- **Oversampling Techniques:** SMOTE, ADASYN.
- **Scalers & Transforms:** RobustScaler, PowerTransformer.
- Using a threshold of 0.5 and SMOTE, XGB and Random Forest classifier models stand out as the top performers (ROC-AUC scores of approximately 99.99%, recall and F1-score 100%), showcasing outstanding predictive accuracy and robustness.
