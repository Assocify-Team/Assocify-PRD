## Design and Implementation

*List the key libraries, languages, components used by the MVP.*
*If applicable, describe essential screens.*
*Decompose the MVP into functional blocks.*
*What data are you collecting / managing?*
*How is it organised?*
*Where is it stored?*
*How is it shared/copied/cached?*
*How is the application developed, tested and deployed?*
*Any special infrastructure requirements.*


### Frontend

#### Key Libraries, Languages, and Components
- **Languages and Frameworks:** 
- **State Management:**
- **Navigation:** 
- **UI Components:**

#### Essential Screens
- **Login Screen:** Secure entry point for user authentication.
- **Home Screen:** Overview of upcoming events, recent transactions, and notifications.
- **Event Management Screen:** Allows users to create, edit, and view upcoming and past events.
- **Budget Overview Screen:** Displays current budget status, recent transactions, and allows entry of new transactions.

### Backend

#### Functional Blocks
- **Authentication** is managed by Supabase's extensive authentication flow
- **Treasury** is handled via Supabase's databases (postgres), and Storage, for images
- **Events** are handled via a few tables in Postgres
- **Profile and association management** are also handled in Postgres and Supabase Storage
- **Maps** are handled by EPFL's map servers and OpenStreetMap

### Data Model

#### Data Collection/Management
- **User Data:** We store the user's display name. It is easy to change, and owned by the user. No other data is externally visible, but some login information is kept.
- **Association Data:** The data related to an association is all stored within Supabase. This includes events, members, receipts, and other treasury information. It can be protected via row-level security.


#### Organization and Storage
- **Database:** All non-image data is stored within databases linked together via foreign keys.
- **Data Organization:** All images are stored in a filesystem-like structure with folders.

#### Sharing, Copying, and Caching
- **Data Sharing:** The data is only transferred between the server and the client, never between clients or externally. As such.
- **Caching Strategy:** Caching is done by storing portions of the database locally, updated with our code, and refreshed upon the user's request. Upon app reload, the cache is not kept. Images are cached with a lifetime and are stored in a cache folder provided by Android. The cache has a maximum size.

The backend can also easily be extended to include indices on the databases, further increasing speed.

### Security Considerations
All communication is done via HTTPS. Row-level security will be added to all tables (they were designed with security in mind), meaning data is protected from authenticated but unauthorized access.

#### Infrastructure and Deployment
The application's backend is on Supabase, which can be self-hosted in its entirety. By default it will be hosted on supabase.com, but it is easy to move over to self-hosted hardware, if desired.

### Test Plan

#### Development, Testing, and Deployment Strategy
- **Unit Testing:** Implement unit tests with Junit tests for all components to ensure functionality and catch bugs early.
- **Integration Testing:** Conduct integration testing to verify that different parts of the application work together as expected.
- **System Testing:** Perform end-to-end system testing to validate the complete and integrated software product.

#### Special Infrastructure Requirements

