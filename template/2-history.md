## History
*Maximum 1 page*
*Describe the V1 POC as planned by Sprint10.*
*What did you learn?*
*What is missing to bridge from PoC to MVP?*

### Description of V1 PoC as Planned by Sprint 10

The initial Proof of Concept (PoC) for our product was planned and executed over the course of 10 sprints, each lasting a week. Key features developed included:

- **User Authentication:**
  We use Google authentication for user login. On their first login, users are required to either choose an existing association to join or create a new one.
- **Core Feature Implementation:**
  - Treasury Management: Our app's first core feature is managing the treasury of an association. Users can effortlessly create budgets, scan receipts, and accurately record them in the accounting books, simplifying financial management.
  - Event Management: The second core feature focuses on overseeing association events. Users can efficiently manage tasks, view them on a map, and integrate them into their schedule, enhancing coordination and productivity.
- **Initial UI/UX Design:**
  - User-Centric Interface: The design prioritizes ease of use and intuitiveness, ensuring that users can navigate the app and utilize its features with minimal effort.
  - Consistent Visual Design: A consistent color scheme (blue), typography, and iconography were employed to create a cohesive visual experience.
- **Database Integration:** We transitioned to using Supabase for our database needs. Supabase, being a relational database, was essential for our project requirements, offering robust data management and real-time capabilities.
### Learnings from the V1 PoC

- **Team Collaboration Challenges:**
At times, backend and frontend developers were working on the same part of the application simultaneously. This necessitated excellent communication skills, as the frontend developer had to convey their requirements to the backend developer. Thus, coordinating both sides effectively presented some challenges and led to delays.
- **Technical Challenges:**
We switched the database we were using: initially, we started with Firebase, but we quickly transitioned to Supabase. The reason for this change is that Supabase is a relational database, which was essential for our project. In contrast, Firebase uses NoSQL, which does not support relational databases.

### Bridging the Gap from PoC to MVP
What features were not included in the PoC but are necessary for a functional MVP: 
- Notifications:
  - Treasurer Notifications: Notify treasurers when new receipts are pending for reimbursement, ensuring timely financial management.
  - President Notifications: Alert the president when new members request to join the association, streamlining the approval process.
- Chat :
  - Discussion Tab: Include a dedicated tab where members of an association can discuss various topics, enhancing communication and collaboration.
  - Access to Meeting Minutes: Provide easy access to the minutes of meetings within the chat tab, allowing members to review and discuss past meetings.
- Home screen:
  - Upcoming Events: Display upcoming events on the home screen so members can quickly see what's scheduled next, promoting better participation and planning.
  - Annoucements: Display important annoucement that should not be missed
- Task Management Enhancements:
  - Task Assignment Notifications: Notify members when tasks are assigned to them, ensuring they are aware of their responsibilities.
  - Task Completion Tracking: Notify relevant members when tasks are completed, maintaining accountability.
- Event Participation Tracking: Keep a record of events each member has participated in, contributing to a sense of accomplishment and engagement




