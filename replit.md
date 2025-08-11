# Overview

This is a full-stack school management system built with React, Express, and PostgreSQL. The application provides role-based access control for managing teachers, activities, inventory, calendar events, and student incidents within an educational institution. It features a modern UI built with shadcn/ui components and Tailwind CSS, with server-side authentication and a comprehensive dashboard for different user roles.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **Framework**: React with TypeScript using Vite as the build tool
- **UI Library**: shadcn/ui components built on Radix UI primitives
- **Styling**: Tailwind CSS with CSS variables for theming
- **State Management**: TanStack Query for server state management
- **Routing**: Wouter for client-side routing
- **Forms**: React Hook Form with Zod validation
- **Authentication**: Context-based auth provider with protected routes

## Backend Architecture
- **Framework**: Express.js with TypeScript
- **Database ORM**: Drizzle ORM with PostgreSQL dialect
- **Authentication**: Passport.js with local strategy and session-based auth
- **Session Storage**: PostgreSQL session store using connect-pg-simple
- **Password Hashing**: Node.js crypto module with scrypt
- **File Structure**: Monorepo structure with shared schema between client and server

## Database Design
- **Users Table**: Role-based user management (admin, teacher, digitizer, coordinator, secretary, assistant_secretary)
- **Activities Table**: Educational activity workflow management with status tracking
- **Inventory Items Table**: School supply management with low-stock alerts
- **Calendar Events Table**: Event scheduling and task management
- **Student Incidents Table**: Incident reporting and tracking system

## Role-Based Access Control
- **Admin**: Full system access including user management
- **Teacher**: Limited to activity submission and viewing own content
- **Digitizer**: Activity processing and digitization workflow
- **Coordinator**: Activity approval and coordination tasks
- **Secretary/Assistant Secretary**: Administrative functions and event management

## API Design Patterns
- RESTful API endpoints with consistent error handling
- Request/response middleware for logging and monitoring
- Authentication middleware protecting sensitive routes
- Zod schema validation for all data inputs
- Standardized JSON responses with proper HTTP status codes

# External Dependencies

## Database
- **Neon Database**: Serverless PostgreSQL database with websocket support
- **Drizzle Kit**: Database migration and schema management
- **Connection Pool**: @neondatabase/serverless for optimized connections

## UI Components
- **Radix UI**: Comprehensive primitive component library
- **Embla Carousel**: Carousel/slider functionality
- **Lucide React**: Icon library for consistent iconography
- **Class Variance Authority**: Type-safe component variants

## Development Tools
- **Vite**: Fast build tool with HMR support
- **ESBuild**: Fast JavaScript bundler for production
- **PostCSS**: CSS processing with Tailwind and Autoprefixer
- **TypeScript**: Type safety across the entire stack

## Authentication & Security
- **Passport.js**: Authentication middleware
- **Express Session**: Session management
- **Crypto Module**: Secure password hashing with salt

## Data Validation
- **Zod**: Runtime type validation and schema generation
- **Drizzle-Zod**: Integration between Drizzle ORM and Zod schemas

## Utilities
- **Date-fns**: Date manipulation and formatting
- **clsx/twMerge**: Conditional className utilities
- **Nanoid**: Unique ID generation