# HRMS Lite

A lightweight Human Resource Management System for managing employees and attendance.

## Tech Stack
- **Frontend**: React, Vite, Tailwind CSS, Axios
- **Backend**: FastAPI, SQLAlchemy, Pydantic, SQLite (Dev) / PostgreSQL (Prod)
- **Database**: SQLite (default)

## Project Structure
- `frontend/`: React application
- `backend/`: FastAPI application

## Running Locally

### Prerequisites
- Node.js & npm
- Python 3.8+

### Steps
1. **Clone/Download** the repository.
2. **Backend Setup**:
   ```bash
   cd backend
   python -m venv venv
   # Windows
   .\venv\Scripts\activate
   # Mac/Linux
   source venv/bin/activate
   
   pip install -r requirements.txt
   uvicorn main:app --reload
   ```
   Backend will run at `http://localhost:8000`.

3. **Frontend Setup**:
   ```bash
   cd frontend
   npm install
   npm run dev
   ```
   Frontend will run at `http://localhost:5173`.

## Deployment

### Frontend (Vercel/Netlify)
- storage: git repo
- framework preset: Vite
- build command: `npm run build`
- output directory: `dist`

### Backend (Render/Railway/Heroku)
- runtime: Python 3
- build command: `pip install -r requirements.txt`
- start command: `uvicorn main:app --host 0.0.0.0 --port 10000` (or $PORT)

## Assumptions
- No authentication required (Admin only).
- SQLite used for simplicity; meant for demo/local use.
