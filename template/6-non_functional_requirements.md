## Non-Functional Requirements

### Security, Privacy, and Data Retention Policies:
*Which are the applicable laws and regulations?*

*What are your internal policies?*

*Which privacy features do you need from the phone?*
#### Security Policy:
One of the main objectives of the Assocify application is the storage and management of accounting data. Since this data is considered as sensible and should at no cost leak public. For this reason all data related to the accounting part of the application will be encrypted on the servers, with only the members of the associations having access at the encryption key. The key would not be stored in the servers, but will be owned by all the members of the app having the comitee status. When a new member of the app is accepted as comitee, he receives directly from the comitee that accepted him the key to access the treasury database. This way even if there is a data breach the treasury data will be difficult to retrieve. For the event data, we will divide the comitee data that will encrypted in the same way than the treasury data, and the public data that can be acessed by all the staffs and will be stored in clear. We consider this data to not be critical, and a data breach on this data would not have a significant impact on the security of the Association.

For this reason the Role system will be implemented in a good to avoid that only persons with the right permissions have access to sensible 

#### Privacy Policy:
At the moment 



#### Data Retention Policy:

### Adoption, Scalability, and Availability:

#### Expected Traffic Patterns:
The two main usages of the assocify app would be for event management and accoutning. We can imagine that the usage linked to accounting would be pretty constant, since the comitee would have to manage the treasury almost constantly. However, we still have to take into account that the usage of the application could increase during the fiscal year-end, since all associations would be reviewing and checking the app at the same time to verify that the accounts are correct.

However, the challenge related to traffic would be linked on the usage during the events: we know that during an event, ideally all the staffs would use the app to upload their receipts, update the tasks that are done and communicate between each other. We also consider that all the staffs would want to access to their updated gamified statistics, which would increase even more the traffic between the server and the different users. Thus the main case we have to take into account is how to manage traffic during the organization of a big event. We also have to take into account the case where multiple organizations have organized an event at the same time, which could increase even more the traffic with the server.
#### Design for Bursty Traffic:
We will use two strategies to handle bursty traffic:
- Caching: we will add a tag on the server and on the app to tell when the server is overwhelmed. When an user's app receives a confirmation with the  