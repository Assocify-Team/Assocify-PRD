## Non-Functional Requirements
*Which are the applicable laws and regulations?*
*What are your internal policies?*
*Which privacy features do you need from the phone?*




### Security, Privacy, and Data Retention Policies:
Assocify is an app that is data-centric. One of the main goals of the app is to store treasury data on a server, so it can be accessed by specific memebers of the associations (like the comitees), while the other members do not have access to the data. Since the data that Assocify manages is often sensible (we are talking about accounting information, which needs to be kept secret), the final app would need to store all acconting data in an encrypted form. The data should be end-to-end encrypted, since we want the users to be sure that the data they upload is not seen nor modified. 

Another priority would be the management of user data: we ask to the user to input their name, a profile picture, and if the user is a staff at an event we would like to have it's localisation. While the name and the profile picture will be stored on the database, the localisation will only be stored on the user's phone. This will prevent data leaks of the position, which would be problematic on a security point of view. Another feature linked to the user would be the score and ranking linked to the gamification aspect of the app. Since the values in this case can't be encrypted (we need a way to compare the different values between each participant), we will ensure the privacy by adding an option in the settings to disable the gamification aspect for the user, if he doesn't want his data stored in the server.

As per the security aspect of the application, Assocify is also based on a strongly based on a system of permissions. Thus we need for the system to be well implemented and tested, to avoid for a member of an association to access to critical data. Thus one major policies we have to ensure is that only members of the comitee will have the possibility to modify the
#### Applicable Laws and Regulations:
The main concern we would have would be in the manner we store the user's data. We would to follow the GPRD for the users in Europe, and the varionited States.
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
- Caching: we will add a tag on the server and on the app to tell when the server is overwhelmed. When an user's app receives a confirmation with the  