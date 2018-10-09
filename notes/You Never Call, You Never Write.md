
# [“You Never Call, You Never Write”: Call and SMS Logs Do Not Always Indicate Tie Strength](https://dl.acm.org/citation.cfm?id=2675143)
Modeling tie strength using SMS and phone logs. At the same time, using qualitative data to suggest the incompleteness of using only these data to inform the tie strength.

### Method
- 40 participants, 24,370 phone contacts, 16,940 calls, 63,893 SMS messages, and 1,853 MMS messages.
- each participant provide 70 contacts
- relationship type contain strong tie
    - immediate family
    - extended family
    - people they live with
    - coworkers
    - people they feel close to
    - people they do hobbies with
- per contact level
    1. How close do you feel to this person? (5-likert scale)
    2. How strongly do you agree with the statement “I talk with this person about important matters”?
    3. How strongly do you agree with the statement “I would be willing to ask this person for a loan of $100 or more”?
    4. How strongly do you agree with the statement “I enjoy interacting with this person socially”?

- social tie groud truth
    - strong tie - the top group (rank 1-4)
    - medium tie - the middle group (rank 5 – 19)
    - weak tie - the remaining contacts

### Key points
- feature exploration: These trends are consistent with tie strength theory: more communication on more channels indicates a strong tie. However, our dataset has a number of counterexamples, pointing to critical challenges for automatically inferring tie strength from communication behavior.
![](https://i.imgur.com/5L8Vi4b.png)
![](https://i.imgur.com/iM2I1nk.png)
![](https://i.imgur.com/xGIn7M4.png)

- features
    - a total of 153 machine learning features: 17 from the contact list, 66 from call logs, 36 from SMS logs, and 34 from combined calls and SMS. These features are based on [Min et al](https://github.com/dimension4TW/paper_notes/blob/master/notes/Mining%20Smartphone%20Data.md).
        - Intensity and regularity
        - Temporal tendency
        - Channel selection and avoidance
        - Maintenance cost

- models
    - SVM
    - leave-one-participant-out cross-validation (each fold contained data from one participant)
![](https://i.imgur.com/rbmnfid.png)
    - Class Condition
        - 3-class: classifies as strong, medium-strong, or weak
        - 2-verystrong: binary classifier that combines medium- strong and weak ties into one class
        - 2-mediumstrong: binary classifier that combines strong and medium-strong ties into one class
    - Dataset
        - all: includes all contacts on the 70-person list
        - contactlist: includes only contacts from the 70-person list who appear in the user’s phonebook (see Figure 2)
        - somecomm: includes only contacts from the 70-person list with at least one logged SMS or call (see Figure 3)
    - low recall in strong tie class
- interview results: provide insight into the misclassification
    - The communication logs only capture relatively recent behavior, and they do not contain the data that indicates a strong long-term relationship.
    - A large amount of interpersonal interaction that happens outside of phone calls and text messages, including communication in other media and face-to-face communication.