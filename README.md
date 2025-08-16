StockRadar

A modern, full-stack web app for tracking stocks in real time with beautiful charts, watchlists, and a simple portfolio tracker.

Table of Contents

Project Intro

Tech Stack

Features

Screenshots

Project Structure

Quick Start

Backend Setup

Frontend Setup

Environment Variables

Available Scripts

API (Starter)

Contributing

Roadmap

License

Contact

Project Intro

StockRadar helps you monitor stocks quickly and intelligently. It provides real‑time-ish* prices, interactive charts, a watchlist, and a lightweight portfolio tracker with authentication.

*Real-time depends on the chosen data provider and plan; demo mode may simulate or use delayed quotes.

Tech Stack

Frontend: React + Vite, Tailwind CSS, (optional) Recharts/Chart.js, Zustand/Redux (TBD)

Backend: Node.js, Express, MongoDB (Mongoose), JWT Auth, CORS, dotenv

Tooling: ESLint, Prettier, GitHub Actions (optional), Husky (optional)

Features

Live/near real-time price updates (provider TBD)

Interactive charts with multiple timeframes

Watchlist with quick add/remove

Portfolio tracker (holdings, avg cost, P/L)

Authentication (register/login with JWT)

Search by symbol/name, recent history

Dark/light theme, responsive UI

Screenshots

Add screenshots to docs/images/ and reference them below.

stockradar/
  docs/
    images/
      dashboard.png
      watchlist.png

Example:



Project Structure

stockradar/
├─ backend/
│  ├─ src/
│  │  ├─ routes/
│  │  ├─ controllers/
│  │  ├─ models/
│  │  └─ utils/
│  ├─ server.js
│  ├─ package.json
│  └─ .env.example
├─ frontend/
│  └─ vite-project/
│     ├─ index.html
│     ├─ src/
│     │  ├─ App.jsx
│     │  ├─ components/
│     │  └─ index.css
│     ├─ package.json
│     └─ .env.example
├─ docs/
│  └─ images/
├─ README.md
└─ LICENSE

Quick Start

Clone the repository and move into it:

git clone https://github.com/vanshshah2924/stockradar.git
cd stockradar

Backend Setup

cd backend
cp .env.example .env   # on Windows: copy .env.example .env
npm install
npm run dev            # if using nodemon, else: node server.js

Backend runs by default on http://localhost:5000.

Frontend Setup

Open a new terminal:

cd frontend/vite-project
cp .env.example .env   # on Windows: copy .env.example .env
npm install
npm run dev

Frontend starts on http://localhost:5173 (or next available port shown in the console).

Environment Variables

Create .env files based on examples and fill real values.

backend/.env.example

PORT=5000
MONGO_URI=mongodb+srv://<user>:<pass>@<cluster>/<db>?retryWrites=true&w=majority
JWT_SECRET=replace-with-strong-secret
CORS_ORIGIN=http://localhost:5173

frontend/vite-project/.env.example

VITE_API_URL=http://localhost:5000
VITE_APP_NAME=StockRadar

Available Scripts

Backend (/backend)

npm run dev – start with nodemon (hot reload)

npm start – start with Node

npm test – run backend tests (if configured)

Frontend (/frontend/vite-project)

npm run dev – start Vite dev server

npm run build – production build

npm run preview – preview production build locally

API (Starter)

Initial example endpoints (expand as you build):

GET /health → { status: "OK" }

POST /api/auth/register → create user

POST /api/auth/login → get JWT

GET /api/stocks/:symbol → stock details/quotes

GET /api/portfolio → user portfolio (auth required)

Contributing

Create a feature branch from dev: feat/<short-name>

Commit using Conventional Commits: feat:, fix:, chore:

Push branch → Open PR into dev

Request review → Merge → Delete branch (local + remote)

Roadmap

Data provider integration (decide source)

Alerts & notifications

Import/export portfolio (CSV)

Unit & integration tests

CI/CD and deployment

License

MIT © 

Contact

Vansh Shah –  · Portfolio: https://codebyvansh.example · GitHub Issues welcome

