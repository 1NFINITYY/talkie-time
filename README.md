# 💬 Talkie Time — Full Stack Real-time Chat App

<p align="center">
  <img src="https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react&logoColor=black" />
  <img src="https://img.shields.io/badge/Node.js-Express-339933?style=for-the-badge&logo=node.js&logoColor=white" />
  <img src="https://img.shields.io/badge/MongoDB-Mongoose-47A248?style=for-the-badge&logo=mongodb&logoColor=white" />
  <img src="https://img.shields.io/badge/Socket.io-4.x-010101?style=for-the-badge&logo=socket.io&logoColor=white" />
  <img src="https://img.shields.io/badge/TailwindCSS-3.x-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white" />
</p>

A full-stack real-time chat application built with the MERN stack and Socket.io.

---

## 🚀 Features

- 🔐 **Authentication & Authorization** — Secure JWT-based login and signup with HTTP-only cookies
- ⚡ **Real-time Messaging** — Instant bi-directional communication powered by Socket.io
- 🟢 **Online User Status** — See who's online in real time
- 🖼️ **Image Sharing** — Upload and share images in chat via Cloudinary
- 🎨 **32 Themes** — Fully customizable UI themes powered by DaisyUI
- 👤 **Profile Management** — Update your avatar and personal info
- 🌐 **Global State Management** — Lightweight and fast state handling with Zustand
- 🛡️ **Error Handling** — Robust error handling on both client and server
- 📦 **Production Ready** — Single-command build and deploy

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| **Frontend** | React 18, Vite, React Router v6 |
| **Styling** | TailwindCSS, DaisyUI |
| **State Management** | Zustand |
| **Backend** | Node.js, Express.js |
| **Database** | MongoDB (via Mongoose) |
| **Real-time** | Socket.io |
| **Auth** | JWT, bcryptjs |
| **Media Storage** | Cloudinary |
| **HTTP Client** | Axios |

---

## 📁 Project Structure

```
talkie-time/
├── backend/
│   └── src/
│       ├── controllers/     # Route handlers
│       ├── lib/             # DB & Socket.io setup
│       ├── middleware/      # Auth middleware
│       ├── models/          # Mongoose models (User, Message)
│       ├── routes/          # API routes (auth, messages)
│       └── index.js         # Entry point
├── frontend/
│   └── src/
│       ├── components/      # Reusable UI components
│       ├── pages/           # Page views (Home, Login, Signup, Profile, Settings)
│       ├── store/           # Zustand state stores
│       ├── lib/             # Axios instance, utilities
│       └── App.jsx
└── package.json             # Root scripts for build & start
```

---

## ⚙️ Getting Started

### Prerequisites

- **Node.js** v18+
- **MongoDB** (Atlas or local)
- **Cloudinary** account (free tier works)

### 1. Clone the repository

```bash
git clone https://github.com/1NFINITYY/talkie-time.git
cd talkie-time
```

### 2. Configure environment variables

Create a `.env` file inside the `backend/` directory:

```env
MONGODB_URI=your_mongodb_connection_string
PORT=5001
JWT_SECRET=your_super_secret_jwt_key

CLOUDINARY_CLOUD_NAME=your_cloud_name
CLOUDINARY_API_KEY=your_api_key
CLOUDINARY_API_SECRET=your_api_secret

NODE_ENV=development
```

### 3. Run in development mode

Open **two terminals**:

**Terminal 1 — Backend:**
```bash
cd backend
npm install
npm run dev
```

**Terminal 2 — Frontend:**
```bash
cd frontend
npm install
npm run dev
```

The app will be live at `http://localhost:5173` 🎉

---

## 📦 Build & Deploy

Build the entire app (installs deps and compiles frontend):

```bash
npm run build
```

Start the production server:

```bash
npm start
```

> In production, the backend serves the compiled React frontend from `frontend/dist/`.

---

## 🔌 API Endpoints

### Auth Routes — `/api/auth`

| Method | Endpoint | Description |
|--------|----------|-------------|
| `POST` | `/signup` | Register a new user |
| `POST` | `/login` | Login and receive JWT cookie |
| `POST` | `/logout` | Clear auth cookie |
| `GET` | `/check` | Verify authenticated session |
| `PUT` | `/update-profile` | Update profile picture |

### Message Routes — `/api/messages`

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/users` | Get all users for sidebar |
| `GET` | `/:id` | Get messages with a specific user |
| `POST` | `/send/:id` | Send a message to a user |

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](./LICENSE) file for details.

---

<p align="center">Made with ❤️ by <a href="https://github.com/1NFINITYY">1NFINITYY</a></p>
