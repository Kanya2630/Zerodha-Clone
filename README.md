# Zerodha Clone

A full-stack Zerodha-like trading dashboard built for learning and portfolio/demo use.  
This repository contains both the **frontend** (React) and **backend** (Node/Express) plus instructions to run locally and deploy.

---

## Table of Contents
1. [Project Overview](#project-overview)  
2. [Features](#features)  
3. [Tech Stack](#tech-stack)  
4. [Folder Structure](#folder-structure)  
5. [Prerequisites](#prerequisites)  
6. [Environment Variables](#environment-variables)  
7. [Install & Run (Development)](#install--run-development)  
8. [Build & Run (Production)](#build--run-production)  
9. [Deploying](#deploying)  
10. [Common Issues & Fixes](#common-issues--fixes)  
11. [API Endpoints (examples)](#api-endpoints-examples)  
12. [Contributing](#contributing)  
13. [License](#license)

---

## Project Overview
This project replicates a simplified Zerodha UI + backend for demonstration and learning. It includes:
- Market watch/quotes
- Order placement simulation (demo mode)
- Portfolio / holdings view
- Historical price charts (mock or real-market API)
- Authentication (basic or mock)

> ⚠️ **This is a demo/learning project.** Do NOT use it with real money or real trading accounts unless you fully implement and secure a real broker integration.

---

## Features
- Responsive trading dashboard (React)
- REST API server (Node + Express)
- Demo simulated order flow (buy/sell)
- Portfolio/holdings management (MongoDB)
- Websocket-like updates (polling or socket) for live-like quotes
- Simple auth (JWT or session-based) — optional

---

## Tech Stack
- Frontend: React (Vite or Create React App), React Router, Axios
- Backend: Node.js, Express, Mongoose (MongoDB)
- Database: MongoDB (Atlas or local)
- Dev tools: nodemon, concurrently (optional)
- Optional: Socket.IO for realtime updates

---

## Folder Structure

---

## Prerequisites
- Node.js (v18+ recommended)
- npm or yarn
- MongoDB (Atlas or local)
- (Optional) An API key for market data if you plan to use real quotes

---

## Environment Variables

Create `.env` files in `backend/` and `frontend/` (if needed).

### backend/.env
PORT=3002
MONGO_URI=mongodb+srv://USER:PASSWORD@cluster0.mongodb.net/zerodha-demo?retryWrites=true&w=majority
JWT_SECRET=your_jwt_secret_here
MARKET_API_KEY=your_market_data_api_key_or_empty
CLIENT_URL=http://localhost:3000


> Replace values above with your credentials. Never commit real secrets.

---

## Install & Run (Development)

### Option A — Run frontend and backend separately (recommended)
**Backend**
```bash
cd backend
npm install
# for dev with auto-reload
npx nodemon server.js     # or "npm run dev" if script exists
