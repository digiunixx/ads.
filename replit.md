# DigiunixAds - Digital Marketing Agency Landing Page

## Overview

This is a modern, responsive landing page for DigiunixAds, a premium digital marketing agency specializing in Meta Ads, Google Ads, and YouTube Ads. The application is built as a full-stack solution with a React frontend and Express.js backend, featuring a contact form system for lead generation. The project has been successfully migrated to Replit environment with full functionality including dynamic case studies and blog posts.

## User Preferences

Preferred communication style: Simple, everyday language.
Design requirements: Professional, high-converting website with yellow + black + white color theme, mobile-first responsive design.

## System Architecture

### Technology Stack
- **Frontend**: React 18 with TypeScript, Vite for build tooling
- **Backend**: Express.js with TypeScript
- **Database**: PostgreSQL with Drizzle ORM
- **UI Framework**: Tailwind CSS with Radix UI components (shadcn/ui)
- **State Management**: TanStack Query for server state
- **Routing**: Wouter for client-side routing
- **Form Handling**: React Hook Form with Zod validation

### Project Structure
The application follows a monorepo structure with clear separation of concerns:
- `client/` - React frontend application
- `server/` - Express.js backend API
- `shared/` - Shared TypeScript types and schemas
- `components.json` - shadcn/ui configuration

## Key Components

### Frontend Architecture
- **Component-based design** using React functional components
- **Responsive layout** with mobile-first approach using Tailwind CSS
- **Section-based landing page** including:
  - Hero section with "Done-For-You Ads" messaging
  - Target niches section (Real Estate, Clinics, Interior Designers, Coaches, Local D2C)
  - Services section (Meta Ads, Google Ads, YouTube Ads)
  - Results section with testimonials and metrics
  - Case studies with real business examples
  - Pricing packages (Starter ₹15K, Growth ₹30K, Premium ₹60-75K)
  - Performance-based pricing model section
  - Contact form and trust elements
- **Form validation** using React Hook Form with Zod schemas
- **Toast notifications** for user feedback
- **Floating WhatsApp integration** for instant communication

### Backend Architecture
- **RESTful API** design with Express.js
- **Type-safe routing** with TypeScript
- **Middleware integration** for request logging and error handling
- **In-memory storage** (MemStorage) for development with interface for easy database migration
- **Contact form processing** with validation

### Database Schema
The application uses a simple contact management system:
- **Contacts table**: Stores lead information including name, phone, email, business type, budget, and message
- **UUID primary keys** for scalability
- **Timestamp tracking** for created_at fields

## Data Flow

1. **User interaction**: Users fill out contact forms on the landing page
2. **Form validation**: Client-side validation using Zod schemas
3. **API submission**: Form data sent to Express.js backend via POST /api/contacts
4. **Server validation**: Backend validates data using shared Zod schemas
5. **Data persistence**: Contact information stored in database (currently in-memory)
6. **Response handling**: Success/error feedback displayed to user via toast notifications

### Contact Form Flow
- Form collects: name, phone, email, business type, budget range, and optional message
- Real-time validation prevents submission of invalid data
- Success submission triggers confirmation toast and form reset
- Error handling provides user-friendly feedback

## External Dependencies

### UI Components
- **Radix UI**: Accessible, unstyled UI primitives
- **Lucide React**: Icon library for consistent iconography
- **Tailwind CSS**: Utility-first CSS framework
- **shadcn/ui**: Pre-built component library

### Database & ORM
- **Drizzle ORM**: Type-safe database ORM
- **@neondatabase/serverless**: PostgreSQL database adapter
- **Drizzle Kit**: Database migration and management tools

### Development Tools
- **Vite**: Fast build tool and development server
- **TypeScript**: Type safety across the application
- **ESBuild**: Fast JavaScript bundler for production

## Deployment Strategy

### Build Process
- **Frontend**: Vite builds React app to `dist/public/`
- **Backend**: ESBuild bundles Express server to `dist/`
- **Database migrations**: Drizzle Kit manages schema changes

### Environment Configuration
- **Development**: Uses tsx for server execution with hot reload
- **Production**: Node.js serves bundled application
- **Database**: Configurable via DATABASE_URL environment variable

### Scaling Considerations
- Current in-memory storage allows for easy migration to PostgreSQL
- Shared schema definitions enable type safety across client/server boundary
- Component architecture supports feature additions and modifications
- API structure ready for additional endpoints and functionality

The application is designed to be easily extensible, with clear separation between presentation and business logic, making it straightforward to add new features like admin dashboards, analytics integration, or additional marketing tools.

## Recent Changes (January 2025)

- ✅ **Migration Completed**: Successfully migrated from Replit Agent to Replit environment
- ✅ **Dynamic Case Studies**: Implemented individual case study pages with routing (/case-study/:id)
- ✅ **Blog Functionality**: Added dynamic blog posts with individual pages (/blog/:slug)
- ✅ **Shared Data Management**: Created centralized data files for case studies and blog content
- ✅ **Navigation Fixed**: All "View Case Study" and "Get Free Strategy Session" buttons now work properly
- ✅ **Responsive Design**: Maintained mobile-first responsive design throughout