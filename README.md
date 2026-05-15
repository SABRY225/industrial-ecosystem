# Industrial Ecosystem Platform (Frontend)

A modern **React-based frontend** for a cinematic Industrial & Commercial Ecosystem Platform with WebGL experience, marketplace system, and enterprise dashboards.

---

# Tech Stack

- React (Vite)
- JavaScript (No TypeScript)
- Tailwind CSS
- GSAP (Scroll Animations)
- Three.js (WebGL / CGI City Scene)
- React Router DOM
- Zustand (State Management)
- React Query (Server State)
- Axios (API Calls)
- Socket.IO Client (Realtime)
- Framer Motion (UI Animations)

---

# Features

## Landing Experience (Cinematic 3D)
- WebGL Industrial City Scene
- Neon Night Lighting (Gold Theme)
- Scroll-based Camera Flythrough
- GSAP ScrollTrigger Animation
- Adaptive Performance Scaling (Mobile Friendly)

---

## Marketplace System
- Company Listings
- Smart Filters (Sector, Trust Level, Location)
- Search System
- Sponsored Listings
- Infinite Scroll

---

## Company Profile
- Company Overview
- Verification Badge System
- Gallery (Images / Videos)
- Services & Products
- Direct Contact (Chat / WhatsApp / Email)

---

## Vendor Dashboard
- Analytics Dashboard
- Wallet System UI
- Product Management
- Ads Management
- Verification Status
- Messages & Notifications

---

## Auth System
- Login / Register
- OTP Verification
- JWT Authentication
- Password Reset

---

## Realtime System
- Live Chat (Socket.IO)
- Notifications
- Live Updates (Orders / Requests)

---

# Project Structure

```bash
src/
│
├── assets/
│   ├── images/
│   ├── icons/
│   ├── models/        # 3D models (GLTF)
│   └── textures/
│
├── components/
│   ├── ui/
│   ├── layout/
│   ├── landing/
│   │   ├── HeroScene.jsx
│   │   ├── CityScene.jsx
│   │   ├── CameraController.jsx
│   │   ├── SectorCards.jsx
│   │   └── ScrollManager.jsx
│   │
│   ├── marketplace/
│   ├── company/
│   ├── dashboard/
│   ├── auth/
│   ├── wallet/
│   ├── ads/
│   └── shared/
│
├── pages/
│   ├── Landing.jsx
│   ├── Marketplace.jsx
│   ├── CompanyProfile.jsx
│   ├── Login.jsx
│   ├── Register.jsx
│   ├── VendorDashboard.jsx
│   ├── Pricing.jsx
│   ├── About.jsx
│   └── Contact.jsx
│
├── hooks/
│   ├── useAuth.js
│   ├── useScroll.js
│   ├── useThreeScene.js
│   └── useSocket.js
│
├── services/
│   ├── api.js
│   ├── auth.service.js
│   ├── company.service.js
│   ├── marketplace.service.js
│   └── wallet.service.js
│
├── store/
│   ├── auth.store.js
│   ├── ui.store.js
│   ├── marketplace.store.js
│   └── wallet.store.js
│
├── routes/
│   └── index.jsx
│
├── utils/
├── constants/
├── styles/
│   ├── globals.css
│   ├── animations.css
│   └── theme.css
│
├── App.jsx
└── main.jsx
```

---

# Installation

## 1. Create Project

```bash
npm create vite@latest web-app -- --template react
cd web-app
```

---

## 2. Install Dependencies

```bash
npm install react-router-dom axios zustand @tanstack/react-query
```

---

## 3. UI & Styling

```bash
npm install tailwindcss postcss autoprefixer
```

Initialize Tailwind:

```bash
npx tailwindcss init -p
```

---

## 4. Animations

```bash
npm install gsap framer-motion
```

---

## 5. Three.js (3D City)

```bash
npm install three @react-three/fiber @react-three/drei
```

---

## 6. Realtime

```bash
npm install socket.io-client
```

---

## 7. Forms

```bash
npm install react-hook-form zod @hookform/resolvers
```

---

## 8. Charts

```bash
npm install recharts
```

---

## 9. Utilities

```bash
npm install lodash dayjs uuid
```

---

## 10. Notifications

```bash
npm install react-hot-toast
```

---

# Environment Variables

Create `.env`

```env
VITE_API_URL=http://localhost:5000/api/v1
VITE_SOCKET_URL=http://localhost:5000
```

---

# Run Project

## Development

```bash
npm run dev
```

---

## Build

```bash
npm run build
```

---

## Preview

```bash
npm run preview
```

---

# Core Architecture

## State Flow

```text
API → React Query → Zustand → UI Components
```

---

## Realtime Flow

```text
Socket.IO Server → Client Hook → Zustand Store → UI Update
```

---

## 3D Scene Flow

```text
Scroll → GSAP → Camera Rig → Three.js Scene Update
```

---

# Performance Optimization

- Lazy Loading Components
- Code Splitting (React Router)
- Texture Compression (WebP / AVIF)
- GPU Detection (adaptive quality)
- FPS scaling for mobile
- CDN for assets

---

# Landing Page (3D System)

## Core Features
- Industrial Night City
- Neon Gold Lighting
- Moving Camera Flythrough
- Scroll Controlled Animation
- Dynamic Ads in Scene

## Stack
- Three.js
- React Three Fiber
- GSAP ScrollTrigger

---

# Marketplace Features

- Smart Filters
- Sector-based Browsing
- Company Ranking System
- Sponsored Listings
- Search Autocomplete

---

# Authentication Flow

```text
Login → JWT → Store Token → Protected Routes
```

---

# Dashboard Features

- Revenue Analytics
- Wallet Tracking
- Leads Management
- Ads Performance
- Verification Status

---

# API Integration

Example Axios Setup:

```js
import axios from "axios";

export const api = axios.create({
  baseURL: import.meta.env.VITE_API_URL,
});

api.interceptors.request.use((config) => {
  const token = localStorage.getItem("token");
  if (token) config.headers.Authorization = `Bearer ${token}`;
  return config;
});
```

---

# Folder Design Philosophy

- Feature-Based Architecture
- Separation of UI / Logic / Services
- Scalable Component System
- Clean State Management (Zustand)

---

# Deployment

Recommended:

- Vercel (Frontend)
- Cloudflare CDN
- Nginx Reverse Proxy (optional)

---

# Future Enhancements

- WebGL Metaverse Mode
- AI Company Recommendation
- AR Product Preview
- Voice Search
- Multi-language (i18n)
- Offline Mode (PWA)

---

# License

MIT

---

# Author

Industrial Ecosystem Platform UI Team