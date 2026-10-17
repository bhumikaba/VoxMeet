## 🎥 VoxMeet — Real-Time Video Conferencing Platform

Connect Beyond Boundaries. Communicate Without Limits.

VoxMeet is a full-stack video conferencing web application designed to make online communication simple, interactive, and accessible. Built using the MERN stack, WebRTC, and Socket.IO, VoxMeet brings users together through real-time video communication, instant messaging, and meeting history management.

Whether connecting with friends, collaborating with teammates, or catching up with loved ones, VoxMeet provides a unified platform for seamless virtual communication.

## ✨ Key Features

🔐 User Authentication — Register and log in with username and password authentication, with passwords securely hashed using bcrypt.

🎥 Real-Time Video Conferencing — Connect with multiple participants through browser-based video communication powered by WebRTC.

🎙️ Audio and Video Controls — Manage microphone and camera access during meetings.

🖥️ Screen Sharing — Share your screen during a meeting using browser media-sharing capabilities.

💬 Live Chat — Exchange messages with participants in real time using Socket.IO.

🔗 Meeting Rooms — Join a meeting using a meeting code and communicate with participants in the same room.

📜 Meeting History — Save and retrieve previous meeting codes and timestamps.

👤 Guest Access — Enter the meeting interface without registering an account.

📱 Interactive User Interface — Navigate through the landing page, authentication screens, meeting interface, and history page.

⚡ Real-Time Event Handling — Handle participant connections, signaling messages, chat events, and disconnections.

🛠️ Technology Stack

## Frontend

React.js — Component-based user interface development

JavaScript (ES6+) — Application logic and interactivity

HTML5 & CSS3 — Page structure and styling

Material UI (MUI) — Interface components and icons

React Router DOM — Client-side navigation

Axios — HTTP requests to backend APIs

Socket.IO Client — Real-time communication with the server

## Backend

Node.js — JavaScript runtime

Express.js — REST API development and request handling

Socket.IO — Real-time messaging and WebRTC signaling

MongoDB — Persistent storage for user and meeting-history records

Mongoose — MongoDB object modeling

bcrypt — Password hashing and verification

Node.js Crypto module — Generation of random authentication tokens

CORS — Cross-origin request configuration

Real-Time Communication

WebRTC — Peer-to-peer audio and video communication

Socket.IO — Signaling, chat messaging, and participant events

STUN — Assists peers in discovering network addresses for connection establishment

Development Tools

Visual Studio Code

Git and GitHub

npm

Postman — API testing

MongoDB Atlas — Cloud database hosting, when configured

## 🏗️ System Architecture

VoxMeet follows a client-server architecture with a real-time communication layer.

                 ┌────────────────────────┐
                 │       React UI         │
                 │  Pages and Components  │
                 └────────────┬───────────┘
                              │
                 ┌────────────▼───────────┐
                 │   Axios / REST APIs    │
                 │   Express + Node.js    │
                 └────────────┬───────────┘
                              │
                 ┌────────────▼───────────┐
                 │        MongoDB         │
                 │ Users and Meeting Logs │
                 └────────────────────────┘

                 ┌────────────────────────┐
                 │    Socket.IO Server    │
                 │ Signaling and Chat     │
                 └────────────┬───────────┘
                              │
                    WebRTC Connection Setup
                              │
                 ┌────────────▼───────────┐
                 │ Audio / Video Streams  │
                 │     Between Peers      │
                 └────────────────────────┘

## How It Works

Users open VoxMeet and register or log in.
The frontend sends authentication requests to the Express backend.
The backend validates credentials and stores user information in MongoDB.
Users enter a meeting room using a meeting code.
Socket.IO coordinates participant discovery and WebRTC signaling.
WebRTC establishes media connections between participants when network conditions allow.
Socket.IO distributes chat messages and participant events.

Meeting codes and timestamps can be stored and retrieved through the meeting-history APIs.

