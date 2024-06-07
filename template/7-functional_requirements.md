# Functional Requirements

*Max 3 pages.*
*List the key features of the MVP precisely.*
*Include appropriate architectural diagrams.*
*Describe key internal functionality.*

## Key Features and Architecture of the MVP

### Key Features of the MVP

#### 1. User Authentication
- **Description:** Secure login/logout functionality using OAuth protocols with Google sign-in.
- **Purpose:** Ensures that only authorized users can access the app and perform sensitive operations, protecting users and organizations data.

#### 2. Budget Management
- **Description:** Real-time tracking of budgets and transactions with features to create, review, and adjust budgets. Includes a three-stage transaction process: pending, validated, and reimbursed.
- **Purpose:** Provides transparency and control over financial management, crucial for treasurers managing organization funds.

#### 3. Event Management
- **Description:** Tools for scheduling, coordinating, and managing events. Includes functionalities for task assignment, location tagging, and notification alerts.
- **Purpose:** Facilitates efficient planning and execution of events, enhancing participation and organizational efficiency.

### Key Internal Functionality

#### Caching and offline usage
**Motivation:** Assocify prioritizes ease of use and speed, but currently relies heavily on APIs that are fully connected to our online database. To improve performance and user experience, our application must support asynchronous requests to the database and implement robust caching mechanisms. This will enable the app to store frequently accessed data locally, reducing the need for repeated network calls and ensuring users to access its data everywhere. One final point is that continuously loading every map tile from free OpenStreetMap servers each time the user switches tabs would result in significant network usage. This can lead to increased data consumption, slower performance, and potential strain on the OpenStreetMap servers.

**Solutions:** To ensure full access to the app:
- Local data storage: We store data fetched from the database locally on the device. In cases where fetching data online fails, the app utilize this locally stored data to ensure continued functionality.
- Asynchronous data updates: Data additions to the database are handled asynchronously. This means that adding new data does not block the user interface or other operations and will be completed as soon as network conditions allow. This approach ensures a smooth and uninterrupted user experience even during periods of network instability.
- Local file caching for the map: The map tiles are cached in the application's local files, up to a certain limit of data. At this point, the fully functional cache management system selects which tiles to overwrite.

These solutions fits perfectly with our data model system. Every data we fetch from the database is interpreted by the application as entities (i.e data classes), which allows us to store everything locally.

(insérer image cool que j'envoie telegram)

#### Permission system for an unified app
**Motivation:** A core priority of Assocify is to provide a unified application that allows users to manage all their associations seamlessly. In each association, users can hold different roles, which grant them varying levels of permissions. This necessitates a dynamic and adaptable user interface that can easily adjust to reflect the user's specific role and permissions within each association.

**Solutions:** Multiple features allows us to have an unified app:
- Role-Based access control: The application implements a role-based access control system. This ensures that users see and interact with features and data appropriate to their specific roles within each association, enhancing both security and usability. A list of role is defined and can be attributed to users by the association's owner. This can be changed any time and fits associations hierarchy perfectly at the same time.
- Dynamic UI Adaptation: The user interface is highly flexible and context-aware, automatically adjusting to display relevant tasks, settings and information based on the user’s current role. This includes showing or hiding menu items, buttons, and access to certain features. By simply checking the user's role, any UI is ajustable.

This Role-Based access system is extremely flexible and scalable as the user role is stored in the database and can be retrived quickly. 
