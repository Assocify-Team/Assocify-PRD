# Timeline/Resource Planning

### Overall Schedule
- **Project Initiation Date:** March 15, 2024
- **Expected Completion Date:** May 30, 2024
- **Key Milestones:**
  - **Milestone 1 [Project Kick-off]:** April 12, 2024
  - **Milestone 2 [First End-To-End]:** May 3, 2024
  - **Milestone 3 [Mid Completion]:** May 17, 2024
  - **Milestone 4 [V1]:** May 30, 2024

### Required Resources
- **Human Resources:**
  - 2 Backend Developpers
  - 5 Frontend Developpers
  - 3 also working on UI/UX 
- **Software Tools:**
  - Development Environment: Android Studio
  - Design Tools: Figma
- **Database:** Supabase
  

### Intermediate Milestones
- **Milestone 1:**

| **Sprint Number** | **Duration dates** | **Objective** | **Outcomes** |
| --- | --- | --- | --- |
| 1 | March 15 - March 21, 2024 | Setup initial project environment and tools. Implement basic functionalities like GitHub setup and branch protection. | Set up project, have good work environnement ready. Basic google authentication. First user stories and figma screens. |
| 2 | March 22 - March 28, 2024 | First design choices on figma and in app. | Initial wireframes and screens on Figma. UI for the login flow and new receipts. Start of APIs for users and associations.  |
| 3 | April 5 - April 11, 2024 | Login flow. More work on treasury. | API for receipts. Viewmodels for the login flow and receipts. Navigation for login flow. UI for treasury. |

- **Milestone 2:**

| **Sprint Number** | **Duration dates** | **Objective** | **Outcomes** |
| --- | --- | --- | --- |
| 4 | April 12 - April 18, 2024 | Photo capture. Change to Supabase. Maps. | Photo capture. Change from Firebase to Supabase. Google Map for the events. UI for events' tasks, for budget and balance screens in treasury, and for Profile page. |
| 5 | April 19 - April 25, 2024 | Supabase APIs. Change to OSM. Finish receipt flow. | Translation of previous APIs to Supabase, adding API for events. Viewmodels for profile personal settings, tasks, events. Transfer from GMaps to OSM to use EPFL's map. Receipt flow done. |
| 6 | April 26 - May 2, 2024 | First epic done. Finish task flow and main profile page. | Task and budget APIs. Can change and add association once connected. First epic test. Viewmodel for treasury items and tasks. Stay connected even while leaving the app. Finish Figma with links between screens. Tasks and profile done.  |

- **Milestone 3:**

| **Sprint Number** | **Duration dates** | **Objective** | **Outcomes** |
| --- | --- | --- | --- |
| 7 | May 3 - May 9, 2024 | Loading. Tasks in all the event's screens. | All Treasury related APIs. General loading system. Load images for receipt from database. Viewmodel for budget and balance. UI for event's schedule. Consistency between screens in all the app. |
| 8 | May 10 - May 16, 2024 | Finish Treasury. Add caching. | Caching for reading information from databse added to all APIs. Working treasury sheets with consistency and cascading with all subtabs, using filters, categories, items. Pins on event's map. Schedule properly displayed with overlapping tasks. |

- **Milestone 4:**

| **Sprint Number** | **Duration dates** | **Objective** | **Outcomes** |
| --- | --- | --- | --- |
| 9 | May 17 - May 23, 2024 | All UI for settings. Fix all finishing details in treasury. | Pick task location. General snackbar gestionnaire for the whole app to give feedback to the user easily. All association settings UI. Link receipt to balance item. |
| 10 | May 24 - May 30, 2024 | Finish map and profile. Permissions. | API for members management. All images in the app are reloaded from the database. Viewmodel for all the association settings. Permissions (limitation to admins) in association settings and treasury. GPS sensor. Be able to reload by dragging down. |

