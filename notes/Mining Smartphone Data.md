# Mining Smartphone Data to Classify Life-Facets of Social Relationships
call + SMS logs to predict life facet (family, work, and social). Experimental results on 40 users showed that we could classify life facets with up to 90% accuracy.

## Method
- 40 participants, 24,370 phone contacts, 16,940 calls, 63,893 SMS messages, and 1,853 MMS messages.
- each participant provide 70 contacts (70-contact list)
![](https://i.imgur.com/YP1ol11.png)

### Applying Machine Learning to Life Facets

- Mobile Communication Patterns
    - Intensity and regularity:The number of and duration of communication actions
        - ![](https://i.imgur.com/l8QgpFW.png)
        - ![](https://i.imgur.com/u8vDpGG.png)
    - Temporal tendency
        - ![](https://i.imgur.com/q3pRyV8.png)
    - Channel selection and avoidance
    - Maintenance cost: people apply different amounts of effort in maintaining different kinds of relationships, where effort (cost) can be evaluated based on the time to last contact between two individuals

- features selection
![](https://i.imgur.com/URHC6Rb.png)
![](https://i.imgur.com/wEcmHBn.png)

- models:
    - ![](https://i.imgur.com/i4ASroM.png)
    - SVMs (Polynomial kernel; d = 2)
    - NB
    - C4.5
![](https://i.imgur.com/TkUODqr.png)
![](https://i.imgur.com/2k8scru.png)
![](https://i.imgur.com/4CIrvdU.png)

## Discussion
- limitation
    - adding two facets: school and maintenance(ex. doctor, shop keeper)
