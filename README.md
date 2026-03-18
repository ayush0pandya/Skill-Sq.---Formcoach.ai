# Skill² — Formcoach.ai

> AI-powered real-time workplace training platform

![Python](https://img.shields.io/badge/Python-3.11-blue)
![FastAPI](https://img.shields.io/badge/FastAPI-0.135-green)
![React](https://img.shields.io/badge/React-19-cyan)
![Claude AI](https://img.shields.io/badge/Claude-AI-orange)

---

## 🏗️ What is Skill²?

Skill² is a real-time AI coaching platform built to revolutionize workplace skills training. Using a camera, workers can train anywhere while employers track progress against standard operating procedures (SOPs).

The system watches a worker's body movements in real time, scores their form, and delivers instant voice coaching — like having a personal trainer on the job site.

---

## 🎯 The Problem

Every year, thousands of workers are injured due to improper technique — lifting boxes wrong, poor posture, unsafe movements. Traditional training is expensive, inconsistent, and hard to scale.

Skill² solves this with AI.

---

## ✨ Features

- 🎥 **Real-time pose detection** — MediaPipe tracks 11 joint angles at 30fps
- 🤖 **AI coaching** — Claude AI analyzes form and delivers personalized feedback
- 🗣️ **Voice feedback** — Coach speaks corrections aloud, no screen needed
- 📊 **Session tracking** — Every rep scored and stored
- ✦ **Skill certification** — Workers earn verified certificates after completing programs
- 🏢 **Organization dashboard** — Employers track workforce progress and create custom training programs
- 📋 **SOP to training program** — Upload any training manual and Claude AI auto-generates a structured program

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React 19, Vite |
| Backend | FastAPI, Python |
| AI Coaching | Anthropic Claude API |
| Pose Detection | MediaPipe |
| Computer Vision | OpenCV |
| Database | SQLite |
| Auth | API Key based |

---

## 🚀 Getting Started

### Backend
```bash
cd skill2-backend
python -m venv venv
venv\Scripts\activate        # Windows
pip install -r requirements.txt
echo ANTHROPIC_API_KEY=your-key > .env
uvicorn main:app --reload
```

### Frontend
```bash
cd skill2-frontend
npm install
npm run dev
```

---

## 📡 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/video` | Live camera stream |
| GET | `/angles` | Current joint angles JSON |
| POST | `/coach` | Get AI coaching tip |
| POST | `/evaluate` | Evaluate a pose |
| POST | `/sessions/start` | Start training session |
| POST | `/sessions/{id}/end` | End session |
| POST | `/sessions/{id}/debrief` | Get AI session debrief |
| GET | `/health` | Server health check |

---

## 👥 Team

Built at Cornell Hackathon 2026
1) Ayush Pandya (me)
2) Ye Lin
3) Weiqi Han
4) Emma
5) Christy Cheung 
---

## 📄 License

MIT
