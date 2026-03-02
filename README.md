# KU ISONGA Digital Health Solutions
> *"Care that follows you."*

![Platform](https://img.shields.io/badge/Platform-Web%20%7C%20Mobile%20%7C%20AI-blue)
![Stack](https://img.shields.io/badge/Stack-Next.js%20%7C%20Node.js%20%7C%20Flutter%20%7C%20Python-green)
![Status](https://img.shields.io/badge/Status-MVP%20%2F%20Hackathon-orange)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

---

## Overview

**KU ISONGA DHS** is a technology-driven healthcare coordination platform designed to improve communication, continuity of care, and operational efficiency between patients and local healthcare facilities. The project focuses on improving information flow within healthcare systems, particularly for patients living with chronic diseases such as diabetes and hypertension.

The platform begins as a practical solution for chronic-care continuity, serving as a scalable foundation for future healthcare network coordination and population-level health intelligence.

---

## Problem Statement

Many healthcare systems face a gap between policy goals and real service delivery at local healthcare centers:

1. Missed appointments due to paper-based follow-up instructions.
2. Poor communication between healthcare providers and patients.
3. Lack of reliable channels for healthcare information.
4. Difficulty locating appropriate facilities when relocating or traveling.
5. Limited mechanisms for patient feedback.

These problems lead to treatment interruption, inefficient resource use, and reduced patient satisfaction — especially for chronic disease management.

---

## Core Functions

### 1. Clinician-Assigned Care Reminders
Doctors assign appointments, medication schedules, and follow-up instructions directly through a web-based clinic dashboard. Patients receive automated reminders via the mobile app or SMS — ensuring no follow-up is missed.

### 2. Continuity-of-Care Facility Locator
Patients can search and locate nearby healthcare facilities equipped to manage their specific chronic condition when they travel or relocate — so care never stops, regardless of location.

### 3. Patient Feedback & Information Channel
Patients submit service feedback through the app. Facilities access aggregated, AI-analyzed insights on their dashboard — turning patient voices into actionable service improvements.

### 4. AI-Powered Health Coordination
- **Missed Appointment Prediction** — Flags at-risk patients and triggers proactive reminders before visits are missed.
- **Smart Reminder Optimization** — Personalizes reminder timing based on each patient's response patterns.
- **Feedback Intelligence** — Automatically identifies recurring service issues from patient feedback using natural language analysis.

> 💡 AI outputs assist healthcare staff in decision-making — without replacing clinical judgment.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend (Provider Dashboard) | Next.js |
| Mobile (Patient App) | Flutter |
| Backend (Core API) | Node.js / Express |
| AI Module | Python / FastAPI |
| Database | PostgreSQL (via Supabase) |
| SMS Integration | Africa's Talking |
| AI Intelligence | Anthropic Claude API |

---

## Project Structure

```
ku-isonga-dhs/
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
│   ├── prisma/
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
└── docker-compose.yml
```

---

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

---

## Branch Strategy

```
main          → stable, demo-ready code only
develop       → integration branch (merge here first)
│
├── feat/web-dashboard      # Frontend dev
├── feat/mobile-app         # Flutter dev
├── feat/backend-api        # Backend dev
├── feat/ai-module          # AI dev
└── fix/[bug-name]          # Bug fixes
```

> ⚠️ Nobody pushes directly to `main`. All changes go through `develop` first via Pull Request.

---

## Team

| Role | Responsibility |
|---|---|
| Product Lead | Problem definition and system design |
| Technical Lead | Backend and AI integration |
| Frontend Developer | Next.js provider dashboard |
| Mobile Developer | Flutter patient app |
| Health Systems Research Lead | Workflow validation and user needs |
| Pitch & Communication Lead | Presentation and stakeholder narrative |

---

## Expected Impact

1. Reduced missed appointments
2. Improved treatment adherence
3. Better patient satisfaction
4. Enhanced operational decision-making for clinics
5. Early foundation for population health analytics

---

## Future Roadmap

1. Pilot testing with a local clinic
2. Collect real user feedback and refine workflows
3. Expand AI models using real operational data
4. Introduce referral coordination between facilities
5. Explore partnership with regional health stakeholders

---

## License

MIT © 2026 [AfyaSync](https://github.com/afyasync) — Kigali, Rwanda
