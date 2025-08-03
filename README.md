# CodeClash
CodeClash is a full-stack online coding platform built for practicing algorithmic problems, competing in timed contests, and engaging with a vibrant developer community. Designed with a modern micro-services architecture, it delivers secure code execution, real-time collaboration, and AI-assisted productivity.

🚀 Features
Secure Authentication – Login/signup with session-based authentication.

Practice Problems – Search, filter, and solve problems using a built-in Monaco code editor.

Live Contests – Real-time leaderboard, submissions, scoring, and ranking.

Secure Code Execution – Isolated Docker-based compiler server supporting C++, Java, Python.

AI Assistance – Google Gemini-powered code review and debugging suggestions.

Developer Community – Discussion boards for problems and contests.

Admin Dashboard – Create/edit problems and contests, manage users.

Profile & Stats – View submissions, track contest performance and history.

📁 Project Structure
CodeClash/
├── Backend/             # Node.js/Express REST API
│   ├── app.js
│   ├── Models/
│   ├── Controller/
│   ├── Routes/
│   └── ...
├── Compiler Server/     # Dockerized code execution service
│   ├── execute{Lang}.js
│   ├── Dockerfile
│   └── ...
└── Frontend/            # React (Vite) single-page app
    ├── src/components/
    ├── src/AppRoutes.jsx
    └── ...

🛠️ Tech Stack
Layer	Technologies
Frontend	React, Vite, MUI, React Router, Monaco Editor
Backend	Node.js, Express, MongoDB, Passport, Joi, Sessions
Compiler	Node.js, Docker, Language-specific runners
AI Integration	Google Gemini API
Security	Helmet, CORS, Rate Limiting

⚙️ Setup & Installation
Clone the Repository
git clone <your-repo-url>
cd CodeClash


Create .env Files

Backend/.env
PORT=
MONGOOSE_URL=
FRONTEND_URL=
COMPILER_URL=
Gemini_api=
SESSION_SECRET=


Compiler Server/.env

PORT=

Install Dependencies

bash
cd Backend && npm install
cd ../Compiler\ Server && npm install
cd ../Frontend && npm install


Run Servers

bash
# Backend
cd Backend
npm run dev

# Compiler Server (Docker recommended)
cd ../Compiler\ Server
docker build -t codeclash-compiler .
docker run -p <host-port>:<container-port> codeclash-compiler
# or
npm start

# Frontend
cd ../Frontend
npm run dev

📌 Core Functionality
Problem Solving – Editor with run/submit, verdicts, and AI debugging.

Contests – Timed events with leaderboards and submission tracking.

Leaderboard – Rank by total points and earliest accepted submission.

Admin – Problem/contest management tools.

AI Tools – Smart review and assistance for submitted code.

🤝 Contributing
Fork the repository.

Create a new branch.

Commit your changes.

Open a pull request with a clear description.

📄 License
Released under the MIT License.

Level up your coding skills with CodeClash! 🔥
