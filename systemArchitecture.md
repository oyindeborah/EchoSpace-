EchoSpace System Architecture

Overview
EchoSpace transforms geolocation data into personal memory maps. The architecture supports real-time location tracking, emotional tagging, and memory visualization.

Frontend
- **Framework:** React Native  
- **Features:**  
  - Map visualization (Google Maps SDK)  
  - Memory Card view (shows date, mood, song, and messages)  
  - Bottom navigation for Map, Journal, and Settings  
- **Data Flow:** User actions → API requests → Backend responses → UI updates

Backend
- **Language:** Node.js  
- **Framework:** Express.js  
- **Core Services:**  
  - Location tracking API  
  - Memory data API (fetch, update, delete memories)  
  - Sync engine for external data (Spotify, Photos, Messages)  

Database
- **Platform:** Firebase (Firestore)  
- **Collections:**  
  - `users`: profile data  
  - `memories`: linked to user IDs, stores location, media, and emotional context  

Communication Flow
- Mobile app → REST API (Express) → Firestore DB  
- Push notifications: Firebase Cloud Messaging  
- Auth: Firebase Authentication  

Security
- User data encrypted at rest and in transit  
- OAuth2 integration for external APIs (e.g., Spotify)

Feasibility
The stack ensures scalability, low-latency sync, and ease of development.  
It uses widely supported open-source tools for fast prototyping and mobile readiness.
