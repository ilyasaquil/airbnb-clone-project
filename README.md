# Airbnb Clone Project

## Project Overview

The **Airbnb Clone Project** simulates a production-grade booking platform inspired by Airbnb.  
It covers backend systems, relational database design, API development, and deployment practices using industry tools.

## Project Goals

- Build a scalable backend system for a property booking application.
- Implement best practices: CI/CD, security, and modular architecture.
- Design an efficient relational database schema.
- Create secure, standards-compliant REST and GraphQL APIs.
- Simulate collaborative development with robust documentation.
  
## Team Roles

### Backend Developer
- Designs and maintains server-side logic, implements APIs, manages database interaction, authentication, and ensures overall performance and security.
### Database Administrator (DBA)
- Responsible for schema design, data integrity, performance tuning, query optimization, and database security.
### DevOps Engineer
- Automates build, test, and deployment pipelines. Manages environments with Docker and CI/CD tools like GitHub Actions.
### Security Engineer
- Implements authentication, authorization, data protection protocols, and regular security assessments.
### Project Manager
- Coordinates team activities, sets goals and milestones, assigns tasks, and ensures timely delivery of project objectives.
### QA Engineer
- Ensures application quality through test planning, execution, bug tracking, and validation of functional requirements.

## Technology Stack
- **Django** – Backend framework for scalable API development.
- **MySQL** – Relational database system.
- **GraphQL** – Flexible and efficient query language.
- **Docker** – Environment consistency through containerization.
- **GitHub Actions** – CI/CD automation for builds, tests, and deployments.

## Database Design
### Users
- `id`: Unique user ID  
- `name`, `email`: Identity and communication  
- `password_hash`: Secure credentials  
- `role`: `host` or `guest`

### Properties
- `id`, `owner_id`: Linked to hosting user  
- `title`, `description`, `location`: Listing details

### Bookings
- `id`, `property_id`, `user_id`: Booking metadata  
- `start_date`, `end_date`: Stay duration

### Reviews
- `id`, `property_id`, `user_id`: Review linkage  
- `rating`, `comment`: Guest feedback

### Payments
- `id`, `user_id`, `booking_id`: Payment source  
- `amount`, `payment_status`: Transaction details

### Entity Relationships
- A **User** (host) can list multiple **Properties**.
- A **User** (guest) can make multiple **Bookings**.
- **Bookings** link guests to specific **Properties**.
- **Reviews** are tied to guests and listings.
- **Payments** correspond to bookings by users.

## Feature Breakdown
### User Management
- Secure login, registration, and profile handling with role-based access control (guest or host).
### Property Management
- Hosts can create and manage listings with details like location, pricing, and availability.
### Booking System
- Guests can browse and reserve properties with real-time availability validation.
### Review and Rating System
- Guests submit ratings and comments after their stay, fostering platform trust.
### Payment Processing
- Secure financial transactions, including bookings and refunds, with end-to-end encryption.
### API Security
- Authentication, authorization, input validation, and rate limiting protect platform integrity.
### CI/CD Integration
- Automated pipelines streamline code testing, building, and deploying via GitHub Actions and Docker.

## API Security
### Authentication
- Verifies user identities and grants access to protected routes.
### Authorization
- Enforces permissions, restricting access to specific resources and actions.
### Rate Limiting
- Prevents abuse by capping API requests per user/IP over time.
### Data Encryption
- Secures data in transit using HTTPS.
### Input Validation and Sanitization
- Defends against SQL injection, XSS, and other threats by ensuring clean inputs.
### Security Importance
- Robust security is critical for protecting user data, ensuring reliable service, and building platform trust.  
