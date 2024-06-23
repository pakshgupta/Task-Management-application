# Task Management Application

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Running the Application](#running-the-application)
- [File Structure](#file-structure)
- [API Endpoints](#api-endpoints)
- [Frontend Components](#frontend-components)
- [Contribution](#contribution)
- [License](#license)

## Introduction

This is a full-stack Task Management Application that allows users to register, log in, create, manage, and filter tasks. The application is designed to help users keep track of their tasks efficiently.

## Features

- User authentication (Registration, Login, Logout)
- Task creation and management
- Task filtering by status (Completed, Incomplete, Archived)
- Profile management
- Responsive design

## Technologies Used

### Backend

- **Node.js**: JavaScript runtime for building scalable network applications.
- **Express**: Fast, unopinionated, minimalist web framework for Node.js.
- **Mongoose**: MongoDB object modeling tool designed to work in an asynchronous environment.
- **JWT (jsonwebtoken)**: For handling user authentication.
- **bcrypt**: Library for hashing passwords.
- **dotenv**: For managing environment variables.
- **cloudinary**: Cloud service for managing images.
- **express-fileupload**: Middleware for handling file uploads.
- **cors**: For handling Cross-Origin Resource Sharing.
- **cookie-parser**: Middleware for parsing cookies.

### Frontend

- **React**: A JavaScript library for building user interfaces.
- **React Router DOM**: For routing and navigation.
- **Bootstrap & React Bootstrap**: For responsive design and pre-built components.
- **axios**: For making HTTP requests.
- **react-hot-toast**: For notifications.
- **react-icons**: For using icons in the application.

## Prerequisites

- **Node.js**: Ensure you have Node.js installed on your system.
- **MongoDB**: You need to have MongoDB set up for the database.
- **Vite**: For building and running the frontend application.

## Installation

### Backend Setup

1. Clone the repository:

    ```bash
   git@github.com:pakshgupta/Task-Management-application.git
    ```

2. Navigate to the `backend` directory:

    ```bash
    cd backend
    ```

3. Install dependencies:

    ```bash
    npm install
    ```

4. Create a `.env` file for environment variables:

    ```plaintext
    MONGO_URI=your_mongodb_connection_string
    JWT_SECRET=your_jwt_secret
    CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
    CLOUDINARY_API_KEY=your_cloudinary_api_key
    CLOUDINARY_API_SECRET=your_cloudinary_api_secret
    ```

### Frontend Setup

1. Navigate to the `frontend` directory:

    ```bash
    cd frontend
    ```

2. Install dependencies:

    ```bash
    npm install
    ```

## Running the Application

### Running the Backend

1. Start the backend server:

    ```bash
    npm run dev
    ```

    The backend server will start at `http://localhost:5000`.

### Running the Frontend

1. Start the frontend development server:

    ```bash
    npm run dev
    ```

    The frontend application will start at `http://localhost:3000`.

## File Structure

### Backend

backend/
│
├── controllers/
│ └── authController.js
│ └── taskController.js
│
├── models/
│ └── User.js
│ └── Task.js
│
├── routes/
│ └── authRoutes.js
│ └── taskRoutes.js
│
├── utils/
│ └── jwtHelper.js
│
├── .env
├── server.js
└── package.json


### Frontend


frontend/
│
├── public/
│ └── index.html
│
├── src/
│ ├── components/
│ │ ├── Navbar.js
│ │ ├── Home.js
│ │ ├── Register.js
│ │ ├── Login.js
│ │ ├── Profile.js
│ │
│ ├── assets/
│ │ └── logo.png
│ │
│ ├── App.js
│ ├── index.js
│ └── package.json


## API Endpoints

### User Routes

- `POST /api/v1/user/register` - Register a new user
- `POST /api/v1/user/login` - Login a user
- `GET /api/v1/user/me` - Get current user details
- `GET /api/v1/user/logout` - Logout user

### Task Routes

- `GET /api/v1/task/mytask` - Get user tasks
- `POST /api/v1/task/new` - Create a new task
- `PATCH /api/v1/task/update/:id` - Update a task
- `DELETE /api/v1/task/delete/:id` - Delete a task

## Frontend Components

- **App**: The main application component.
- **Navbar**: The navigation bar for the application.
- **Home**: Displays the user's tasks.
- **Register**: Registration form for new users.
- **Login**: Login form for existing users.
- **Profile**: Displays the user's profile and allows updates.

## Contribution

Contributions are welcome! If you have any suggestions or improvements, feel free to submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

