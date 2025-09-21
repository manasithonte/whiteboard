# Whiteboard Application

A real-time collaborative whiteboard application built with React and Node.js, featuring user authentication, canvas sharing, and real-time drawing synchronization.

## 🚀 Features

### Drawing Tools
- **Brush Tool**: Freehand drawing with smooth strokes
- **Line Tool**: Draw straight lines
- **Rectangle Tool**: Create rectangular shapes with customizable fill
- **Circle Tool**: Draw circular shapes with customizable fill
- **Arrow Tool**: Create directional arrows
- **Eraser Tool**: Remove elements from the canvas
- **Text Tool**: Add text annotations

### Collaborative Features
- **Real-time Collaboration**: Multiple users can draw simultaneously
- **Canvas Sharing**: Share canvases with specific users
- **Live Updates**: See other users' drawings in real-time
- **User Authentication**: Secure login and registration system

### Additional Features
- **Undo/Redo**: Full history management for all actions
- **Export**: Download canvas as PNG image
- **Color Palette**: Multiple color options for strokes and fills
- **Stroke Size Control**: Adjustable line thickness
- **Responsive Design**: Works on desktop and mobile devices

## 🏗️ Architecture

The application consists of two main parts:

### Frontend (React)
- **Location**: `whiteboard-tutorial/`
- **Framework**: React 18 with React Router
- **Styling**: CSS Modules + Tailwind CSS
- **Drawing Library**: Rough.js for hand-drawn aesthetics
- **Real-time**: Socket.IO client for live collaboration

### Backend (Node.js)
- **Location**: `backend/`
- **Framework**: Express.js
- **Database**: MongoDB with Mongoose
- **Authentication**: JWT tokens with bcrypt password hashing
- **Real-time**: Socket.IO server for WebSocket communication

## 🛠️ Tech Stack

### Frontend
- React 18.2.0
- React Router DOM 7.1.5
- Socket.IO Client 4.8.1
- Rough.js 4.6.6 (hand-drawn graphics)
- Perfect Freehand 1.2.0 (smooth brush strokes)
- Axios 1.7.9 (HTTP client)
- React Icons 4.12.0
- Tailwind CSS 3.3.6

### Backend
- Node.js
- Express.js 4.21.2
- MongoDB with Mongoose 8.10.0
- Socket.IO 4.8.1
- JWT Authentication (jsonwebtoken 9.0.2)
- Password Hashing (bcrypt 5.1.1)
- CORS enabled

## 🚀 Getting Started

### Prerequisites
- Node.js (v14 or higher)
- MongoDB (local or cloud instance)
- npm or yarn package manager

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd whiteboard
   ```

2. **Set up the Backend**
   ```bash
   cd backend
   npm install
   ```

3. **Set up the Frontend**
   ```bash
   cd ../whiteboard-tutorial
   npm install
   ```

4. **Environment Setup**
   
   Create a `.env` file in the `backend` directory:
   ```env
   MONGODB_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret_key
   PORT=5001
   ```

5. **Start the Backend Server**
   ```bash
   cd backend
   npm start
   ```
   The backend will run on `http://localhost:5001`

6. **Start the Frontend Development Server**
   ```bash
   cd whiteboard-tutorial
   npm start
   ```
   The frontend will run on `http://localhost:3000`

## 📱 Usage

### User Registration & Login
1. Navigate to the application
2. Click "Register" to create a new account
3. Or click "Login" if you already have an account

### Creating a Canvas
1. After logging in, you'll be redirected to the main whiteboard
2. Start drawing using the toolbar tools
3. Your canvas is automatically saved

### Sharing a Canvas
1. Each canvas has a unique URL (e.g., `/canvas-id`)
2. Share the URL with other users
3. They can join and collaborate in real-time

### Drawing Tools
- Select any tool from the toolbar
- Choose colors and stroke sizes from the toolbox
- Use keyboard shortcuts:
  - `Ctrl+Z`: Undo
  - `Ctrl+Y`: Redo

## 🔧 API Endpoints

### User Routes (`/api/users`)
- `POST /register` - User registration
- `POST /login` - User authentication
- `GET /profile` - Get user profile (protected)

### Canvas Routes (`/api/canvas`)
- `GET /` - Get user's canvases (protected)
- `POST /` - Create new canvas (protected)
- `GET /:id` - Get specific canvas (protected)
- `PUT /:id` - Update canvas (protected)
- `DELETE /:id` - Delete canvas (protected)
- `POST /:id/share` - Share canvas with user (protected)

## 🔒 Security Features

- JWT-based authentication
- Password hashing with bcrypt
- Canvas access control (owner and shared users only)
- CORS configuration
- Input validation and sanitization

## 🌐 Deployment

### Backend Deployment
The backend is configured for Vercel deployment with `vercel.json`.

### Frontend Deployment
The React app can be deployed to any static hosting service like Vercel, Netlify, or GitHub Pages.


**Happy Drawing! 🎨**
