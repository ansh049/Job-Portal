# Job Portal

A full-stack job portal application for job seekers and employers. The app includes user authentication, job browsing, company management, job posting, applicant tracking, and profile handling.

## Tech Stack

- Frontend: React, Vite, Tailwind CSS, Redux Toolkit, React Router
- Backend: Node.js, Express, MongoDB, Mongoose
- Authentication: JWT and cookie-based session handling
- Media uploads: Cloudinary via Multer

## Features

- Job seeker sign up and login
- Browse jobs and view job details
- Apply to job listings
- Recruiter/company creation and company setup
- Post new jobs from an admin dashboard
- Review applicants for each job
- User profile management
- Modern responsive UI for desktop and mobile screens

## Project Structure

```text
jobportal-yt-main/
├─ backend/
│  ├─ controllers/
│  ├─ middlewares/
│  ├─ models/
│  ├─ routes/
│  ├─ utils/
│  ├─ .env
│  ├─ index.js
│  └─ package.json
├─ frontend/
│  ├─ src/
│  ├─ public/
│  ├─ index.html
│  ├─ package.json
│  └─ vite.config.js
├─ README.md
└─ .gitignore
```

## Prerequisites

Before running the project, make sure you have the following installed:

- Node.js v18 or newer
- npm or yarn
- MongoDB running locally or a MongoDB Atlas connection string
- Cloudinary account for image uploads

## Setup

### 1) Backend setup

```bash
cd backend
npm install
```

Create a `.env` file inside the `backend` folder with the variables below:

```env
PORT=3000
MONGO_URI=mongodb://localhost:27017/jobportal
SECRET_KEY=your_super_secret_key
CLOUD_NAME=your_cloud_name
API_KEY=your_cloudinary_api_key
API_SECRET=your_cloudinary_api_secret
```

Note: the current backend code reads `SECRET_KEY` for authentication. If your environment uses a different variable name, keep it aligned with the code that signs and verifies JWTs.

### 2) Frontend setup

```bash
cd frontend
npm install
```

## Run the app

Open two terminals.

### Terminal 1: Start backend

```bash
cd backend
npm run dev
```

The backend runs at:

```text
http://localhost:3000
```

### Terminal 2: Start frontend

```bash
cd frontend
npm run dev
```

The frontend runs at:

```text
http://localhost:5173
```

## Available Scripts

### Backend

```bash
npm run dev
```

Starts the Express server with nodemon for live reloads.

### Frontend

```bash
npm run dev
npm run build
npm run preview
npm run lint
```

## Production Build

```bash
cd frontend
npm run build
```

The production build is generated in the `frontend/dist` folder.

## Notes

- The application is designed as a monorepo with separate backend and frontend folders.
- Frontend requests are configured to use the local backend API at `http://localhost:3000`.
- Cloudinary is used for upload features, so you need valid Cloudinary credentials for image-related flows.

## License

This project is for educational and demonstration purposes.
