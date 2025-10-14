<div align="center">

# TISD — Tracking Innovation & Sustainable Development

[![Platform](https://img.shields.io/badge/Platform-Online-6c5ce7?style=for-the-badge&logo=github&logoColor=white)](https://github.com/gavin100305/SEA_TISD_GavinSoares_10223)
[![CRCE](https://img.shields.io/badge/CRCE-Computer%20Engineering-4ecdc4?style=for-the-badge&logo=university)](https://github.com/gavin100305/SEA_TISD_GavinSoares_10223)
[![Full Stack](https://img.shields.io/badge/Full%20Stack-Development-95e1d3?style=for-the-badge&logo=stackshare)](https://github.com/gavin100305/SEA_TISD_GavinSoares_10223)

**Full Stack Web Platform for Project Documentation, Collaboration & SDG Monitoring**

[Video Demo](https://drive.google.com/file/d/1o5ImbNLncLn5QnEmz6RTGGksLdejhNtM/view?usp=drive_link) • [Presentation](https://drive.google.com/file/d/1m1CsQIu3UkefCNPSk1NJn_JBPbWSdz6P/view?usp=drive_link)

</div>

---

## Technology Stack

<div align="center">

![React](https://img.shields.io/badge/React-18.x-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Django](https://img.shields.io/badge/Django-Python-092E20?style=for-the-badge&logo=django&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind-CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-Database-003B57?style=for-the-badge&logo=sqlite&logoColor=white)
![Gemini AI](https://img.shields.io/badge/Gemini-API-8E75B2?style=for-the-badge&logo=google&logoColor=white)
![Chart.js](https://img.shields.io/badge/Chart.js-Visualization-FF6384?style=for-the-badge&logo=chartdotjs&logoColor=white)

</div>

## Overview

TISD (Tracking Innovation & Sustainable Development) is a comprehensive web-based platform developed as part of the Full Stack Development course at Fr. Conceicao Rodrigues College of Engineering (Computer Engineering, Sem 4). The platform systematically tracks student projects, promotes SDG alignment, and facilitates collaboration among students, faculty, NGOs, and industry mentors.

Repository structure (high level):

```
SEA_TISD_GavinSoares_10223/
├── backend/        # Django API, models, and business logic
├── frontend/       # React + Tailwind UI components
└── README.md       # <-- you are here
```

### Key Features

- Systematic project tracking across departments and academic years
- SDG (Sustainable Development Goals) alignment and impact analysis
- Intelligent mentor-student-collaborator matching system
- Real-time progress monitoring and institutional insights
- Advanced analytics powered by Gemini API
- Collaboration tools with meeting scheduler and notifications

## User Roles & Capabilities

### 🌍 1. Viewers (Public, NGOs, Industry Experts)

- Explore academic projects categorized by department, year, and SDG goals
- View project details, mentors, student teams, and collaborators
- Filter projects by SDG, department, and project status
- Add comments and testimonials on projects
- Express interest in mentoring or collaborating

### 👨‍🎓 2. Students (Project Teams / Innovators)

- Create and manage personal or group projects
- Upload descriptions, objectives, deliverables, reports, PPTs, and demo videos
- Map projects to relevant SDGs
- Connect with faculty mentors and external collaborators
- Track progress and receive mentor feedback
- Use meeting scheduler for check-ins
- Collaborate using the collaborator connect system
- Receive automated reminders and mentor updates
- View project analytics, SDG contribution, and performance insights
- Full search and filter support across platform

### 👩‍🏫 3. Faculty (Project Guides / TISD Coordinators)

- Add, review, and mentor student projects
- Map projects to relevant SDGs and academic objectives
- Connect with NGOs and industry experts for real-world guidance
- View collaborator activities with mentees
- Send feedback and reminders via email
- Participate in scheduled meetings with students and collaborators

### 🔧 4. Admins (College Moderators / Incubation Cell)

- Approve, edit, and manage projects, users, and collaborators
- Generate advanced reports using Gemini API (SDG impact charts, department analytics, participation trends)
- View data visualizations and charts
- Monitor registered users and activities
- Moderate testimonials and comments
- Track mentor-student-collaborator engagements
- Send platform-wide notifications and updates

### 📊 5. Management (Institutional Heads / Accreditation Bodies)

- Access macro-level insights on project innovation trends and SDG impact
- Track mentor-student engagement metrics
- Evaluate departmental performance and sustainability focus
- Download institutional reports for audits and accreditations

## Core Functional Requirements

- **Project Creation & Management** — Complete CRUD operations with file uploads
- **SDG Mapping & Impact Analysis** — Align projects with UN Sustainable Development Goals
- **Mentorship System** — Faculty and collaborator matching with students
- **NGO/Industry Collaboration** — External partnership module
- **Smart Charts & Reports** — Gemini API-powered analytics
- **Meeting Scheduler** — Integrated calendar for mentor-student meetings
- **Commenting & Testimonials** — Community feedback system
- **Advanced Search & Filters** — Comprehensive filtering across all sections
- **Role-Based Access Control** — Secure, permission-based access
- **Email Notifications** — Automated updates via Nodemailer
- **Real-Time Progress Tracking** — Live project status monitoring

## Quick Start

These instructions will get a local copy running for development and testing.

### Prerequisites

- Python ≥ 3.8
- Node.js ≥ 16 and npm
- SQLite3 (bundled with Django)
- Gemini API Key
- GitHub API Token
- SMTP credentials (for email notifications)

### Installation

1. **Clone the Repository**

```bash
git clone https://github.com/gavin100305/SEA_TISD_GavinSoares_10223.git
cd SEA_TISD_GavinSoares_10223
```

2. **Backend (Django)**

```bash
cd backend

# Create & activate virtual environment
python -m venv venv
source venv/bin/activate      # Linux/Mac
venv\Scripts\activate         # Windows

# Install dependencies
pip install -r requirements.txt

# Run migrations and collect static files
python manage.py migrate
python manage.py collectstatic

# Start the development server
python manage.py runserver
```

The backend server will run at `http://localhost:8000`

3. **Frontend (React)**

Open a new terminal and navigate to the frontend directory:

```bash
cd frontend

# Install dependencies
npm install

# Start the development server
npm run dev
```

The frontend will run at `http://localhost:5173` (default Vite port)

### Environment Configuration

Create a `.env` file in the `backend/` directory with the following variables:

```
# Django Settings
SECRET_KEY=your_django_secret_key
DEBUG=True

# Gemini API
GEMINI_API_KEY=your_gemini_api_key

# GitHub API
GITHUB_TOKEN=your_github_token

# Email Configuration (SMTP)
EMAIL_HOST=smtp.gmail.com
EMAIL_PORT=587
EMAIL_HOST_USER=your_email@gmail.com
EMAIL_HOST_PASSWORD=your_app_password
EMAIL_USE_TLS=True
```

## API Endpoints (selected)

Below are common endpoints. Consult the Django `urls.py` files for the complete list.

**Authentication & Users:**

```
POST /api/auth/register/
POST /api/auth/login/
GET  /api/auth/profile/
```

**Project Management:**

```
GET  /api/projects/          # list all projects
POST /api/projects/          # create project
GET  /api/projects/:id/      # read project
PUT  /api/projects/:id/      # update project
DELETE /api/projects/:id/    # delete project
```

**Collaboration & Mentorship:**

```
GET  /api/mentors/           # list mentors
POST /api/meetings/          # schedule meeting
GET  /api/testimonials/      # view testimonials
POST /api/testimonials/      # add testimonial
```

**Analytics:**

```
GET  /api/analytics/sdg/     # SDG impact reports
GET  /api/analytics/dept/    # department-wise analytics
POST /api/reports/generate/  # generate AI-powered reports
```

## Project Details & Notable Files

- `backend/manage.py` — Django management script
- `backend/tisd/` — Main Django app with models, views, and serializers
- `backend/requirements.txt` — Python dependencies
- `frontend/src/` — React components and pages
- `frontend/src/components/` — Reusable UI components
- `frontend/src/pages/` — Main application pages
- `frontend/public/` — Static assets

## Running Tests

```bash
# Backend tests
cd backend
python manage.py test

# Frontend tests (if configured)
cd frontend
npm test
```

## Deployment

**Backend:** Deploy to platforms like Railway, Render, Heroku, or PythonAnywhere. Configure environment variables and use Gunicorn for production:

```bash
pip install gunicorn
gunicorn tisd.wsgi:application
```

**Frontend:** Deploy to Vercel, Netlify, or any static hosting service:

```bash
npm run build
# Deploy the 'dist' folder
```

## Next Steps (Suggested)

- Add comprehensive API documentation (Swagger/OpenAPI)
- Implement CI/CD pipeline with GitHub Actions
- Add unit and integration tests
- Set up production database (PostgreSQL)
- Configure CDN for static file serving
- Implement caching strategy (Redis)

## Support

For support or questions, open an issue in this repository or contact the development team.

---

## 👥 Development Team

**Built with ❤️ for Full Stack Development Course at CRCE**

**Team Members:**
- **Gavin Soares** - [GitHub](https://github.com/gavin100305)
- **Ankit Kumar** - [GitHub](https://github.com/ankit935686)
- **Alok Sinha** - [GitHub](https://github.com/aloksinha123)

<div align="center">

---

[![GitHub Stars](https://img.shields.io/github/stars/gavin100305/SEA_TISD_GavinSoares_10223?style=social)](https://github.com/gavin100305/SEA_TISD_GavinSoares_10223/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/gavin100305/SEA_TISD_GavinSoares_10223?style=social)](https://github.com/gavin100305/SEA_TISD_GavinSoares_10223/network/members)

**Making Innovation Trackable, Sustainable, and Collaborative**

</div>
