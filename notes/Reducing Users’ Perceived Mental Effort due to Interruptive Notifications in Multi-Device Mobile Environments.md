# Reducing Users' Perceived Mental Effort due to Interruptive Notifications in Multi-Device Mobile Environments

Pervious work has shown that using UI Event can effectively reduce nobile users' mental burden by detecting oportune breakpoint. In this work, in addition to UI event, adding pysical activity is able to improve the performance of detecting the breakpoint of mobile users.

## Key points
1. Common approaches to address interruption overload:
- defer noti to opportune moment -> breakpoint
- mitigate the interruptive nature of noti -> change the modality (eg. silent mode, vibration, LED)
2. principles for detecting breakpoints in Attelia:
- feasible for mobile and wearable devices.
- support real-time detection.
- applied to deverse type of noti sources.
- all-day-long use
3. Attelia I
detect breakpoint a) without using dedicated psycho-physiology sensor b) real-time c) works with wide vareity of smart phone app
- smartphones only
- only when users activity manipulating her phone

4. Attelia II
- multi-device
- cover all aspects of a user's life including times while a user is not manipulating devices.

5. Breakpoint
- UI based breakpoint: while the device is actively being used.
- Physical activity based breakpoint: cover the time while user is not actively being used.

## Experiment
1 month with 41 participants(31 male, 10 female)

![](https://i.imgur.com/Nvx3KKW.png)
![](https://i.imgur.com/nqaNixM.png)

phase 1 result:
![](https://i.imgur.com/T3WiuQT.png)

phase 2: chosing the best 5 models(h,g,f,j,d) with the model they design in advance.

Systme Arch

Attelia I
![](https://i.imgur.com/2Vjla1E.png)

Attelia II
![](https://i.imgur.com/q7958lk.png)
![](https://i.imgur.com/BaWsV1p.png)
![](https://i.imgur.com/sj63zUN.png)

## Questions
1. None the participants uses a smartwatch before the experiment.
2. Using 10-likert scale to decide the breakpoints may not be accurate.
![](https://i.imgur.com/OQjdncQ.png)

## Ref
1. multi-display environment for notification
- Dostal, J., Kristensson, P. O., and Quigley, A. Subtle gaze-dependent techniques for visualising display changes in multi-display environments. In Proceedings ofthe 2013 International Conference on Intelligent User Interfaces, IUI ’13 (2013), 137–148.
- Garrido, J. E., Penichet, V. M. R., Lozano, M. D., Quigley, A., and Kristensson, P. O. Awtoolkit: Attention-aware user interface widgets. In Proceedings ofthe 2014 International Working Conference on Advanced Visual Interfaces, AVI ’14 (2014), 9–16.
