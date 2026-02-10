# LegalMind Case Study — Fullstack Frontend Prototype

## Overview
This is a **frontend prototype** for the Full Stack Developer case study.  
It demonstrates a **legal AI chat interface**, **file upload**, **PDF viewer**, and **role based access control** (RBAC) using **React, TypeScript, Tailwind, Zustand, and React Query**.

---

## Tech Stack
- **React + TypeScript (Vite)** — main framework
- **Tailwind CSS v3** — utility-first styling
- **Zustand** — lightweight UI state (sidebar, toggles)
- **TanStack Query (React Query)** — server-state for chat & upload
- **React PDF Viewer** — display PDF and highlight pages
- **react-hot-toast** — notifications
- **react-error-boundary** — global error handling
- **react-window** — virtualized message list
- **Vitest + React Testing Library** — unit testing

---

## Architecture

src/
 ├─ app/
 │   ├─ providers/
 │   │   ├─ QueryProvider.tsx
 │   │   ├─ AuthProvider.tsx (mock)
 │   │   └─ ErrorBoundary.tsx
 │   ├─ store/
 │   │   └─ uiStore.ts (Zustand)
 │   └─ routes.tsx
 │
 ├─ components/
 │   ├─ atoms/
 │   ├─ molecules/
 │   └─ organisms/
 │
 ├─ features/
 │   ├─ auth/
 │   ├─ chat/
 │   ├─ upload/
 │   └─ pdf/
 │
 ├─ lib/
 │   ├─ api.ts (mock backend)
 │   └─ stream.ts (mock streaming)
 │
 ├─ pages/
 │   ├─ Login.tsx
 │   └─ Dashboard.tsx
 │
 └─ main.tsx

---

## Features Implemented

### Authentication & RBAC
- Roles: `admin` and `junior`
- Upload button visible **only to admin**

### Chat Interface
- Virtualized chat history

### File Upload
- Drag & drop file input
- Status indicators: Uploading → Processing → Indexed
- Toast notifications

### PDF Viewer
- Multi page PDF display
- Highlight specific page when citation is clicked

### UI / UX
- Sidebar with collapse toggle
- Tailwind CSS utility-first styling
- Accessible (aria-live for AI typing, keyboard focus)

### Error Handling
- Global error boundary
- Reset Chat button
- Toast notifications for errors

### Testing
- Sample Vitest + React Testing Library test for Upload component

---

> The focus is **frontend architecture, UX, and role based logic**.

---

## Next Improvements
- Connect real backend (Azure AD / Auth0 + real SSE/WebSockets)
- Implement RAG / vector search for AI responses
- Full PDF citation extraction & navigation
- Unit & E2E tests for all components
- Add Shadcn/UI fully for atomic design polish
