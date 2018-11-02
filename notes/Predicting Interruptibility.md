# [Predicting Interruptibility for Manual Data Collection: A Cluster-Based User Model ( Visuri et al. MobileHCI '17)](https://people.eng.unimelb.edu.au/vkostakos/files/papers/mobilehci17.pdf)

Provide two contribution in Quantified-Self applications to reduce data logging burden: 
1. alert dialog
2. using user cluster to predict users' mobile interaction

## Background and Motivation
1. Manual Data Collection: 
    - Generate user-driven insight (both for research and system)
2. Issue in Manual Data Collection:
    - contunuous tracking lead to burden
    - decrease engagement overtime
    - extra interruption
3. Solutions
    - predict mobile interaction, and transform brief smart phone usages into data contribition (e.g. killing time) 

## Methods
1. opportune moment for data contribution: situ in which the user is not actively performing a task:
    - [Btown et al](https://dl.acm.org/citation.cfm?id=2628377)
        - Occasioning use (e.g. IM notification)
        - Filling time (using mobile phone)
        - Micro-breaks (users self interrupt their main task)
2. Altert Dialogs
    - quick to interact
    - easy to dismiss
![](https://i.imgur.com/o6sTBSt.png)

3. Opportune Interruption using alert dialogs
![](https://i.imgur.com/yTnHJ1j.png)

4. LifeTracker
![](https://i.imgur.com/eNL0ayb.png)

5. Features and Target
    - dismiss vs accept
    - data contribution
![](https://i.imgur.com/rQAgPgA.png)

6. exp setup
    - Four week field study
        - 48 participants
        - 36 males, 12 females
        - age: 21~53
        - Android 5.0+
        - 3 Euros/ day for 4 week
    - open-ended post-study survey
        - experience with the application
        - “What influenced your decision to answer or reject a dialog?”

## Result
1. 19287 dialogs, 15,434 (80.0%) were accepted, 3658 (19.0%) were dismissed, and 195 (1.0%) resulted in an application launch.

![](https://i.imgur.com/QTEYfIt.png)

2. Select RF as best practice
![](https://i.imgur.com/1ElH8Zm.png)

3. Predicting individual users'(who predviously unknown) interaction: Proposed User Cluster Classification
![](https://i.imgur.com/Jb7kSTg.png)'
    - cluster based on 40 dimensions, using k means clustering algo
        - demographic information (age, sex)
        - pre-study survey
            - Q1) “Do you often read the arriving notifications immediately?”, on a 4-point scale (Never, Sometimes, Usually, Always).
            - Q2) “What kind of applications (categories) do you use on your personal smartphone?”, according to a selection from Play Store categories, including the “Other” category, which allows the user to be more specific using free text.
            - Q3) “Would you describe your smartphone use as active (frequent short periods of time), passive (only check when you are prompted by e.g. a notification), or mixed?”
            - Q4) “Would you describe yourself as a technology enthusiast?”, on a 4-point scale (Definitely not, Not really, Somewhat, Definitely).
        - user’s device usage patterns (usage frequency during different hours of day)
    - best in k = 7

4. ![](https://i.imgur.com/vFZkduh.png)

## Findings
1. Clusters
    - **Cluster 1: Casual Users** (10 users)
        - the most passive device usage style
        - low tech enthusiasm
        - slowest response rate to notifications
    - **Cluster 2: Social Chatterers** (7)
        - frequent usage of communication apps
        - Smartphone usage is balanced over the duration of the day (9am to 8pm)
        - quickly respond to notifications
        - consider themselves tech enthusiasts
    - **Cluster 4: Night Owls** (7)
        - most likely to use their smartphones between 10pm and 8am
        - users in this group are likely to use communication applications with low versatility in application usage
    - **Cluster 5: Work On-the-go** (8)
        - respond to interruptions quickly
        - report using e.g. finance applications frequently
        - daily rhythm that does not involve smartphone usage after 10pm

2. 
![](https://i.imgur.com/uQBqt67.png)
- among diff cluster:  
    - network type and hour (“Casual Users”, Cluster 1)
    - Wi-Fi and internet availability (“Night Owls”, Cluster 2)
    - session duration (“Work On-the-go”, Cluster 5)
- Diff from General model
    - physical acitvity +
    - proximity + 
    - session type (new or continuing session) -

3. Post-study survey
- time when dismiss the dialog
    - more important priority task being performed on the smartphone
    - physical activity
    - time of the day
    - surrounding physical context
    - bad mood
- accept the dialog
    - brief interactions (*“If the question was just a button to select one option I mostly answered them because it was nearly as quick as rejecting a dialog.”*)
    - lack of anything better to do

## Discussion
1. Personalized model vs General model
    - General models have poor fit for individual users with specific usage and behavior traits
    - Personalised models requires significant amount of collected training data
2. Features matter differently in different cluster
    - Casual User:
        - hour
    - Work on the go: 
        - session duration (within communication in 45 seconds)
    - Night Owls:
        - Wifi, internet availibility
3. Personalized model more effectively
    - less data needed

## Limitation
1. The research app is not merely designed to collect data
    - other reasons for the user not to contribute the data
    - quality of the data
2. Alert Dialog may be itself too intrusive 

### Insight for me
1. Thoughtful in considering the interrupting nature (not derectly derived the interactions as non-distrupting)
2. Post study survey could emphasize more on when and how the prediction may not be good.