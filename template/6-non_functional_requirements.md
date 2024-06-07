## Non-Functional Requirements

### Security, Privacy, and Data Retention Policies:

#### Security Policy:
One of the main objectives of the Assocify application is the storage and management of accounting data. Since this data is considered as sensible it should at no cost leak. For this reason all data related to the accounting part of the application will be encrypted on the servers, with only the members of the associations having access at the encryption key. The key would not be stored in the servers, but will be owned by all the members of the app having the comitee status. When a new member of the app is accepted as a comitee, he receives directly from the comitee that accepted him the key to access the treasury database. This way even if there is a data breach the treasury data will be difficult to retrieve. For the event data, we will divide the comitee data in a private part that will be encrypted in the same way, and a public part that can be acessed by all the staffs and will be stored in clear. We consider this data to not be critical, and a data breach on this data would not have a significant impact on the security of the Association.

#### Privacy Policy:
For the first version of the application, the only data we plan to collect from the users is their name and the associations they are part of. These informations will be stored on the database, but the only persons that will be able to see it will be the users. No information will be exchanged with a third-party. 

One major privacy concern of our applicationis the geographical localisation. During an event, a user can accept for it's position to be tracked, so that he can see how distant he is from a certain place and check which task is the nearest. The localisation information is kept as secret, as it is not sent in the server. The distance calculation is done locally, so that there is no way for the developers of application to know where the different users are located.

As for the event data, it will be processed in an anonymized way to retrieve statistical data (duration of an event, number of task). All personal data (name of users, name of tasks, exact location) will be removed to ensure the privacy. The resulting data will be use to improve our service, such as knowing which are the dates where the most events take place, the number of tasks or the number of staffs. This way we can adapt our sevices and servers by knowing the dates where we will receive the most stress.


#### Data Retention Policy:
For it to be functioning, the Assocify app necessitates lots of data. For this reason we have developed these policies on data retention:

- The treasury data is end-to-end encrypted. This is an important feature, since the treasury data is considered important and should not be compromised by an attack on the server.

- The event and the profile data are stored in the server. In this case the end-to-end encryption will not be possible since both the event and profile data will have to be acessible to a growing number of users. However, the data will still be encrypted during the communications, so that it cannot be robbed by a malicious attacker.

- User data is stored on the server. There is no password stored (the authentication is managed by Google), so there will only be the name and the email adress to be stored. 

- After one year of inactivity, the user is notified by mail. In case of an absence of a response, all data linked to the user is deleted from the server. For an association, it's after three years of inactivity (the data on the server has not been modified nor acessed) that the data is eliminated.

- At any point in time, the user can decide to delete it's data. He has a period of 30 days to retract the demand, after that it's data will be deleted permanently. For an association, it's the president that has to ask for the deletion, and the period to retract is the same as for the user.

- The user can ask at any time all the data from his user profile or from his association if he is the president. This data can be used as a backup, or to check what informations are stored on the database.

### Adoption, Scalability, and Availability:

#### Expected Traffic Patterns:
The two main usages of the assocify app would be for event management and accounting. We can imagine that the usage linked to accounting would be pretty constant, since the comitee would have to manage the treasury almost constantly. However, we still have to take into account that the usage of the application can increase during the fiscal year-end, since all associations would be reviewing and checking the app at the same time to verify that the accounts are correct.

However, the challenge related to traffic would be linked on the usage during the events: we know that during an event, ideally, all the staffs would use the app to upload their receipts, update the tasks that are done and communicate between each other. We also consider that all the staffs would want to access to their updated gamified statistics, which would increase even more the traffic between the server and the different users. Thus the main case we have to take into account is how to manage traffic during the organization of a big event. We also have to take into account the case where multiple organizations have organized an event at the same time, which could increase even more the traffic with the server.


#### Design for Bursty Traffic:
We will use several strategies to handle bursty traffic:

- **Caching:** we will add a tag on the server and on the app to tell when the server is overwhelmed. When an user's app receives a confirmation with the overwhelmed tag, the application starts taking the data from the server automatically and does so only when asked to or for critical operations (update a to-do task). Once the traffic is no longer bursty, it stops sending the overwhelmed tag so the app knows that it can start reusing the app as intended.

- **Priority system:** There are some operations that are more important than others. When having a period of bursty traffic, we give priority to all treasury operations (saving receipts or modify budgets) before doing the events operations. This is due to the fact that we want to be sure that the accounting remains consistent, while we have less problems having the tasks of the event to be a little more inconsistent.