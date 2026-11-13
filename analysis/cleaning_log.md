# Cleaning log

The data was cleaned in Power Query. This log compares the raw survey export (17 columns, 100 rows) with the cleaned dataset (12 columns, 98 rows).

| # | Step | Raw data | Cleaned data |
|---|---|---|---|
| 1 | Remove blank submissions | 2 rows with a timestamp but no answers (a test entry on 26 Oct and an empty submission on 3 Nov) | Removed. 98 rows remain. |
| 2 | Remove columns not needed for analysis | Timestamp, "Are you above 18?", "Are you currently an undergraduate MBBS student?", consent question, Email | Removed. 12 columns remain. Emails are not published. |
| 3 | Group age | Free text: 18 to 30, "20 years", "22 years old", "20years old", "21+", "00", "Unknown", blank | 18 - 20 (42), 21 - 23 (53), 24 and Above (3). Ten responses with a missing or invalid age are included in 21 - 23. |
| 4 | Standardise institutions | 28 spellings and acronyms, such as BAMUMSA, Bamusa, Bmu, ILUMSA, Unilorin, BIUMSA | 13 institution names. One acronym (KOMUMSA) was kept as written. |
| 5 | Group academic level | Numeric: 200, 300, 400, 500, 600 | Preclinicals = 200 to 300L (22). Clinicals = 400L and above (76). |
| 6 | Group phone type | Tecno 13, Redmi 19, Itel 5, Oppo 2, Android 4, "Amdriod" 1, Others 9, Iphone 27, Samsung 18 | Android 53 (all brands above, including Others), Iphone 27, Samsung 18 |
| 7 | Label distraction answers | Numbers 1 to 5 in four columns | Never, Rarely, Sometimes, Often, Always |
| 8 | Left unchanged | Daily hours, time of day, primary purpose, phone location | No changes needed |

## Notes on the cleaning

- **Age:** respondents with a missing or invalid age were placed in the 21 - 23 group, which is why that group has 53 students against 43 with a valid age in the band.
- **Phones:** "Others" was assumed to be Android. Samsung is an Android brand but is kept separate, so use the phone-type breakdown with caution.
- **Screening questions:** the over-18, MBBS and consent columns were removed after the blank rows were dropped.
