# React Job Management System

This repository contains a modern React job management application built with React Router for navigation and JSON Server for backend simulation. The app features a complete job tracking experience including user authentication, job creation and management, issue tracking within jobs, and category organization. It demonstrates React component architecture, state management, and RESTful API integration for a job management platform.

## Prerequisites

- Node.js and npm installed on your system
- A modern web browser (Chrome, Firefox, Edge, Safari, etc.)
- (Optional) A code editor like VS Code, Sublime Text, or Atom for easier code navigation

## Installation

1. **Clone the repository** (if not already downloaded):
   ```sh
   git clone <repository-url>
   cd Job-Management-main
   ```
2. **Install dependencies**:
   ```sh
   npm install
   ```

## How to Run

1. **Start the JSON Server** (backend simulation):
   ```sh
   npx json-server --watch database.json --port 9999
   ```

2. **Start the React development server** (in a new terminal):
   ```sh
   npm start
   ```

This will open the app in your default browser at [http://localhost:3000](http://localhost:3000). The page will reload automatically when you make changes to the source code.

**Note**: Make sure both the JSON Server (port 9999) and React development server (port 3000) are running simultaneously for the application to work properly.

## Project Structure

```
Job-Management-main/
├── database.json
├── public/
│   ├── favicon.ico
│   ├── index.html
│   ├── logo192.png
│   ├── logo512.png
│   ├── manifest.json
│   └── robots.txt
├── src/
│   ├── components/
│   │   ├── addJob.jsx
│   │   ├── detail.jsx
│   │   ├── job.css
│   │   ├── job.jsx
│   │   └── login.jsx
│   ├── App.js
│   └── index.js
├── package.json
├── package-lock.json
└── README.md
```

- **database.json**: Mock database containing users, jobs, categories, and issues data for the JSON Server.
- **public/**: Contains static assets and the HTML template.
  - `index.html`: The main HTML file loaded by React.
  - `manifest.json`, `robots.txt`: Standard web app metadata and configuration.
  - `favicon.ico`, `logo192.png`, `logo512.png`: App icons and branding assets.
- **src/**: Contains the React source code.
  - `components/`: Reusable React components for different sections of the app.
    - `login.jsx`: User authentication component with form validation.
    - `job.jsx`: Main job listing component with search, filtering, and CRUD operations.
    - `detail.jsx`: Job detail view with issue management and tracking.
    - `addJob.jsx`: Form component for creating new jobs with validation.
    - `job.css`: Styling for the job components.
  - `App.js`: Main application component with routing and authentication state management.
  - `index.js`: Entry point that renders the React app.
- **package.json**: Project metadata and dependencies including React, React Router, Axios, and JSON Server.
- **README.md**: Project documentation (this file).

## Features

- **User Authentication**: Secure login system with localStorage session management
- **Job Management**: Create, read, update, and delete jobs with category organization
- **Issue Tracking**: Add and manage issues within each job with start/end dates and status
- **Search and Filter**: Search jobs by title and filter by category and status
- **Responsive Design**: Clean, professional interface for job management
- **Real-time Updates**: Dynamic data updates with JSON Server backend simulation
- **Form Validation**: Input validation for job creation and user authentication

## Data Structure

The application manages the following data entities:

- **Users**: Authentication with username/password and unique user IDs
- **Jobs**: Main job entities with title, category, status, and associated issues
- **Categories**: Job categorization system for organization
- **Issues**: Sub-tasks within jobs with individual tracking and deadlines

## Technologies Used

- **React 18.3.1**: Modern React with hooks and functional components
- **React Router DOM 7.0.2**: Client-side routing for single-page application
- **Axios 1.7.9**: HTTP client for API requests
- **JSON Server 0.17.3**: Mock REST API backend for development
- **React Scripts 5.0.1**: Development and build tools

## API Endpoints

The application uses the following JSON Server endpoints:

- `GET /users` - Retrieve all users for authentication
- `GET /jobs?uId={userId}` - Get jobs for specific user
- `GET /jobs/{id}` - Get specific job details
- `POST /jobs` - Create new job
- `PATCH /jobs/{id}` - Update job (e.g., add issues)
- `DELETE /jobs/{id}` - Delete job
- `GET /categories` - Get all job categories

## Learn More

- [React Documentation](https://reactjs.org/)
- [React Router Documentation](https://reactrouter.com/)
- [JSON Server Documentation](https://github.com/typicode/json-server)
- [Axios Documentation](https://axios-http.com/)
- For questions or contributions, please open an issue or pull request.
