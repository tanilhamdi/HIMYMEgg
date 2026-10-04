# 💬 Beggtho? Chat & Dashboard App

A full-stack real-time chat and dashboard application built with **React (Vite)** on the frontend and **Node.js (Express & Mongoose)** on the backend. It features secure JWT authentication via HTTP-only cookies, password hashing with bcrypt, and live message polling.

---

## 🚀 Features

- **Authentication System:** Secure Sign up (`/signin`) and Login (`/login`) with hashed passwords (`bcrypt`) and JWT stored safely in `HttpOnly` cookies.
- **Real-time Chat:** Authenticated live chat room with automatic message scrolling and 5-second interval polling.
- **Quick Links:** Integrated shortcut buttons to navigate to external services or related projects.
- **Protected Routes:** React Router navigation guarded by backend session checks (`/api/me`).

---

## 🛠️ Tech Stack

### Frontend
- **React (Vite)**
- **React Router DOM** (v6)
- **CSS** (Custom styling)

### Backend
- **Node.js & Express**
- **MongoDB & Mongoose** (Users & Messages collections)
- **JSON Web Tokens (JWT)** & **Cookie Parser**
- **Bcrypt** (Password hashing)
- **CORS** (Configured for credentials and production/development environments)

---

## 📁 Project Structure

```text
├── src/
│   ├── App.jsx        # Main dashboard and live chat interface
│   ├── Login.jsx      # Login page component
│   ├── Signin.jsx     # Registration page component
│   ├── main.jsx       # React entry point & router definitions
│   └── App.css        # Global and component styles
├── server.js          # Express backend and database models
└── package.json       # Project dependencies and scripts
```

---

## ⚙️ Environment Variables

To run the backend server, make sure you configure your `.env` file with the following variables:

```env
PORT=4000
JWT_SECRET=your_super_secret_jwt_key
MONGO_URI=your_mongodb_connection_string
NODE_ENV=development # or production
```

---

## 📦 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/tanilhamdi/beggtho.git
cd beggtho
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Run the Application
- **Start Backend:**
  ```bash
  node server.js
  ```
- **Start Frontend (Vite dev server):**
  ```bash
  npm run dev
  ```

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.
