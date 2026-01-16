# CNCF_Hackathon

## Topic:- Open Source For Good

#### Problem Statement:- Creating a social/enviornmental challenge and building a cloud native solution for it, using at least one CNCF Project.
---

## Solution

## CloudWave🌊  
CloudWave is a modern, cloud-native web application built with React, Next.js, and TypeScript that provides real-time monitoring of water buoys across the globe. Designed for Dockeer deployment with CNCF tool integration.

### Features
 - Interactive World Map: Beautiful Leaflet.js integration with dark theme
 - Real-time Data Streaming: Live updates every 5 seconds with WebSocket support
 - Modern Tech Stack: React 18, Next.js 14, TypeScript, Tailwind CSS
 - Cloud-Native Ready: Docker deployment with monitoring integration
 - Responsive Design: Works seamlessly across all devices
 - Modern UI/UX: Glassmorphism effects, smooth animations, gradient text
 - Real-time API: RESTful endpoints with live data updates

### Project Structure
```
cloudwave/
├── src/
│   ├── app/
│   │   ├── api/
│   │   │   └── buoys/
│   │   │       └── route.ts          # API endpoint for buoy data
│   │   ├── globals.css               # Global styles with Tailwind
│   │   ├── layout.tsx                # Root layout component
│   │   └── page.tsx                  # Main page component
│   ├── components/
│   │   ├── BuoyMarker.tsx           # Individual buoy marker component
│   │   ├── HeroSection.tsx          # Landing page hero section
│   │   ├── StatusBar.tsx            # Real-time status indicator
│   │   └── WorldMap.tsx             # Main map component
│   ├── hooks/
│   │   └── useBuoyData.ts           # Custom hook for data management
│   └── types/
│       └── buoy.ts                  # TypeScript type definitions
├── docker/
│   ├── Dockerfile.dev              # Development Docker image
│   └── docker-compose.yml          # Local development setup
├── index.html                       # In-line html file to reflect a basic Idea of the react app
├── package.json
├── next.config.js
├── tailwind.config.js
├── tsconfig.json
└── README.md
```

### Project Setup

1) Cloning & Setting up locally
   ```bash
   # Clone the repository
   git clone https://github.com/your-username/cloudwave.git
   cd cloudwave

    # Install dependencies
    npm install
    # or
    yarn install
    # or
    pnpm install
    ```

2) Development Server
   ```bash
   # Start the development server
    npm run dev
    # or
    yarn dev
    # or
    pnpm dev
   ```

#### Docker Development 

1) Create Docker Development enviornment
   ```bash
   # Build and run with docker-compose
    docker-compose up -d

    # View logs
    docker-compose logs -f cloudwave
    ```

2) Production Docker Build
   ```bash
   # Build production image
    docker build -f docker/Dockerfile -t cloudwave:latest .

    # Run production container
    docker run -p 3000:3000 -e NODE_ENV=production cloudwave:latest
   ```

## Future Scope
- AI integration for real-time monitoring of climate changes in Oceanic Regions.
- Tracking data for every single Buoy on the grid.
- OpenTelemetary use case integration.
