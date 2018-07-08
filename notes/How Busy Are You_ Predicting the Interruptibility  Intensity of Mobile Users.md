# How Busy Are You? Predicting the Interruptibility  Intensity of Mobile Users

The work propose a 2-stage hierachy model to 1) predict whether the user will react to mobile notification 2) predict how interruptible the users are.

The work then introduce personality traits into the prediction model to provide good initial prediction for new users in the system.

## Key Points and Findings
1. People's interruptibility to notification is distributed among many levels, we can't just simply distinguish as interruptible and uninterruptible.
2. 2 stage hierarchical:
![](https://i.imgur.com/0rw9i7x.png)


    1 stage: predict whether users will react to mobile interruptions. 
    2 stage: predict how interrutable the users are.
3. For new users in the system, the modle users data of other users who share similar personality, so that it can reduce training time in early stage while maintain comparable prediction accuracy.
4. Measure interruptibility with 5 likert scale (highly interruptable, interruptible, neutral, uninterruptable, highly uninterruptable)
5. Collected data
    whose task: task sender
    what task: task content(mapped into the notification content from various app)
6. hypothesis: people's availability or busyness can also be related to potential tasks they could perform.
7. Prediction Model
    **First Stage: Reaction Prediction** 
    Distinguish Reaction/ Completeley unavaiable based on smartphone sensors, personal traits(Big 5)
8. The more pleasant, the more interruptible.
9. Participants were less interruptable at shopping places then at entertainment places.
10. Participants are less interruptible at work places than an entertainment places.
11. Interruptibility:
    Low: Study(4.36)
    High: Using phone(2.88)
12. Participants became less interruptible when the interruption took longer time.
13. Participants were more interruptible when interrupted by people they know, close to or see frequently than strangers.
14. People who have similar personality traits can behave similarly under similar contents.
## Experiment
1. **Data Colloction** ![](https://i.imgur.com/FpcvkVQ.png)
2. **1-stage Result** ![](https://i.imgur.com/zslDkUq.png)
3. **2-stage Result** ![](https://i.imgur.com/Cr8RaEh.png)
    ![](https://i.imgur.com/YUGhkbt.png)
    ![](https://i.imgur.com/lmYyBCU.png)
    ![](https://i.imgur.com/qDqhvmq.png)


## Notes
1. In general, acceptable response rate is 11%~60%.
2. test-MiniIPIP: ligthweight Big 5
3. BMIS: mood collection
4. Foursquare: GPS data labeling
5. Location categories: entertainment, health % medical, home, professional, church, restuarant, shopping, transportation, work, others.
6. activity categories: American Time Use Survey
7. Recall: completeness of the classifier
## Ref
1. **Location Category**: Richard Cooper and Bradley Franks. 1993. Interruptibility as a constraint on hybrid systems. Minds and Machines 3, 1 (1993), 73–96.
2. **Big 5**: Boele De Raad. 2000. The Big Five Personality Factors: The psycholexical approach to personality. Hogrefe & Huber Publishers.
3. **Notification from immediate family members are more acceptable**: Joel E. Fischer, Nick Yee, Victoria Bellotti, Nathan Good, Steve Benford, and Chris Greenhalgh. 2010. Effects of Content and Time of Delivery on Receptivity to Mobile Interruptions. In Proceedings ofthe 12th International Conference on Human Computer Interaction with Mobile Devices and Services (MobileHCI ’10). ACM, New York, NY, USA, 103–112. DOI:
http://dx.doi.org/10.1145/1851600.1851620
4. **Interpersonal relationship may influence how the interruption percieved**: Rikard Harr and Victor Kaptelinin. 2012. Interrupting or Not: Exploring the Effect of Social Context on Interrupters’ Decision Making. In Proceedings ofthe 7th Nordic Conference on Human-Computer Interaction: Making Sense Through Design (NordiCHI ’12). ACM, New York, NY, USA, 707–710. DOI: http://dx.doi.org/10.1145/2399016.2399124
5. **Driving interruptibility**: SeungJun Kim, Jaemin Chun, and Anind K. Dey. 2015. Sensors Know When to Interrupt You in the Car: Detecting Driver Interruptibility Through Monitoring of Peripheral Interactions. In Proceedings ofthe 33rd Annual ACM Conference on Human Factors in Computing Systems (CHI ’15). ACM, New York, NY, USA, 487–496. DOI:
http://dx.doi.org/10.1145/2702123.2702409
6. **Considering the notification content, respond time to notification can be predicted**: Abhinav Mehrotra, Mirco Musolesi, Robert Hendley, and Veljko Pejovic. 2015. Designing Content-driven Intelligent Notification Mechanisms for Mobile Applications. In Proceedings ofthe 2015 ACM International Joint Conference on Pervasive and Ubiquitous Computing (UbiComp ’15). ACM, New York, NY, USA, 813–824. DOI:
http://dx.doi.org/10.1145/2750858.2807544
7. **Predict 1)reaction presence 2) respond time 3) sentiment**: Veljko Pejovic and Mirco Musolesi. 2014. InterruptMe: Designing Intelligent Prompting Mechanisms for Pervasive Applications. In Proceedings ofthe 2014 ACM International Joint Conference on Pervasive and Ubiquitous Computing (UbiComp ’14). ACM, New York, NY, USA, 897–908. DOI:
http://dx.doi.org/10.1145/2632048.2632062

