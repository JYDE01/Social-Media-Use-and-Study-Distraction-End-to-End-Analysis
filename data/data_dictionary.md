# Data dictionary

File: `cleaned_survey_data.xlsx` (98 rows, 12 columns). One row per respondent.

| Column | Original survey question | Type | Values |
|---|---|---|---|
| What is your age | What is your age | Category | 18 - 20, 21 - 23, 24 and Above |
| Institution/MSA | Institution/MSA | Category | 13 institutions, for example Bayelsa Medical University, University of Ilorin, Benson Idahosa University |
| What is your current academic level? | What is your current academic level? | Category | Preclinicals (200 to 300L), Clinicals (400L and above) |
| What phone do you use? | What phone do you use? | Category | Android, Iphone, Samsung |
| Daily hours | How many hours per day do you spend on social media platforms (weekdays and weekends combined)? | Ordered category | Less than 2 hours, 2 to 3 hours, 4 to 5 hours, More than 5 hours |
| Time of day | Which time of day do you spend the most time scrolling or messaging? | Category | Morning, Afternoon, Evening, Before going to bed, Midnight |
| Primary purpose | What is your primary purpose for using social media on a daily basis? | Category | Entertainment / Videos / Reels, Socializing / Chatting with friends, Academic discussions & Study groups, News, Current Affairs & Trends |
| Phone location | Where is your phone when you study? | Category | Beside you, In your bag, Others |
| Q1 Notifications | I lose focus during study sessions because I check social media notifications | Ordered category | Never, Rarely, Sometimes, Often, Always |
| Q2 Scrolling | I spend more time scrolling on social media than intended when I am supposed to be studying | Ordered category | Never, Rarely, Sometimes, Often, Always |
| Q3 Delaying | Social media distraction causes me to delay completing academic assignments or reading notes | Ordered category | Never, Rarely, Sometimes, Often, Always |
| Q4 Concentration | I find it difficult to maintain concentration on lecture materials without checking my phone | Ordered category | Never, Rarely, Sometimes, Often, Always |

## Derived fields (calculated in Power BI)

| Field | Definition |
|---|---|
| Score (Q1 to Q4) | Never = 1, Rarely = 2, Sometimes = 3, Often = 4, Always = 5 |
| Distraction Index | Average of the four scores, from 1 (never distracted) to 5 (always distracted) |
| High distraction | Distraction Index of 3.5 or above |
