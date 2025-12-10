SafeDropAI App
Smart identity and risk screening for digital deliveries
Status: Active
Python: 3.10+
License: MIT
Overview
SafeDropAI App protects riders and SMEs from unsafe anonymous buyers.
It verifies buyers before dispatch and creates a clean case record for investigators.
Users
Phone shops
Independent riders
Delivery services
Safety teams
Key Features
Face match check
Phone number trust score
Delivery location risk scan
Order message keyword alerts
Automatic risk score
Dispatch block for risky orders
Rider arrival timer
Panic alert
Case log export
How It Works
Order placed on WhatsApp or web form
App sends secure verification link
Buyer uploads selfie and location pin
AI checks identity signals
Seller views risk score
Rider gets safety status
Logs stored for follow-up when needed
System Diagram (Text)
Buyer → SafeDrop Form
↓
AI checks → Score → Dashboard
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
Docker and Docker Compose
Encrypted storage
Installation
Requirements
Python 3.10+
Docker and Docker Compose
Git
Setup
Copy code
Bash
git clone https://github.com/RamadhaHassan/safedropaiapp.git
cd safedropaiapp
cp .env.example .env
docker compose up --build
Test API
Copy code
Bash
curl -X POST http://localhost:8000/api/v1/verify \
-H "Content-Type: application/json" \
-d '{"phone":"+2547...","selfie_url":"https://","address":"Nairobi"}'
Expected output:
Risk score in JSON.
API Docs
When backend is running locally, open:
Copy code

http://localhost:8000/docs
Folder Structure
Copy code

safedropaiapp/
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
├── .env.example
├── README.md
├── app/
│   ├── main.py
│   ├── api/
│   │   └── v1/routes.py
│   ├── core/
│   │   └── config.py
│   ├── services/
│   │   ├── face_check.py
│   │   └── risk_score.py
│   ├── db/
│   ├── models/
│   ├── worker.py
│   └── tests/
└── ui/   (Frontend for Vercel)
