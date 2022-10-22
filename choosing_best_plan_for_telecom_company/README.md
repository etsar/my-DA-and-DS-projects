# Determination of a profitable plan for the telecom company "Megaline"
## Goal
The commercial department of the telecom operator "Megaline" wants to know which of the two prepaid plans brings in more revenue in order to adjust the advertising budget.
<br>**The purpose of the study** is to test two statistical hypotheses:
1. The average revenue from users of the `ultra` and `smart` plans differs;
2. The average revenue from users in Moscow area is different from that of the users from other regions.
## Data
The data consists of the following files:
- `calls.csv` - contains the following information about calls:
  - `id` — unique call identifier,
  - `call_date` — call date,
  - `duration` — call duration (in minutes),
  - `user_id` — identifier of the user making the call.
- `internet.csv` - contains the following information about web sessions:
  - `id` — unique session identifier,
  - `mb_used` — the amount of data spent during the session (in megabytes),
  - `session_date` — web session date,
  - `user_id` — user identifier.
- `messages.csv` - contains the following information about text messages:
  - `id` — unique text message identifier,
  - `message_date` — text message date,
  - `user_id` — the identifier of the user sending the text.
- `tariffs.csv` - contains the following information about prepaid plans:
  - `tariff_name` — plan name,
  - `rub_monthly_fee` — monthly charge in rubles,
  - `minutes_included` — monthly minute allowance,
  - `messages_included` — monthly text allowance,
  - `mb_per_month_included` — data amount allowance (in megabytes),
  - `rub_per_minute` — price per minute after exceeding the package limits,
  - `rub_per_message` — price per text after exceeding the package limits,
  - `rub_per_gb` — price per extra gigabyte of data after exceeding the package limits.
## Libraries used
Matplotlib, NumPy, pandas, SciPy
## Conclusion
We analyzed the clients' behavior and tested two statistical hypotheses. As a result, we statistically confirmed that:
1. the average revenue from users of the two plans differs, and 
2. the average revenue from Moscow users is equal to the average revenue from other regions users.

It is expedient for Megaline's commercial department to attract more users of the `ultra` plan, since it is more profitable for the company in terms of obtaining guaranteed revenue (i.e., monthly fee).
<br>An advertising campaign to attract new `ultra` users should be carried out for all regions.
