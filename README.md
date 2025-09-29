# Live Polling System

A real-time polling system built with React, Express.js, and Socket.io that allows teachers to create polls and students to participate in real-time.

## Features

### Teacher Features
- Create new polls with multiple choice questions
- Set configurable time limits (30s - 5min)
- View live results with real-time updates
- See participant list and manage students
- Remove students from the poll
- View poll history
- Real-time chat with students

### Student Features
- Join with unique name per session
- Submit answers to active polls
- View live results after submitting
- Auto-show results when time expires
- Real-time chat with teacher and other students
- Responsive design for mobile and desktop

## Color Palette

- Primary Purple: `#7765DA`
- Secondary Purple: `#5767D0`
- Dark Purple: `#4F0DCE`
- Light Gray: `#F2F2F2`
- Dark Gray: `#373737`
- Medium Gray: `#6E6E6E`

## Project Structure

```
polling/
├── frontend/          # React TypeScript app
│   ├── src/
│   │   ├── components/    # React components
│   │   ├── context/       # Socket.io context
│   │   └── types.ts       # TypeScript interfaces
├── backend/           # Express.js + Socket.io server
│   ├── server.js          # Main server file
│   └── package.json
└── README.md
```

## Quick Start

### Option 1: Automated Setup (Recommended)

**Windows:**
```bash
start.bat
```

**Linux/Mac:**
```bash
./start.sh
```

### Option 2: Manual Setup

1. **Install all dependencies**:
   ```bash
   npm run setup
   ```

2. **Start both servers**:
   ```bash
   npm run dev
   ```

### Option 3: Individual Setup

#### Backend Setup

1. Navigate to the backend directory:
   ```bash
   cd backend
   npm install
   npm run dev
   ```

#### Frontend Setup

1. In a new terminal, navigate to frontend:
   ```bash
   cd frontend
   npm install
   npm start
   ```

**Servers will run on:**
- Backend: `http://localhost:5000`
- Frontend: `http://localhost:3000`

## Usage

1. **Start both servers** (backend on :5000, frontend on :3000)
2. **Open the app** in your browser
3. **Choose your role**: Student or Teacher
4. **As a Teacher**:
   - Create polls with questions and options
   - Set time limits
   - Monitor student responses in real-time
   - Manage participants
5. **As a Student**:
   - Enter your name to join
   - Wait for teacher to ask questions
   - Submit your answers
   - View live results

## Deployment

### Backend Deployment (e.g., Heroku, Railway, Render)

1. Set environment variables:
   ```
   PORT=5000
   NODE_ENV=production
   CORS_ORIGIN=https://your-frontend-domain.com
   ```

2. Deploy with:
   ```bash
   npm start
   ```

### Frontend Deployment (e.g., Netlify, Vercel)

1. Build the app:
   ```bash
   npm run build
   ```

2. Set environment variable:
   ```
   REACT_APP_SERVER_URL=https://your-backend-domain.com
   ```

3. Deploy the `build` folder

## Features Implemented

- ✅ Real-time polling with Socket.io
- ✅ Teacher poll creation and management
- ✅ Student participation and live results
- ✅ Configurable time limits
- ✅ Student removal functionality
- ✅ Chat system between teacher and students
- ✅ Poll history viewing
- ✅ Responsive design
- ✅ Exact Figma design implementation
- ✅ Complete color palette adherence

## Technology Stack

- **Frontend**: React 18, TypeScript, Socket.io Client
- **Backend**: Express.js, Socket.io, Node.js
- **Real-time Communication**: Socket.io
- **Styling**: CSS3 with CSS Variables
- **State Management**: React Context API

## API Endpoints

- `GET /api/health` - Health check
- `GET /api/current-poll` - Get current active poll
- `GET /api/poll-history` - Get all previous polls

## Socket Events

### Client to Server
- `joinAsStudent` - Student joins with name
- `createPoll` - Teacher creates new poll
- `submitAnswer` - Student submits answer
- `endPoll` - Teacher ends current poll
- `removeStudent` - Teacher removes student
- `sendMessage` - Send chat message

### Server to Client
- `currentPoll` - Current poll state
- `newPoll` - New poll created
- `pollResults` - Updated poll results
- `pollEnded` - Poll has ended
- `studentsUpdate` - Updated student list
- `newMessage` - New chat message
- `error` - Error message
- `removed` - Student was removed
#
