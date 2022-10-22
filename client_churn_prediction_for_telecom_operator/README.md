# Prediction of client churn of the telecom operator "Interconnect"
## Goal
The telecom operator "Interconnect" wants to learn how to predict their client churn. 
If it turns out that the user is going to leave, they will be offered promotional codes and special conditions.
## Data
The data consists of the following files obtained from various sources:
- `contract.csv` — contains the following information about contracts with clients:
  -  `customerID` - client's identification number,
  -  `BeginDate` – service start date,
  -  `EndDate` – service end date,
  -  `Type` – payment type: monthly, yearly, etc.,
  -  `PaperlessBilling` – electronic billing,
  -  `PaymentMethod` – payment method,
  -  `MonthlyCharges` – monthly charges,
  -  `TotalCharges` – total amount of money spent on services for the entire time.
- `personal.csv` —  contains the following personal information about the clients:
  - `customerID` - client's identification number,
  - `gender` – client's gender,
  - `SeniorCitizen` – retirement status,
  - `Partner` – having a spouse,
  - `Dependents` – having dependents.
- `internet.csv` — contains the following information about internet services:
  - `customerID` - client's identification number,
  - `InternetService` – Internet. The connection can be of two types: via a telephone line (DSL, digital subscriber line) or through a fiber optic cable,
  - `OnlineSecurity` – a malicious website blocker,
  - `OnlineBackup` – a cloud file storage for data backup,
  - `DeviceProtection` – an antivirus software,
  - `TechSupport` – a dedicated technical support line,
  - `StreamingTV` – TV streaming services,
  - `StreamingMovies` – a movie directory.
- `phone.csv` — contains the following information about landline communication services:
  - `customerID` - client's identification number,
  - `MultipleLines` – the possibility to connect to several lines simultaneously during a call.
## Libraries used
CatBoost, Matplotlib, NumPy, pandas, Phi_K, re, Seaborn,  scikit-learn, time
## Conclusion
We examined the provided data, performed some transformations and procedures (converted the headers and data types, replaced missing values, merged all tables into a single dataframe, added additional features, explored a portrait of departed clients, looked at the Spearman's and phi-k's correlation matrix, splitted datasets into train and test samples, built, searched hyperparameters using HalvingGridSearchCV with cross-validation and trained 2 models - CatBoost and Random Forest classifiers).

As a result, we got that all models showed good quality in cross-validation (threshold: ROC AUC is greater than 0.85).
<img width="1245" alt="results_image" src="https://user-images.githubusercontent.com/94500188/197359683-b965f8c5-9116-44fb-a30f-784594801cc2.png">
<br>The best quality in cross-validation was shown by the CatBoost model trained on the dataset AFTER deleting the features with the following hyperparameters {'depth': 6, 'iterations': 500, 'learning_rate': 0.04}, - ROC AUC of this model was 0.894. 
<br>We checked the quality of the best model on our test sample, - the model proved to be reliable - ROC AUC was 0.879.

Thus, the chosen model predicts the client churn quite well. Therefore, the telecom operator "Interconnect" can use this model on current data - if it turns out that the user plans to leave, they need to offer promotional codes or some special offers, which can help retain clients.
