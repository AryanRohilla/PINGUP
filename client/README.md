# PingUp - Social Network Platform

PingUp is a full-stack social networking platform built with modern web technologies. It allows users to connect, share posts, stories, send messages, and manage connections.

## Technologies Used

### Frontend (client/)
- **React**: UI library for building interactive user interfaces.
- **Vite**: Fast development server and build tool.
- **Redux Toolkit**: State management for user, messages, and connections.
- **Clerk**: Authentication and user management.
- **Tailwind CSS**: Utility-first CSS framework for styling.
- **Axios**: HTTP client for API requests.
- **React Router**: Routing for SPA navigation.
- **Lucide React**: Icon library.
- **Moment.js**: Date formatting.

### Backend (server/)
- **Node.js**: JavaScript runtime.
- **Express**: Web framework for building REST APIs.
- **MongoDB**: NoSQL database for storing user, post, story, message, and connection data.
- **Mongoose**: ODM for MongoDB.
- **ImageKit**: Image upload and transformation.
- **Multer**: File upload middleware.
- **Nodemailer**: Email sending.
- **Inngest**: Event-driven workflows (e.g., scheduled story deletion, notifications).
- **Clerk Express**: Middleware for authentication.

## Project Structure

```
client/
  ├── src/
  │   ├── Components/      # Reusable UI components
  │   ├── features/        # Redux slices
  │   ├── pages/           # Route pages
  │   ├── assets/          # Images and icons
  │   ├── api/             # Axios instance
  │   └── app/             # Redux store
  ├── public/              # Static files
  ├── index.html           # Main HTML file
  └── vite.config.js       # Vite configuration

server/
  ├── controllers/         # Route controllers
  ├── models/              # Mongoose schemas
  ├── routes/              # Express routers
  ├── configs/             # DB, ImageKit, Multer, Nodemailer configs
  ├── middlewares/         # Auth middleware
  ├── inngest/             # Event workflows
  ├── server.js            # Entry point
  └── package.json         # Dependencies
```

## Features

- User authentication and profile management
- Create, edit, and delete posts with images
- Post creation with images and text
- Stories (text, image, video) with auto-deletion after 24 hours
- Messaging (real-time via SSE)
- Discover users and manage connections (follow, connect, accept)
- Notifications and email reminders
- Recent messages and chat box
- View user profiles and their posts

## Getting Started

1. **Install dependencies**  
   - `cd client && npm install`
   - `cd server && npm install`

2. **Configure environment variables**  
   - Set up `.env` files in both `client/` and `server/` folders.

3. **Run the development servers**  
   - Client: `npm run dev`  
   - Server: `npm run server