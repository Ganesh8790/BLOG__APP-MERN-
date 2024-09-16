# Blog Web Application

This is a **full-stack Blog Web Application** built using the **MERN stack** (MongoDB, Express.js, React, Node.js). The app allows users to register, log in, create, edit, and delete blog posts. It provides a platform for users to share their thoughts and ideas in the form of blog posts.

## Features

- **User Authentication**: Secure login and registration functionality.
- **CRUD Operations**: Users can create, read, update, and delete blog posts.
- **Responsive Design**: The app is fully responsive for both desktop and mobile views.
- **Real-time Updates**: Blog posts are updated in real-time upon creation or modification.
- **Data Persistence**: MongoDB is used to store user information and blog posts.

## Tech Stack

### Frontend:

- React.js
- Material UI
- HTML, CSS, JavaScript

### Backend:

- Node.js
- Express.js
- MongoDB for database storage
- Authentication

## Prerequisites

Ensure you have the following installed on your system:

- [Node.js](https://nodejs.org/)
- [npm](https://www.npmjs.com/)
- [MongoDB](https://www.mongodb.com/) (or set up a remote MongoDB cluster)
- [Visual Studio Code](https://code.visualstudio.com/)

## Setup Instructions

### 1. Clone the Repository

First, clone the repository to your local machine:

```bash
git clone https://github.com/Ganesh8790/blog-web-app.git
cd blog-web-app
```

### 2. Install Backend Dependencies

In the root directory of the project, install the backend dependencies:

```bash
npm install
```

### 3. Install Frontend Dependencies

Navigate to the `client` folder (which contains the React frontend) and install the frontend dependencies:

```bash
cd client
npm install
```

### 4. Set Up MongoDB

Make sure your MongoDB server is running locally or configure it to use a remote MongoDB cluster.

If using a local server, start it with:

```bash
mongod
```

Update the MongoDB connection URI in your `.env` file (explained below).

### 5. Create `.env` File

In the root directory, create a `.env` file to configure environment variables for the project.

Here’s an example of the content for your `.env` file:

```bash
# .env file

# Port on which the server will run
PORT = 8080

# Development mode
DEV_MODE = development

# MongoDB connection string
MONGO_URL = your_mongo_db_connection_url
```

Replace `your_mongo_db_connection_url` with the actual MongoDB URI string, such as:

For a local MongoDB instance:

```bash
MONGO_URL = mongodb://localhost:27017/blogApp
```

For a MongoDB Atlas cluster:

```bash
MONGO_URL = mongodb+srv://<username>:<password>@cluster0.mongodb.net/blogApp?retryWrites=true&w=majority
```

Make sure to add the `.env` file to your `.gitignore` file so it’s not included in your repository:

```bash
# Ignore the .env file
.env
```

### 6. Available Scripts

The following npm scripts are available in the project:

- **Backend**:

  ```bash
  npm run start
  ```

  Runs the backend server (`server.js`) on the port specified in the `.env` file (default is `http://localhost:8080`).

- **Frontend**:

  ```bash
  npm run client
  ```

  Runs the frontend React app on `http://localhost:3000`.

- **Development Mode** (for running both frontend and backend concurrently):

  ```bash
  npm run dev
  ```

  Runs both backend and frontend using the `concurrently` package.

## Folder Structure

```bash
├── client               # Frontend code (React app)
│   ├── public
│   └── src
│       ├── components   # React components
│       ├── pages        # Different page components (e.g., Home, Blog, Login)
│       ├── App.js
│       └── index.js
├── server.js            # Entry point for the Node.js server
├── models               # MongoDB data models (e.g., User, BlogPost)
├── routes               # Express routes for handling requests
├── .env                 # Environment variables
├── .gitignore           # Ignore node_modules, .env, etc.
└── package.json         # Dependencies and npm scripts
```

## Dependencies

### Backend

- **Express.js**: Fast, unopinionated, minimalist web framework for Node.js.
- **Mongoose**: MongoDB object modeling for Node.js.
- **bcrypt**: Library for hashing passwords.
- **cors**: Middleware for handling Cross-Origin Resource Sharing.
- **dotenv**: For loading environment variables from `.env`.

### Frontend

- **React.js**: Frontend library for building user interfaces.
- **Material UI**: React UI framework for pre-built responsive components.
