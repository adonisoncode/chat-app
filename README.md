⚡ Ome-chat: Real-Time Messaging Platform

A high-performance, low-latency chat application featuring a modern "Cyberpunk/Terminal" aesthetic. Built with React.js and Firebase Firestore.

📖 About The Project

Ome-chat is a real-time messaging solution designed to demonstrate WebSocket-like behavior using serverless architecture. Unlike traditional HTTP polling where the client asks the server for updates, Ome-chat utilizes Firestore Listeners to push data to all connected clients instantly.

The UI is designed with a "Developer First" dark mode, featuring a responsive layout that works seamlessly on desktop and mobile devices.

🌟 Key Features

⚡ Instant Synchronization: Messages appear on all devices in milliseconds using Firestore onSnapshot listeners.

🔐 Anonymous Authentication: One-click entry using Firebase Auth (frictionless user experience).

🎨 Cyberpunk UI: Custom-built interface using Tailwind CSS with a Slate/Emerald color palette.

📱 Fully Responsive: Adaptive sidebar for desktop and streamlined header for mobile users.

🔄 Smart Auto-Scroll: Chat window automatically snaps to the latest message when received.

🚀 How to Run Locally

Follow these steps to get the project running on your machine.

Prerequisites

Node.js installed (v16 or higher)

npm or yarn

Installation

Clone the repo

git clone [https://github.com/adonisoncode/ome-chat.git]
cd ome-chat



Install NPM packages

npm install



Configure Firebase

Go to Firebase Console.

Create a new project.

Enable Authentication (Sign-in method: Anonymous).

Enable Cloud Firestore (Start in Test Mode).

Create a .env file in the root directory and add your keys:

VITE_API_KEY=your_api_key
VITE_AUTH_DOMAIN=your_project.firebaseapp.com
VITE_PROJECT_ID=your_project_id



Run the App

npm run dev



📂 Project Structure

/src
├── components/
│   ├── LoginScreen.jsx    # Landing page & Auth handler
│   └── ChatRoom.jsx       # Main chat interface & logic
├── App.jsx                # Route management & state init
├── main.jsx               # Entry point
└── index.css              # Tailwind imports



🧠 How It Works (Technical Concept)

This project avoids the complexity of setting up a dedicated WebSocket server (like Socket.io) by leveraging Firestore's Real-time SDK.

The Listener: The app attaches a listener to the global_chat collection in the NoSQL database.

The Trigger: Whenever a document is added to this collection, Firebase triggers the listener.

The Update: React state is updated immediately with the new payload, causing a re-render of the message list.

This architecture ensures O(1) complexity for message retrieval on the client side during active sessions.

🤝 Contributing

Contributions are welcome!

Fork the Project

Create your Feature Branch (git checkout -b feature/AmazingFeature)

Commit your Changes (git commit -m 'Add some AmazingFeature')

Push to the Branch (git push origin feature/AmazingFeature)

Open a Pull Request

👤 Author

$$Maulik Sharma$$

GitHub: @adonisoncode

LinkedIn: www.linkedin.com/in/maulik-sharma-02a22b21a

Made for CSE Minor Project
