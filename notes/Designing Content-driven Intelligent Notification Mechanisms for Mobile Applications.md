# Designing Content-driven Intelligent Notification Mechanisms for Mobile Applications
The work discuss how content and context can be used together in order to design intelligent non-disruptive notification mechanisms. Also, the work take into account the type of information delivered and the social relationship between the information sender and reciever.

## Key Points and Findings
1. What define an opportune moment?
the user can respond to an interrupion in 4 possible ways:
a) handle it immediately
b) acknowledge it and agree to handle it later
c) decline it
d) withdraw it
2. The work hypothesize that a moment is opportune to deliver a notification only if the user handle the noti immdeiately.
3. Time delay in response to a notification: As shown in Figure 3, more than 60% of the notifications were clicked within 10 minutes from the time of arrival. In general the maximum response time taken by a user to handle notifications that arrive at opportune moments is 10 minutes. In this study, they choose 10 mins as the *threshold time delay* for responding the notification.
![](https://i.imgur.com/rgTKvVd.png)
4. Impact of the context on response time: 
    The data shows that the activity of users does impact hte response time of notifications.
![](https://i.imgur.com/we0vK34.png)

5. Impact of Content on Notification Acceptance
- Highest acceptance: The family chat and work email notifications with around 81% and 77% within 10 minutes of arrival time, respectively.
- The worst acceptance: system, tools, and music and media.

6. User-defined rule perform worse may lies in:
- user preferences change with time
- users can define very abstract rules as compared to the complex rules created with the data-driven approach by using numerous other features.

7. GENERIC VS PERSONAL BEHAVIORAL MODEL
- generic model achieves extremely high specificity (i.e., around 95%) because it gets trained with most of the rejected notifications in different contexts. 
- prediction model trained on a user’s personal data is more accurate than a generic prediction model trained on multiple users’ data

![](https://i.imgur.com/KGRDpU2.png)

8. Discussion:
- 70% of the notifications that a user receives belong to email and chat categories, and we can further use the social circles of users to sub-categorize email and chat notifications. But user do not create social circles on every communication app and not all communication applications facilitate users to create social circles.


## Experiment
1. Data Colleciton ![](https://i.imgur.com/2ccZCT2.png)
2. NotifyMe also collects subjective data from its users by triggering six questionnaires each day (new questionniare does not triggered for the next 30 minutes). 
![](https://i.imgur.com/RJMrOSV.png)
3. NotifyMe posts 12 notifications on the user’s smartphone containing information that is randomly chosen from breaking news, weather update, and Facebook likes to enhence the richness of the categories of information received by participants.
4. 35 participants btw 21 and 35.
5. The work split the chat and email notifications in the following four sub-categories based on the sender’s relationship with the recipient of a notification: 
    * Work: sender works or studies with the recipient
    * Social: sender has a social tie with the recipient
    * Family: sender is the recipient’s family member or relative
    * Other: sender not related to the recipient with the above relations
![](https://i.imgur.com/Rc8To4x.png)
6. Category probability list for each location:
- Workplace: work, social, family
- Home: social, family, work
- Other: family, social, work

7. Feature Ranking: the name of the app from which the notification is triggered, and the app category are the most important features.
![](https://i.imgur.com/A1ik13i.png)

8. Building prediction model:
- Data-driven learning
to evaluate the value of using the information type and social circle, the prediction models is built in three ways:
    1) without using information type and social circle; 
    2) using only information type; 
    3) using information type and social circle.

- User-defined Rules:
    base on answered questionnaires
    1) notification category
    2) best location
    3) best time

![](https://i.imgur.com/Gs7x397.png)


9. Online-learning: on day N a model was built by using notifications from day 1 to N and it was evaluated to predict the acceptance of notifications that arrived on day N+1.

![](https://i.imgur.com/wTxv6WS.png)



## Notes
1. Sesitivity: the proportion of actual positives which are correctly identified (i.e., number of notifications that are correctly predicted as accepted / number of notifications that are actually accepted)
2. Specificity: the proportion of actual negatives which are correctly identified (i.e., number of notifications that are correctly predicted as declined / number of notifications that are actually declined)

## Reference
1. **personal communication notifications are responded to quickly because of the social pressure and the exchange of time critical information by the communication applications:** Pielot, M., Church, K., and de Oliveira, R. An in-situ study of mobile phone notifications. In MobileHCI’14 (September 2014).

2. **a notification’s response is influenced by the user’s general interest in the no- tification content, entertainment value perceived in it and ac- tions required by the notification, but not the time of delivery:** Fischer, J. E., Yee, N., Bellotti, V., Good, N., Benford, S., and Greenhalgh, C. Effects of content and time of delivery on receptivity to mobile interruptions. In MobileHCI’10 (September 2010)