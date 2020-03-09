# Predicting_Health_Insurance_Fraud

Each year, health insurance fraud costs public and private companies between $30-$70 billion. Healthcare provider fraud is one of the most important kinds of fraud. Medicare and Medicaid recently started releasing the yearly data related to all the providers' claims. Office of Inspector General releases a monthly list of providers who are convicted of abuse and/or fraud. Predictive analysis using machine learning algorithms is performed on these two datasets to find the patterns in the provider's behavior to detect the fraud.
After cleaning the datasets by removing missing values, dimensionality reduction is performed to retain only the relevant features. Features kept have the information about the unique identifier for each provider, their gender, type of the service, number of services for which reimbursement is claimed and total amount allowed for each service. 
Fraud and non-fraud labels are created by joining the dataset for services and convicted provider's dataset. 
Column transformation pipeline is applied to convert selected categorical features into numerical using OneHotEncoder. 
Three classification models are trained: logistic regression (LR), random forest (RF), and gradient boosted trees (GBT). 
The performance of the models is evaluated using ROC, AUC, ANOVA, and post hoc using Tukey (HSD).
GBT outperforms both LR and RF with an AUC score of about 84%.
The final trained model can be used on a similarly large dataset, containing claims by the service providers, to predict whether their behavior is fraudulent or not. The results should be taken with a grain of salt, as the model focuses on high recall as compared to precision to increase the likelihood of catching a fraudster.
