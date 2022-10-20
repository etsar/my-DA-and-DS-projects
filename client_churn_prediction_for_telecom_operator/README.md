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
