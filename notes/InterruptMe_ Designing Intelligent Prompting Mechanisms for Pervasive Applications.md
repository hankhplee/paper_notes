# InterruptMe: Designing Intelligent Prompting Mechanisms for Pervasive Applications

The work seek to answer whether and how suitable moments for interruption can be identified and utilized in a mobile system, using activity, location , time if day , emotion and engagement information.

## Key Points and Findings
### 1. Identifying Opportune Moments for Interruption: 
- Reaction presence: the work aims to predict if a recipient will react to an interruption.
- Time to reaction: the work aims to predict if a recipient will react to an interruption within a given time interval.
- Sentiment: the work aims to predict a recipient’s attitude to- wards a moment in which a notification comes.

### 2. Context – Response Hypothesis:
The work is the first to investigate notification interruptibility in relation to smartphone-sensed context.
- Notification context. The context in which a notification is sent determines an interruption success.
- Response context. The context in which a reaction is recorded determines an interruption success.
- Notification-response context change. In case of a successful interruption, the context changes from the notifi- cation to the reaction.
- Notification context variation. The variation of context at the notification time indicates an interruption success.

### 3. MODELLING INTERRUPTIBILITY
The goal is to predict the actual outcome (interruptibility) AOi at an interruption instance (notification that is sent out) i, using N sensed features f1, ..., fN that describe the current context.
![](https://i.imgur.com/zTulqCs.png)
![](https://i.imgur.com/w9xr9Rt.png)

- Evaluation of Interruptibility Models: 
    * The work uses a trace-driven simulator to evaluate the performance of the models.
    * In SampleMe we take fine-grained accelerometer readings five minutes before and up to five minutes after each notification. We calculate the activity variation level and use it as a feature in the analysis.
    * Outcome AOi of each of the instances in the dataset as a binary successful or unsuccessful.
    * **reaction presence**: we label as successful any instance where a user responded to the notification
    * **time to reaction**: we label as successful any instance where a user responded no later than td after a notification
    * **reaction sentiment**: we label as successful any instance where a user indicated that the interruption was not irritating beyond a given threshold.

![](https://i.imgur.com/LfRdnzu.png)

- Batch Learning
    - In SampleMe the sentiment was recorded as an answer to the question “Is this a good moment to interrupt?” on a four-point Likert scale with the following labels: not at all, a little, somewhat, and very much. 
    - optune memont: little or above
    ![](https://i.imgur.com/akU1T3k.png)
    ![](https://i.imgur.com/kkwQYE8.png)
    - the influence of the context at the time of response on the outcome of the interruption: sentiment
    ![](https://i.imgur.com/qRxKrMp.png)
    - the relationship between notification-response context change and the user reaction: the change in the **Bluetooth environment** is significantly different between opportune and non-opportune moments for interruption
    ![](https://i.imgur.com/2faShrf.png)
    - while previous works point out the catiation of context at the time of noti indicates opportune moment, the work dd not find a significant correlation btw interruptibility and activity change with a stricter definition of the opportune moment for interruption.
    ![](https://i.imgur.com/CPDPzhO.png)
- Online Learning
![](https://i.imgur.com/npuIoXb.png)

### 4. EXPERIMENTAL EVALUATION FOR INTERRUPTME
![](https://i.imgur.com/4lnQ8Nc.png)
- set the response treshold to 10 min:  
    - ![](https://i.imgur.com/aayJNf4.png)
    - Ten minute is also the minimum interval between consecutive interruptions in the experiment
- Sentiment towards interruption moments
![](https://i.imgur.com/HH5plPl.png)
- Amount of Interruptibility: the recent exposure to interruptions determines user frustration, therefore, sentiment towards interruptions in the experiment. Isolated notifications tend to be more favorable than the ones received after a large number of recent notifications. However, the context can remain in the same, favorable, state for an extended period of time, in which case our application will deliver notifications back-to-back and, as shown in Figure 9, exhaust the interruptibility of the user.
![](https://i.imgur.com/8DApbFj.png)

### 5. Responsiveness: 
a user’s feedback reaction to a notification. Responsiveness is an important aspect of interruptibility, especially for communication applications

### 6. Attentiveness: 
the level of attention that the user has towards an incoming interruption.


## Experiment
1. Dataset:
- The application notifies the user about a survey, which consists of questions related to user’s attitude towards being interrupted, his location, activities, company, and emotions
![](https://i.imgur.com/UlCgyyv.png)


- The application senses user’s **GPS** coordinates, **Bluetooth** and **WiFi environment**, **phone’s accelerometer**. Context sensing is performed once a notification is sent to a phone, and once a user replies to the survey.
- 2 weeks, 20 adult subjects(20~37 years old)
- 8 notifications were sent to each participant per day at random times between 8 am and 10 pm local time.
- Location labeling: “Residential”, “Work”, or “Public”.


## Note
1. **How to process sensor raw data:**
We calculate the change in the reported GPS location, accelerometer features, Bluetooth and WiFi environment for the two context readings for each answered notification. The GPS change is expressed in meters, accelerometer change is represented by the intensity of a vector of accelerometer mean, variance and MCR between the two readings, and Bluetooth and WiFi change is expressed with the Jaccard distance between the sets of sensed devices recorded at the two context points.
2. **How to measure context change**:
In order to measure context changes we take fine-grained accelerometer readings from five minutes before to five minutes after each notification. We then calculate a vector that consists of the mean, variance and the mean crossing rate in each one-minute window and measure the Euclidean distance between vectors recorded in subsequent time windows. We take the maximum observed distance as a measure of activity change at the notification time. 
3. **N of 1 randomized trial:** The work alternates days when notifications about surveys are managed through the InterruptMe library with days when notifications are received randomly. The N of 1 trial helps us avoid the bias in response reactions that would skew the results if we were to employ a test method where the users are split into two groups according to the notification policy.
