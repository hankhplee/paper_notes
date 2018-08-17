# My Phone and Me: Understanding People’s Receptivity to Mobile Notification
The works believe that interruptibility management systems fail to achieve a very high accuracy in predicting the opportune moment because there is still a lack ofunderstanding concerning the factors influencing the user’s receptivity to mobile notifications in different physical and cognitive situations.

1) personality traits influence the time people attend the notification, and how distruptive the noti percieved.
2) disruption from noti perceived varies with its senders
3) ongoing task type is associated with the perceived disruption.

## key points and findings
1. Key Contribution: 
    * The impact of a **notification’s alert modality** on the **user’s ability to perceive a notification** alert;

    * The impact of the **alert modality, sender-recipient relationship, presentation of a notification, the ongoing task type, completion level** and **task complexity** on the **response time**.

    * The impact of the **sender-recipient relationship**, and the **ongoing task’s type, completion level and complexity** on the **perceived disruption**.

    * The role of the **sender-recipient relationship, notification content** and the **perceived disruption** on the **user’s decision to accept or dismiss a notification**;

    * The impact of the **user’s personality** on the **perceived disruption and response time to a notification**.

2. Users tend to click highly disruptive notifications if they contain valuable information.
3. The **alert modality** has a significant impact on the **time taken by the users to view** the notification.
4. Response Time
![](https://i.imgur.com/PWmRMxh.png)
seen time: when user unlock the phone
decision time: see -> act upon it
response time: arrive -> react
    - Alert mode vs Seen Time: Seen time is fastest when the phone is in vibrate mode and slowest for silent node. (**one-way ANOVA**)
    - Ongoing task type vs seen time: Notifications are seen fastest when the user is commuting and slowest when idle.(**one-way ANOVA**)
    - onging task complexity vs seen time: User’s attentiveness increases (reducing the seen time) with the increase in the complexity of an ongoing task. (**weak negative correlation**)
    - What Factors Influence the Decision Time: The decision time is higher for the notifications from less frequently contacted senders.(**one-way repeated measure ANOVA**)
    - Notification representation matters: High-priority notifications get quicker response. (**t-test**)

5. Why is a notification disruptive
The perceived disruption was measured with a 5-point Likert scale, the responses are coded as: Strongly disagree=1, Somewhat disagree=2, Neu- tral=3, Somewhat agree=4 and Strongly agree=5.
- disruptive vs ongoing task complexity: Perceived disruption increases with the increase in the complexity of an ongoing task.(**Kendall’s Tau correlation**)
- Ongoing task completion level vs disruptive: Notifications are perceived as most disruptive if they arrive when the user is in the middle of or finishing a task, and least disruptive if the user is idle or starting a new task.(**one-way ANOVA** of the reported disruption was carried out for each class of task completion level-starting, in the middle, finishing and not doing anything)
- sender vs disruptive: Messages from subordinates and system messages (where the sender is not a person) are considered as most disruptive. Whereas, extended family members are considered as the least disruptive.(**one-way ANOVA**)
- ongoing task type: highest while working, lowest while idle. (**one-way ANOVA**)

6. Acceptance of notification
![](https://i.imgur.com/9fi4dC1.png)
- disruption vs acceptance: The response for perceived disruption are coded: Strongly disagree=1, Some- what disagree=2, Neutral=3, Somewhat agree=4 and Strongly agree=5. Likelihood of the acceptance of a notification de- creases with the increase in the perceived disruption. (**logistic regression** with low coefficient)
- Why are disruptive notifications accepted?
![](https://i.imgur.com/CVCtnKJ.png)

7. Personality
- disruption vs personality (**linear regression model**; DV: average disruption)
![](https://i.imgur.com/oJ6jxyd.png)

The average disruption is computed as a mean of disruption reported by the user through the questionnaires. All responses were encoded with the following values Strongly disagree=1, Somewhat disagree=2, Neu- tral=3, Somewhat agree=4, and Strongly agree=5.

8. Respond
- seen time/ decision time vs personality (**linear regression model**; DV: the mean of the seen/decision time of all notification received by the user.)
![](https://i.imgur.com/ah6cqJz.png)


## research design
1. in the wild study with app sending ESM
![](https://i.imgur.com/q2LyAG6.png)

2. dataset
![](https://i.imgur.com/N21P4z1.png)
Whether the application that triggered the notification was launched after the removal time of that notification -> infer the user’s response to a notification

3. 4 ESMs/ day, ESM is triggered only when a noti is handled with 4-hour time window.
![](https://i.imgur.com/6vp5M7o.png)



## notes
1. *receptivity*: a user’s reaction to an interruption and their subjective experience of it.
2. *opportune moments*: moments in which a user quickly and/or favorably reacts to a notification


## questions
1. why senders(in What Factors Influence the Decision Time part) are analyed with repeated ANOVA?

## thonghts
A well contructed paper with clear contributions supported by statistics analysis(ANOVA, t-test, correlation analysis, linear regression)