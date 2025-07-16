# 🏠 HomeQuest – Real Estate Web Application

A full-stack real estate platform for finding, listing, and communicating about properties, with search functionality, user authentication, and real-time messaging.

## 📋 Features

- 🔐 User authentication (register, login)
- 🏘️ Property listings with detailed information
- 🔍 Advanced search and filtering (by city, price, property type, bedrooms)
- 📍 Interactive map integration with property locations
- 💬 Real-time chat system between users
- 💾 Save favorite properties functionality
- 📱 Responsive design for all devices
- 🔔 Notification system for new messages
- 👤 User profile management

## 🛠️ Tech Stack

**Frontend:**
- React.js
- SCSS for styling
- React Router for navigation
- Leaflet for maps integration
- Socket.io client for real-time communication
- Zustand for state management

**Backend:**
- Express.js RESTful API
- Prisma ORM
- MongoDB database
- JWT authentication
- Socket.io for real-time messaging

**DevOps:**
- Concurrently for running multiple services
- Nodemon for development
- NPM for package management

## 🚀 Installation

### Prerequisites
- Node.js
- MongoDB

### Setup

```bash
# Clone the repository
git clone https://github.com/aditya-7562/HomeQuest.git
cd HomeQuest

# Install dependencies for all services
npm install
```

### Environment Variables

Create a `.env` file in the `/api` directory with the following variables:

```
DATABASE_URL=mongodb://localhost:27017/homequest
JWT_SECRET=your_jwt_secret_key
CLIENT_URL=http://localhost:5173
```

### Running the Application

```bash
# Run all services concurrently (backend, frontend, and socket server)
npm run build:all

# Or run services individually
npm run build:backend  # Start the API server
npm run build:frontend # Start the React development server
npm run build:socket   # Start the Socket.io server
```

## 🌐 API Reference

### Authentication

```
POST /api/auth/register
Register a new user

POST /api/auth/login
Authenticate user and return JWT token
```

### Properties

```
GET /api/posts
Fetch all properties with optional filters

GET /api/posts/:id
Fetch a specific property by ID

POST /api/posts
Create a new property listing
```

### User Management

```
GET /api/users/:id
Get user profile

PUT /api/users/:id
Update user profile

POST /api/users/save/:postId
Save a property to favorites
```

### Messaging

```
GET /api/chats
Get all user chats

GET /api/chats/:id
Get a specific chat

POST /api/messages/:chatId
Send a message in a chat
```

## 📁 Folder Structure

```
📦 HomeQuest
 ┣ 📂 api/                 # Backend Express API
 ┃ ┣ 📂 controllers/       # API route controllers
 ┃ ┣ 📂 middleware/        # Express middleware
 ┃ ┣ 📂 prisma/            # Prisma schema and migrations
 ┃ ┣ 📂 routes/            # API route definitions
 ┃ ┗ 📜 app.js             # Express application setup
 ┣ 📂 client/              # React frontend
 ┃ ┣ 📂 public/            # Static assets
 ┃ ┣ 📂 src/
 ┃ ┃ ┣ 📂 components/      # Reusable UI components
 ┃ ┃ ┣ 📂 context/         # React context providers
 ┃ ┃ ┣ 📂 lib/             # Utility functions
 ┃ ┃ ┣ 📂 routes/          # Page components
 ┃ ┃ ┗ 📜 App.jsx          # Main application component
 ┗ 📂 socket/              # Socket.io server
   ┗ 📜 app.js             # Socket.io setup
```

## 👥 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

⭐ **HomeQuest** - Find your dream home today! ⭐
