# ClassiMarket - Online Marketplace Platform

## Overview

ClassiMarket is a full-stack online marketplace application where users can buy and sell items within their local community. The platform features a modern web interface built with React and a RESTful API backend powered by Express.js. Users can browse categorized listings, post advertisements, manage favorites, and interact with sellers through a clean, responsive interface.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript for type safety and modern development
- **Routing**: Wouter for lightweight client-side routing 
- **State Management**: TanStack Query (React Query) for server state management and caching
- **UI Components**: Radix UI primitives with shadcn/ui component library for consistent, accessible design
- **Styling**: Tailwind CSS with CSS variables for theming and responsive design
- **Form Handling**: React Hook Form with Zod validation for type-safe form management
- **Build Tool**: Vite for fast development and optimized production builds

### Backend Architecture
- **Runtime**: Node.js with Express.js framework for RESTful API endpoints
- **Database**: PostgreSQL with Drizzle ORM for type-safe database operations
- **Schema Management**: Shared TypeScript schema definitions between frontend and backend
- **Development**: In-memory storage fallback for development/demo purposes
- **Session Management**: Express sessions with PostgreSQL session store

### Data Storage
- **Primary Database**: PostgreSQL for production data persistence
- **ORM**: Drizzle ORM with migrations support for schema management
- **Database Provider**: Neon Database (serverless PostgreSQL)
- **Schema**: Shared TypeScript definitions using Drizzle schema and Zod validation

### Authentication & Authorization
- **Session-Based**: Express sessions with secure cookie storage
- **User Management**: Registration, login, and user profile management
- **Security**: Password hashing and session-based authentication
- **Authorization**: User-specific data access for ads, favorites, and profiles

### API Structure
- **RESTful Design**: Standard HTTP methods (GET, POST, PUT, DELETE) for resource management
- **Endpoints**:
  - `/api/categories` - Category management and listing
  - `/api/ads` - Advertisement CRUD operations with filtering
  - `/api/users` - User registration and profile management
  - `/api/favorites` - User favorite ads management
  - `/api/auth` - Authentication endpoints
- **Data Validation**: Zod schemas for request/response validation
- **Error Handling**: Centralized error middleware with proper HTTP status codes

## External Dependencies

### Database & Storage
- **@neondatabase/serverless**: Serverless PostgreSQL database connection
- **drizzle-orm**: Type-safe database ORM and query builder
- **drizzle-kit**: Database migrations and schema management
- **connect-pg-simple**: PostgreSQL session store for Express

### UI & Styling
- **@radix-ui/***: Comprehensive suite of accessible UI primitives
- **tailwindcss**: Utility-first CSS framework
- **class-variance-authority**: Type-safe variant API for component styling
- **lucide-react**: Consistent icon library

### Development & Build
- **vite**: Fast build tool and development server
- **typescript**: Static type checking
- **@replit/vite-plugin-runtime-error-modal**: Development error handling
- **@replit/vite-plugin-cartographer**: Replit-specific development tools

### Form & Validation
- **react-hook-form**: Performant form library with minimal re-renders
- **@hookform/resolvers**: Integration adapters for validation libraries
- **zod**: TypeScript-first schema validation

### State Management & API
- **@tanstack/react-query**: Server state management and caching
- **wouter**: Lightweight routing library