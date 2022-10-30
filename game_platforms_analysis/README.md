# Determination of patterns that form the success of the game
## Goal
In order to plan advertising campaigns online store "Ice" wants to know patterns that determine whether a game succeeds or not. 
<br>**The purpose of the study** is to create a user profile for each region and test two statistical hypotheses:
1. Average user ratings of the `Xbox One` and `PC` platforms are the same;
2. Average user ratings for the `Action` and `Sports` genres are different.
## Data
The historical data on game sales (until 2016) contains the following information:
- `Name` — game name
- `Platform` — game platform name
- `Year_of_Release` — game year of release
- `Genre` — game genre
- `NA_sales` — North American sales (millions of copies sold)
- `EU_sales` — sales in Europe (millions of copies sold)
- `JP_sales` — sales in Japan (millions of copies sold)
- `Other_sales` — sales in other countries (millions of copies sold)
- `Critic_Score` — critics' score (maximum of 100)
- `User_Score` — users' score (maximum of 10)
- `Rating` — ESRB rating
## Libraries used
Matplotlib, NumPy, pandas, SciPy, Seaborn
## Conclusion
Since game industry is changing really fast, we decided to use the 3-year period from 2014 to 2016 inclusive as the actual period for the analysis.
<br>We identified, that users' ratings have no correlation with sales, and critics' ratings have poor correlation with sales over the actual period.

We also analyzed the users' behavior for each region for the actual period and noticed, that the profile of a user from North America 
is largely the same as that of a user from Europe, but differs significantly from users from Japan.
<br>Potentially popular (and profitable) in 2017 will be games on `PS4` and `XOne` platforms, that are `Action` or `Shooter` genre and rated `M` by ESRB
(for North America and Europe) or `Role-Playing` genre and rated `T` by ESRB (for Japan).

We also tested two statistical hypotheses and statistically confirmed that:
1. average user ratings of the `Xbox One` and `PC` platforms are the same over the actual period.
2. average user ratings of the `Action` and `Sports` genres differ in the actual period.
