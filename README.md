# SafeDropAiApp
Smart identity and risk screening for digital deliveries

## Status
Python | License: MIT

## Overview
SafeDropAiApp protects riders and SMEs from unsafe anonymous buyers. It verifies buyers before dispatch and creates a secure case log for investigators.

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
1. Order arrives via WhatsApp or web form  
2. System sends secure verification link  
3. Buyer uploads selfie and confirms location  
4. AI checks identity and behavior  
5. Seller views risk score  
6. Rider receives safety status  
7. Logs stored for case support  

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

## Installation

### Requirements
- Python 3.10+  
- Docker + Docker Compose  
- Git  

### Setup
```bash
git clone https://github.com/RamadhaHassan/SafeDropAiApp.git
cd SafeDropAiApp
cp .env.example .env
docker compose up --build
License
MIT License 2025

Contact
Owner: Ramadha Hassan

Email: ramadhanabdullahi@gmail.com

GitHub: github.com/RamadhaHassan

Project: SafeDropAiApp
