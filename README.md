# ku-isonga-dhs
KU ISONGA Digital Health Solutions — AI-powered chronic care coordination  platform connecting patients and healthcare providers. "Care that follows you."

# KU ISONGA Digital Health Solutions
> "Care that follows you."

## Overview
KU ISONGA DHS is a technology-driven healthcare coordination platform designed to
improve communication, continuity of care, and operational efficiency between patients
and local healthcare facilities.

## Problem
> Missed appointments due to paper-based follow-up instructions.
> Poor communication between healthcare providers and patients.
> Lack of reliable channels for healthcare information.
> Difficulty locating appropriate facilities when relocating or traveling.
> Limited mechanisms for patient feedback.

## Solution
## Core Functions

### 1. Clinician-Assigned Care Reminders
Doctors assign appointments, medication schedules, and follow-up instructions 
directly through a web-based clinic dashboard. Patients receive automated 
reminders via the mobile app or SMS — ensuring no follow-up is missed.

### 2. Continuity-of-Care Facility Locator
Patients can search and locate nearby healthcare facilities equipped to manage 
their specific chronic condition when they travel or relocate — so care never 
stops, regardless of location.

### 3. Patient Feedback & Information Channel
Patients submit service feedback through the app. Facilities access aggregated, 
AI-analyzed insights on their dashboard — turning patient voices into actionable 
service improvements.

### 4. AI-Powered Health Coordination
- **Missed Appointment Prediction** — Flags at-risk patients and triggers 
  proactive reminders before visits are missed.
- **Smart Reminder Optimization** — Personalizes reminder timing based on 
  each patient's response patterns.
- **Feedback Intelligence** — Automatically identifies recurring service 
  issues from patient feedback using natural language analysis.

> AI outputs assist healthcare staff in decision-making — without replacing 
> clinical judgment.

## Tech Stack
- Frontend: Next.js
- Mobile: Flutter
- Backend: Node.js / Express
- AI: Python / FastAPI
- Database: PostgreSQL

## Project Structure
ku-isonga-dhs/
```bash
│
├── apps/
│   ├── web/                  # Next.js — Provider Dashboard
│   │   ├── app/
│   │   ├── components/
│   │   └── package.json
│   │
│   ├── mobile/               # Flutter — Patient App
│   │   ├── lib/
│   │   ├── android/
│   │   ├── ios/
│   │   └── pubspec.yaml
│   │
│   └── ai/                   # Python FastAPI — AI Module
│       ├── models/
│       ├── routes/
│       ├── services/
│       └── requirements.txt
│
├── backend/                  # Node.js / Express — Core API
│   ├── src/
│   │   ├── routes/
│   │   ├── controllers/
│   │   ├── models/
│   │   ├── middleware/
│   │   └── services/
│   ├── prisma/               # Database schema
│   └── package.json
│
├── docs/                     # Documentation
│   ├── architecture.md
│   ├── api-reference.md
│   └── KU_ISONGA_DHS.pdf
│
├── .github/
│   └── PULL_REQUEST_TEMPLATE.md
│
├── .gitignore
├── README.md
└── docker-compose.yml        # Optional, for running everything locally
```

## Getting Started

### Prerequisites
Make sure you have the following installed on your machine:

- [Node.js](https://nodejs.org/) v18+
- [Python](https://www.python.org/) 3.10+
- [Flutter](https://flutter.dev/docs/get-started/install) 3.0+
- [Git](https://git-scm.com/)
- [PostgreSQL](https://www.postgresql.org/) (or use Supabase)

---

### Installation

**1. Clone the repository**
```bash
git clone https://github.com/afyasync/ku-isonga-dhs.git
cd ku-isonga-dhs
```

**2. Backend (Node.js / Express)**
```bash
cd backend
npm install
cp .env.example .env        # Add your environment variables
npx prisma migrate dev      # Set up the database
```

**3. Frontend (Next.js)**
```bash
cd apps/web
npm install
cp .env.example .env.local  # Add your environment variables
```

**4. AI Module (Python / FastAPI)**
```bash
cd apps/ai
python -m venv venv
source venv/bin/activate    # Windows: venv\Scripts\activate
pip install -r requirements.txt
cp .env.example .env        # Add your environment variables
```

**5. Mobile App (Flutter)**
```bash
cd apps/mobile
flutter pub get
```

---

### Running Locally

**Backend**
```bash
cd backend
npm run dev
# Runs on http://localhost:5000
```

**Frontend**
```bash
cd apps/web
npm run dev
# Runs on http://localhost:3000
```

**AI Module**
```bash
cd apps/ai
source venv/bin/activate
uvicorn main:app --reload
# Runs on http://localhost:8000
```

**Mobile App**
```bash
cd apps/mobile
flutter run
# Launches on connected device or emulator
```

> 💡 **Tip:** Run each service in a separate terminal window.
> For a one-command setup, use `docker-compose up` (coming soon).

## Team
| Role | Name |
|------|------|
| Product Lead | Niyomwungeri Felicien |
| Technical Lead | Niyomugabo Fidele |
| Frontend Dev | Sangwamana Emeran |
| Mobile Dev | Niyomwungeri Felicien |
| AI / Backend | Team Devs |
| HS-Research & Communication Lead | Aisha Kaitu Koita |

## License
MIT
