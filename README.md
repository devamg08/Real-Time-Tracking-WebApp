Live, Zomato/Swiggy-style tracking in your browser.
A device streams its GPS location to a Node.js server over Socket.IO,
and a Leaflet web map updates markers in real time.




✨ Features

📍 Live locations: Markers move instantly as devices report new coordinates

👥 Multi-device: Track multiple clients simultaneously

🗺️ Beautiful maps: Leaflet + OpenStreetMap tiles (no paid keys)

🧩 Simple API: Minimal socket events for send/receive location

🧭 Accuracy options: Choose frequency, distance threshold, and more

🧱 Room-based isolation (optional): Group devices by order/trip/tenant




Device (Browser)                      Server (Node + Socket.IO)                 Viewer (Map UI)
-----------------                     ---------------------------               ----------------
navigator.geolocation  --emit-->  send-location {lat,lng,id}   --broadcast--> receive-location
                ▲                                                                        |
                │                                             │
                └-- watchPosition         └-- tracks last known per socket               └-- Leaflet marker setLatLng(...)





🧪 Try it with two devices

Open the map on Device A (your phone).

Open the same link on Device B (laptop).

Move Device A → watch its marker update on both screens 🤩
