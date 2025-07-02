# Pack 100 Criativos Editáveis - Marketing Digital Landing Page

## Overview

This is a full-stack React application built for a Brazilian marketing product landing page. The application promotes a pack of 100 editable creative assets for digital marketing purposes. It features a modern, responsive design with a single-page application architecture that includes hero sections, pricing offers, testimonials, and conversion-focused elements.

## System Architecture

### Frontend Architecture
- **Framework**: React 18+ with TypeScript
- **Build Tool**: Vite for fast development and optimized production builds
- **Styling**: Tailwind CSS with custom design system using CSS variables
- **UI Components**: shadcn/ui component library built on Radix UI primitives
- **Routing**: Wouter for lightweight client-side routing
- **State Management**: TanStack Query for server state management
- **Form Handling**: React Hook Form with Zod validation

### Backend Architecture
- **Runtime**: Node.js with Express.js server
- **Database**: PostgreSQL with Drizzle ORM for type-safe database operations
- **Database Provider**: Neon Database (serverless PostgreSQL)
- **Session Management**: PostgreSQL-based session storage
- **API Design**: RESTful API architecture with `/api` prefix

### Development Environment
- **Development Server**: Vite dev server with HMR (Hot Module Replacement)
- **TypeScript**: Strict type checking across frontend, backend, and shared code
- **Code Organization**: Monorepo structure with shared types and schemas

## Key Components

### Frontend Structure
```
client/
├── src/
│   ├── components/ui/     # Reusable UI components (shadcn/ui)
│   ├── hooks/            # Custom React hooks
│   ├── lib/              # Utility functions and configurations
│   └── pages/            # Page components (landing, not-found)
```

### Backend Structure
```
server/
├── index.ts              # Express server setup and middleware
├── routes.ts             # API route definitions
├── storage.ts            # Data layer with memory/PostgreSQL implementations
└── vite.ts              # Development server integration
```

### Shared Resources
```
shared/
└── schema.ts             # Database schemas and types using Drizzle ORM
```

## Data Flow

1. **Client Requests**: Frontend makes API calls using TanStack Query
2. **Server Processing**: Express server handles requests with proper error handling
3. **Data Storage**: Currently uses in-memory storage with PostgreSQL schema ready
4. **Response Handling**: Type-safe responses using shared TypeScript interfaces
5. **State Management**: TanStack Query manages caching and synchronization

## External Dependencies

### UI and Styling
- **Radix UI**: Accessible, unstyled UI primitives
- **Tailwind CSS**: Utility-first CSS framework
- **Lucide React**: Modern icon library
- **Class Variance Authority**: Type-safe CSS class composition

### Backend Services
- **Neon Database**: Serverless PostgreSQL database
- **Drizzle ORM**: Type-safe database toolkit
- **Connect PG Simple**: PostgreSQL session store for Express

### Development Tools
- **Replit Integration**: Runtime error overlay and cartographer for development
- **ESBuild**: Fast JavaScript bundler for production builds
- **PostCSS**: CSS post-processor with Autoprefixer

## Deployment Strategy

### Development
- **Local Development**: `npm run dev` runs both Vite dev server and Express server
- **Hot Reloading**: Vite provides instant feedback for frontend changes
- **Type Checking**: `npm run check` for TypeScript validation

### Production
- **Build Process**: 
  1. Frontend: Vite builds optimized static assets
  2. Backend: ESBuild bundles server code for Node.js
- **Deployment**: Single command `npm start` runs the production server
- **Database**: Drizzle migrations with `npm run db:push`

### Architecture Decisions

**Problem**: Need for type-safe full-stack development
**Solution**: Shared TypeScript schemas using Drizzle ORM
**Benefits**: Eliminates type mismatches between frontend and backend

**Problem**: Fast development iteration
**Solution**: Vite + Express integration with HMR
**Benefits**: Instant feedback during development

**Problem**: Scalable UI component system
**Solution**: shadcn/ui built on Radix UI primitives
**Benefits**: Accessible, customizable, and maintainable components

**Problem**: Landing page conversion optimization
**Solution**: Single-page application with scroll-based interactions
**Benefits**: Fast loading, smooth user experience, better conversion rates

## Changelog

- July 02, 2025. Initial setup

## User Preferences

Preferred communication style: Simple, everyday language.