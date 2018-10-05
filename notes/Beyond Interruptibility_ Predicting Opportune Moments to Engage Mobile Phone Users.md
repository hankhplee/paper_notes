# Beyond Interruptibility: Predicting Opportune Moments to Engage Mobile Phone Users

## Method
1. 4 week with 337 participants
2. 3367 cases participants engaged with the provided content
3. ESM
    - create 10~15 notification per day, 30689 responses in total
    - time treshhold: 10 min

## Model
1. targeted varible
    - 1: when the user opened the questionnaire and engaged with one of the two suggested contents by clicking on it
    - 0: when the user either did not open the questionnaire or opened it but ignored the suggested content
2. feature
    - three different time windows
        - current moment (e.g., current screen status or number of unlocks in the last 5 minutes)
        - recent (e.g., fraction of time screen was on in the last hour)
        - current day (e.g., fraction of time screen was on since 5 am today)
    - feature extraction
        - communication activity 
        - context
        - demographics
        - phone status
        - usage patterns
- Model choice
    - ***XGBoost***
    - logistic regression
    - random forests

3. result
without past actions: 
![](https://i.imgur.com/H7vx4Uf.png)
with past actions: 
![](https://i.imgur.com/pdoT04e.png)

![](https://i.imgur.com/BYI7c7D.png)


## Limitation
1. unanswered ESM infer inopportune moment