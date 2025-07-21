# Calendar Stories App

A full-stack web application where users can leave stories (text, images, or videos) for each hour of every day.  
Features a calendar header, 24-hour sidebar, and interactive story timeline.

## Quick Start

### Prerequisites
- [Node.js](https://nodejs.org/)
- [MongoDB](https://www.mongodb.com/try/download/community)

### Setup

```bash
git clone <repo_url>
cd calendar-stories-app
npm install
cd client
npm install
cd ..
```

### Start Development

```bash
# In the root directory
npm run dev
```

- Frontend: http://localhost:5173
- Backend: http://localhost:5000

### Build for Production

```bash
# Build frontend
cd client
npm run build
cd ..
# Start backend with static build
npm start
```

## Features

- Calendar navigation (month/year)
- 24-hour timeline for each day
- Post stories per hour (text, images, videos)
- Responsive design

---