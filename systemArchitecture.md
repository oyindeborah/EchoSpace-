EchoSpace System Architecture  

Overview  
EchoSpace operates on a **three-layer architecture** designed to connect location data, emotional context, and user experience.  
It transforms passive GPS data into interactive, emotional storytelling.

Core Layers  

Data Layer  
- Captures user location history via **Google Maps API**.  
- Pulls related media (Spotify, Google Photos, Notes).  
- Stores all data securely in **Firebase Firestore**.  

Memory Layer  
- Organizes raw data into “Memory Nodes” (location + time + emotion).  
- Detects recurring patterns such as revisited places.  
- Links emotional tags and reflection prompts to each node.  

Experience Layer  
- Displays nodes on a 3D interactive map in **React Native**.  
- Allows users to replay memories, tag moods, and write reflections.  
- Provides weekly insights like *“You often visit here on weekends.”*

Data Flow  
1. User’s GPS and media data are collected.  
2. APIs enrich the data with context (songs, images, messages).  
3. The backend processes this data and builds a **Memory Node**.  
4. The frontend displays the node on an interactive map.  
5. The user can interact, replay, or edit the memory.  

Technology Stack  

| Component | Technology | Purpose |
|------------|-------------|----------|
| **Frontend** | React Native | Mobile user interface |
| **Backend** | Node.js + Express | Logic and API endpoints |
| **Database** | Firebase Firestore | Cloud-based data storage |
| **Integrations** | Google Maps, Spotify | Context enrichment |
| **Authentication** | Firebase Auth | Secure login and data privacy |

Component Communication  
- The **frontend** sends user actions (e.g., mood tags, reflections) to the backend via HTTPS requests.  
- The **backend** interacts with Firebase to retrieve or update data.  
- The **database** returns structured memory data, displayed as interactive elements on the map.  

Feasibility  
This approach is technically realistic because:  
- Google and Spotify APIs are publicly accessible.  
- Firebase ensures secure and scalable storage.  
- React Native enables fast cross-platform development.  
- Node.js provides flexibility for data handling and API creation.  

System Diagram  

https://docs.google.com/document/d/1HKBbU5d_dXwtG7XJbVFMKNYcEV6PVOqKyXKDdq-AoVM/edit?usp=drivesdk

Summary  

EchoSpace merges emotional intelligence with location technology.  
It turns data most people ignore into reflective experiences — proving that the unknown product (Google Maps Timeline) can evolve into a deeply personal storytelling tool.
