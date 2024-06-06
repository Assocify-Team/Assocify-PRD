## Non-Functional Requirements
*Which are the applicable laws and regulations?*
*What are your internal policies?*
*Which privacy features do you need from the phone?*

*What kind of traffic patterns do you expect to see?*
*Are there known periods of bursty traffic that the MVP must be designed to support?*


### Security, Privacy, and Data Retention Policies:
Assocify is an app that is data-centric. One of the main goals of the app is to store treasury data on a server, so it can be accessed by specific memebers of the associations (like comitees), while the other members cannot have access to the data. Since the data that Assocify manages is often sensible (we are talking about accounting information, which needs to be kept secret), the final app would need to store all acconting data in an encrypted form. The data should be end-to-end encrypted, since we want the users to be sure that the data they upload is not seen nor modified.  
#### Applicable Laws and Regulations:

#### Internal Policies:

#### Privacy Features Required from the Phone:
The app assocify will need three specific authorizations: 
- Camera authorization
- Geolocalisation access
- Storage access

However, all the authorizations are optional and only asked in the case they are needed. For exeample, the camera is asked the first time the user wants to upload a receipt, or wants to change it's profile picture. The localization will also be asked the first 

### Adoption, Scalability, and Availability:

#### Expected Traffic Patterns:
The two main usages of the assocify app would be for event management and accoutning. We can imagine that the usage linked to accounting would be pretty constant, since the comitee would have to manage the treasury almost constantly. However, we still have to take into account that the usage of the application could increase during the fiscal year-end, since all associations would be reviewing and checking the app at the same time to verify that the accounts are correct.

However, the challenge related to traffic would be linked on the usage during the events: we know that during an event, ideally all the staffs would use the app to upload their receipts, update the tasks that are done and communicate between each other. We also consider that all the staffs would want to access to their updated gamified statistics, which would increase even more the traffic between the server and the different users. Thus the main case we have to take into account is how to manage traffic during the organization of a big event. We also have to take into account the case where multiple organizations have organized an event at the same time, which could increase even more the traffic with the server.
#### Design for Bursty Traffic:
We will use two strategies to handle bursty traffic:
-Caching: 