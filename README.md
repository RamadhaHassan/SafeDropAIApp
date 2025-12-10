SafeDropAiApp

Smart identity and risk screening for digital deliveries

Overview

SafeDropAiApp protects riders and SMEs from unsafe anonymous buyers. It verifies buyers before dispatch and creates a secure case log for investigators.

Users

Phone shops

Independent riders

Delivery services

Safety teams

Key Features

Face match check

Phone trust check

Delivery location risk scan

Order keyword alerts

Automatic risk score

Dispatch block for risky orders

Rider arrival timer

Rider panic alert

Secure case log export

How It Works

Order arrives via WhatsApp or web form

System sends secure verification link

Buyer uploads selfie and confirms location

AI checks identity and behavior

Seller views risk score

Rider receives safety status

Logs stored for case support

System Diagram
Buyer → SafeDrop Form
       ↓
FastAPI backend → Face + phone + message scan
       ↓
Risk score → Secure database
       ↓
Seller dashboard → Approve or block
       ↓
Rider timer + panic alert
       ↓
Case log for investigators

Tech Stack

Python

FastAPI

n8n automation

Face match model

Phone intelligence API

WhatsApp Cloud API

PostgreSQL

Docker + Docker Compose

Encrypted storage

Folder Structure
SafeDropAiApp/
│
├─ backend/       # FastAPI server
│   ├─ controllers/
│   ├─ routes/
│   ├─ models/
│   ├─ utils/
│   ├─ requirements.txt
│   └─ server.py
├─ frontend/      # React or other frontend framework
│   ├─ src/
│   │   ├─ components/
│   │   ├─ pages/
│   │   └─ App.js
│   └─ package.json
├─ models/        # AI models for face match, liveness, and scoring
├─ docs/          # Setup notes, flow diagrams, guides
├─ .env.example   # Example environment variables
├─ docker-compose.yml
└─ README.md

Installation
Requirements

Python 3.10+

Node.js 18+

npm or yarn

Docker + Docker Compose

Git

Local Setup

Clone the repository:

git clone https://github.com/RamadhaHassan/SafeDropAiApp.git
cd SafeDropAiApp


Copy .env.example to .env and fill values:

cp .env.example .env


Example .env values:
backend/.env

PORT=5000
DB_URL=your_database_url
SECRET_KEY=your_secret_key


frontend/.env

REACT_APP_API_URL=http://localhost:5000


Install dependencies

cd backend
pip install -r requirements.txt
cd ../frontend
npm install


Start servers
Backend

cd ../backend
uvicorn server:app --reload


Frontend

cd ../frontend
npm start


App runs at http://localhost:3000.

Docker Setup (Optional)
docker compose up --build


Make sure docker-compose.yml defines backend, frontend, and database services.

Vercel Deployment

Sign in to Vercel

Connect GitHub repo SafeDropAiApp

Set environment variables in Vercel

Configure build commands (frontend: npm install && npm run build, backend if needed)

Deploy

Updating Project
git add .
git commit -m "Update project"
git push origin main


Vercel auto-deploys updates.

License

MIT License 2025

Contact

Owner: Ramadha Hassan

Email: ramadhanabdullahi@gmail.com

GitHub: github.com/RamadhaHassan

Project: SafeDropAiApp
