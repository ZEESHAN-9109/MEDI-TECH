# Overview

MediTech is a comprehensive healthcare management platform built for India, focusing on community health support, AI-powered medical assistance, and family health management. The application serves rural and urban populations with features like symptom checking, medication management, health education through gamification, and community health worker support.

The platform is designed as a full-stack web application using React for the frontend and Express.js for the backend, with PostgreSQL as the database. It emphasizes accessibility through multilingual support, offline-first capabilities, and voice interactions to serve India's diverse population.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **Framework**: React 18 with TypeScript for type safety and modern development
- **Styling**: Tailwind CSS with shadcn/ui components for consistent, accessible UI design
- **State Management**: TanStack React Query for server state management and caching
- **Routing**: Wouter for lightweight client-side routing
- **Form Handling**: React Hook Form with Zod validation for type-safe form management
- **Component Library**: Radix UI primitives with custom styling for accessibility compliance

## Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Database ORM**: Drizzle ORM with PostgreSQL for type-safe database operations
- **Database Provider**: Neon Database (serverless PostgreSQL)
- **API Design**: RESTful API with organized route handlers
- **Validation**: Zod schemas shared between frontend and backend for consistency

## Database Design
- **Primary Database**: PostgreSQL with comprehensive health data schema
- **Key Entities**: Users, health metrics, medications, appointments, family members, community health workers, quiz questions, government schemes, notifications, and symptom analyses
- **Data Relationships**: Normalized design with proper foreign key relationships
- **Migration Strategy**: Drizzle Kit for schema migrations and version control

## AI Integration
- **AI Provider**: OpenAI GPT-5 for medical analysis and content generation
- **Use Cases**: Symptom analysis, health education content, and personalized recommendations
- **Safety Measures**: Medical disclaimers and guidance to seek professional care
- **Voice Support**: Web Speech API integration for multilingual voice interactions

## Authentication & Security
- **Authentication**: Simple email/password authentication with session management
- **Session Storage**: PostgreSQL-based session storage using connect-pg-simple
- **Data Protection**: User data isolation and validation at API level
- **Privacy**: Secure handling of sensitive medical information

## Mobile-First Design
- **Responsive Design**: Mobile-first approach with Tailwind CSS breakpoints
- **Progressive Web App**: Offline-first capabilities with service worker integration
- **Touch Interactions**: Optimized for mobile devices with gesture support
- **Performance**: Code splitting and lazy loading for optimal mobile performance

# External Dependencies

## Database Services
- **Neon Database**: Serverless PostgreSQL hosting with automatic scaling
- **Connection**: Environment-based DATABASE_URL configuration

## AI Services
- **OpenAI API**: GPT-5 integration for medical analysis and content generation
- **Configuration**: API key management through environment variables

## UI Components & Libraries
- **Radix UI**: Comprehensive component library for accessibility
- **Tailwind CSS**: Utility-first CSS framework
- **Lucide React**: Icon library for consistent iconography
- **React Hook Form**: Form state management and validation

## Development Tools
- **Vite**: Fast build tool and development server
- **TypeScript**: Type safety across the entire application
- **ESBuild**: Fast JavaScript bundler for production builds
- **Drizzle Kit**: Database migration and introspection tools

## Browser APIs
- **Geolocation API**: Location services for emergency features and health worker proximity
- **Web Speech API**: Voice input and output for accessibility
- **Notification API**: Browser notifications for medication reminders
- **Camera API**: QR code scanning for medicine verification

## Additional Services
- **Government Scheme Integration**: External APIs for healthcare scheme verification
- **Emergency Services**: Integration points for SOS calling and ambulance dispatch
- **Telephony**: Phone call integration for health worker communication