# Dismissed! A Detailed Exploration of How Mobile Phone Users Handle Push Notification
1. systematically split notifications into five **categories**, including a novel separation of messages into individual- and group messages.
2. conduct a comprehensive analysis of the behaviors involved in **attending** the notification.

## Key points and findings
1. main contribution:
    - updated statistics on the number of notifications that people receive per day from 5 different categories (messaging, group messaging, email, social, non-social) – being the first ever investigation considering group messages as a separate entity and using of a novel API for more accurate measurement;
    - a detailed exploration into how notifications are handled, investigating 4 different types of attendance (seen, checked, consumed, removed); and
    - the data and the code, appended to this paper, through which we arrived to these insights.

2. Definition of Attending in Previous Work
    1. Fischer et al. [10]:
        * interruptibility: “more interesting from a technical systems-oriented perspective, e.g. as a trigger to an action”
        * receptivity: considering the (emotional) experience of the interruption. 
        * opportune moments: interruption delivery as moments that “minimise the detrimental effects of interruptions”. 
    2. Turner et al. [31] identified four stages of responsiveness in the context of a study where a task-reminder app frequently created notifications to ask user to check off a to-do list item: 
        (1) **Unreachable**: the user did not react to the arrival of the notification, either because they were not interrupted or did not want to triage any notification;
        (2) **Reachable**: the user interacted with the device (e.g. turned the screen on) to – presumably – triage the notification, but may not have proceeded further; 
        (3) **Engageable**: the user was reachable and proceeded to access the notification list (which may re- quire them to unlock the device), but may dismiss it or not proceed further; and 
        (4) **Receptive**: the user was engage-able and proceeded to tap on and consume the notification, opening the application.

3. Notification Categories
* Messaging
    (1) messages are the most frequent notifications [29, 25]
    (2) they are usually targeted directly at the receiver and thus usually highly relevant, and 
    (3) that one-to-one messaging is associated with the highest pressure to respond in a timely fashion.
* Group Messaging
* Email
* Social
* Non-Social

4. RESULTS | NOTIFICATION VOLUME
![](https://i.imgur.com/mMpOxZl.png)
![](https://i.imgur.com/qJqCXUG.png)
![](https://i.imgur.com/Qae11Bv.png)


5. RESULTS | NOTIFICATION ATTENDANCE

* Definition of Attendance
    * Shown
        * not included in the alaysis due to the uncertainty.
    * Seen
        * unlock the device or has already unlocked the device when the notification arrived
    * Checked
        * open the notification drawer
    * Comsumed
        * open the corresponding app of the notification
    * Removed
        (1) manually discarding the notification
        (2) the notification timing out
        (3) consuming the notification on a different device.

6. Notification Conversion Rates
the notification is considered consumed if the app is opened before the notification is removed
![](https://i.imgur.com/IngXGNv.png)

7. Immediate Attendance
![](https://i.imgur.com/FGCoBnj.png)

8. Notification Attendance Flow
    * Messages are Attended Fastest
    * Group Message are Attended Slower than Individual Messages
    * Messages Have Highest Consumption Rate
    * Few Differences in Time Until Checked or Consumed
    * NonSocial Notifications are Quickly Dismissed
    * Email and Social Notifications Take Longest to be Attended

9. Discussion
    * We confirm previous findings [12, 19, 29, 25] that the majority of mobile phone notifications originate from messaging applications.
    * We expected that group mes- sage notifications would be more frequent, since they involve a lot of people. However, we found that the majority of messaging notifications are from 1-to-1 chats. Nevertheless, this does not necessarily mean that there are fewer group message. Another explanation is that our participants muted group chats.
    * notifications from non-messenger apps are consumed at much lower rates (Email: 15.47%, Social, 26.55%, NonSocial: 16.19%) -> cross device
    * Notifications from non-messaging apps were removed significantly later than those of messaging apps. This indicates that participants take more time to arrive to the decision to dismiss a non-messaging notification. We hypothesize that there are two factors: there is less social pressure to respond immediately, and dismissing a notification is the harder choice to make, because it ultimately means to accept the possibility of missing out on something.
