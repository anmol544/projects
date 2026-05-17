# School Management System

A full-stack school management system built with React, Redux, Express, and MongoDB. The project supports separate workflows for admins, teachers, and students, making it easier to manage classes, subjects, attendance, marks, notices, and complaints from a single platform.

## Overview

This repository contains:

- A React frontend for the user interface
- An Express + MongoDB backend for APIs and data storage
- Role-based dashboards for `Admin`, `Teacher`, and `Student`

## Features

### Admin

- Register and log in
- Manage classes, subjects, teachers, and students
- Assign subjects to teachers
- Update student attendance and exam marks
- Create, view, update, and delete notices
- Review student complaints

### Teacher

- Log in to a dedicated dashboard
- View assigned class and subject information
- Mark student attendance
- Submit complaints

### Student

- Log in to a dedicated dashboard
- View profile and enrolled subjects
- Track attendance
- Submit complaints

## Tech Stack

- Frontend: React, React Router, Redux Toolkit, Material UI, Styled Components, Axios, Recharts
- Backend: Node.js, Express, Mongoose, bcrypt, CORS, dotenv
- Database: MongoDB

## Project Structure

```text
Group19_IWP_W24_Project/
+-- README.md
`-- projects/
    +-- backend/
    |   +-- controllers/
    |   +-- models/
    |   +-- routes/
    |   +-- index.js
    |   `-- package.json
    `-- frontend/
        +-- public/
        +-- src/
        |   +-- assets/
        |   +-- components/
        |   +-- pages/
        |   `-- redux/
        +-- netlify.toml
        `-- package.json
```

## Environment Variables

Create a `.env` file in each app where needed.

### Backend: `projects/backend/.env`

```env
MONGO_URL=your_mongodb_connection_string
PORT=5000
```

### Frontend: `projects/frontend/.env`

```env
REACT_APP_BASE_URL=http://localhost:5000
```

## Getting Started

### 1. Install dependencies

Backend:

```bash
cd projects/backend
npm install
```

Frontend:

```bash
cd projects/frontend
npm install
```

### 2. Start the backend

```bash
cd projects/backend
npm start
```

The backend runs on `http://localhost:5000` by default.

### 3. Start the frontend

```bash
cd projects/frontend
npm start
```

The frontend runs on `http://localhost:3000`.

## Available Scripts

### Frontend

- `npm start` - Runs the React app in development
- `npm run build` - Builds the frontend for production
- `npm test` - Runs frontend tests

### Backend

- `npm start` - Starts the backend with `nodemon`
- `npm run build` - Installs dependencies
- `npm test` - Placeholder test script

## API Modules

The backend exposes routes for:

- Admin authentication and profile
- Student management
- Teacher management
- Class management
- Subject management
- Notices
- Complaints
- Attendance and exam results

## Deployment Notes

- The frontend includes a `netlify.toml` file for SPA redirects on Netlify
- Make sure `REACT_APP_BASE_URL` points to your deployed backend URL in production

## Notes

- The frontend title is set to `School Management System`
- The app uses role-based navigation and separate dashboards after login
- MongoDB connection is required before the backend can serve app data

## Future Improvements

- Add automated tests for frontend and backend
- Add API documentation
- Add Docker support for easier local setup
- Improve role permissions and validation
