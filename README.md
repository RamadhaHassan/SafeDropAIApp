# SafeDropAIApp
Smart identity and risk screening for digital deliveries

## Overview
SafeDropAIApp protects riders and small businesses from unsafe anonymous buyers. It verifies buyers before dispatch and creates a secure case log for investigators when incidents happen.

## Users
- Phone shops
- Independent riders
- Delivery services
- Safety teams

## Key Features
- Face match check  
- Phone trust check  
- Delivery location risk scan  
- Order keyword alerts  
- Automatic risk score  
- Dispatch block for risky orders  
- Rider arrival timer  
- Rider panic alert  
- Secure case log export  

## How It Works
1. Seller receives an order
2. System sends a secure verification link to the buyer
3. Buyer uploads a selfie and confirms location
4. AI checks identity, device signals, and message behaviour
5. Seller views the risk score
6. Rider receives safety status
7. All logs are saved for future case support

### System Diagram (Text)
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

markdown
Copy code

## Tech Stack
- Python  
- FastAPI  
- n8n automation  
- Face match model  
- Phone intelligence API  
- WhatsApp Cloud API  
- PostgreSQL  
- Docker + Docker Compose  
- Encrypted storage  

## Folder Structure
SafeDropAIApp/
│
├─ backend/
│ ├─ controllers/
│ ├─ routes/
│ ├─ models/
│ ├─ utils/
│ ├─ requirements.txt
│ └─ server.py
├─ frontend/
│ ├─ src/
│ │ ├─ components/
│ │ ├─ pages/
│ │ └─ App.js
│ └─ package.json
├─ models/
├─ docs/
├─ .env.example
├─ docker-compose.yml
└─ README.md

markdown
Copy code

## Installation

### Requirements
- Python 3.10+
- Node.js 18+
- npm or yarn
- Docker + Docker Compose
- Git

### Local Setup
Clone the repository:
```bash
git clone https://github.com/RamadhaHassan/SafeDropAIApp.git
cd SafeDropAIApp
Copy environment variables:

bash
Copy code
cp .env.example .env
Install dependencies:

Backend:

bash
Copy code
cd backend
pip install -r requirements.txt
Frontend:

bash
Copy code
cd ../frontend
npm install
Start development servers:

Backend:

bash
Copy code
cd ../backend
uvicorn server:app --reload
Frontend:

bash
Copy code
cd ../frontend
npm start
Docker Setup
bash
Copy code
docker compose up --build
