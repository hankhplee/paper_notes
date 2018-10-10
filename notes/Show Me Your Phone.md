# Show Me Your Phone, I Will Tell You Who Your Friends Are: Analyzing Smartphone Data To Identify Social Relationships

using calls, SMS, MMS and email to predict social relationship(work, family and social-interation)

## Exp
### Data Collection
19 participants data collection, classify contacts into acquaintances (ACQ), coworkers (WORK), family (FAM), friends (FRIENDS), and school/university (UNI).

### Dataset
1. In total, 1,895 phone contacts, 8,207 calls, 25,805 e-mails, 22,566 SMS, and 102 MMS messages were collected.
![](https://i.imgur.com/25bOkGp.png)
![](https://i.imgur.com/Z4i0dGB.png)
![](https://i.imgur.com/n6DxXQf.png)

2. overall number of contacts for each relationship category is different: 30% are classified as acquaintances, 27% as friends, 23% as coworkers, 14% as uni/school, and 6% as family members.
![](https://i.imgur.com/LUOR7va.png)

3. most interactions are beased on a unique channel(73% of the contacts).

4. Temporal factor
![](https://i.imgur.com/PpywsV4.png)
![](https://i.imgur.com/kuX2HaD.png)

### Feature Extraction
1. features are based on [Min et al.](https://github.com/dimension4TW/paper_notes/blob/master/notes/Mining%20Smartphone%20Data.md)
![](https://i.imgur.com/Tn9urgR.png)
2. correlation-based features selection and obtain 29 recommended features, and no MMS features were included.

## Model
1. models
    1. SVM
    2. C4.5
    3. naïve Bayes
2. balancing dataset
    1. Under: under-sampling the major class of DATA by randomly resampling the instances without replacement.
    2. SMOTE: using the synthetic minority oversampling approach
    3. SMUNDER: the combination of the two aforementioned approaches
#### Three Categories: WORK, FAM, andSOC
![](https://i.imgur.com/QXPAXEQ.png)
#### Five Categories: ACQ, WORK, FAM, FRIENDS, and UNI
![](https://i.imgur.com/xrFXB16.png)

### Evaluation
#### Three Categories: WORK, FAM, andSOC
![](https://i.imgur.com/o0bRraN.png)
![](https://i.imgur.com/YJ5Jzg5.png)
![](https://i.imgur.com/GZxHcNK.png)
#### Five Categories: ACQ, WORK, FAM, FRIENDS, and UNI
![](https://i.imgur.com/pYUmS5T.png)
![](https://i.imgur.com/oJhtxmq.png)


## Note
1. Time period
![](https://i.imgur.com/PpywsV4.png)
