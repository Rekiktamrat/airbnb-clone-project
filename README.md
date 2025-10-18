# airbnb-clone-project

## Overview
The Airbnb Clone Project is a backend-focused learning project that simulates building a scalable booking platform similar to Airbnb.  
It aims to develop strong backend development, API design, and database management skills using Django, MySQL, and GraphQL.

## Project Goals
- Build a robust backend system for an Airbnb-like app  
- Implement database and API security best practices  
- Understand CI/CD pipelines and deployment workflows  
- Collaborate effectively using GitHub  

## Team Roles

### Backend Developer
Responsible for building and maintaining the backend logic, APIs, and integration with the database.

### Database Administrator (DBA)
Designs, manages, and optimizes the database schema and ensures data integrity and security.

### DevOps Engineer
Implements CI/CD pipelines, manages deployment environments, and ensures system reliability through automation.

### Security Engineer
Focuses on implementing security protocols such as authentication, authorization, and data encryption.

### Project Manager
Coordinates the team, manages timelines, and ensures all deliverables align with project objectives.


## Technology Stack

- **Django** – A Python web framework used to build RESTful APIs efficiently.  
- **MySQL** – A relational database for structured data management.  
- **GraphQL** – Enables flexible and efficient client-server data exchange.  
- **Docker** – For containerization and consistent deployment environments.  
- **GitHub Actions** – Used for automated CI/CD pipeline integration.


## Database Design

### Entities

1. **User**
   - id (PK)
   - name
   - email
   - password
   - role (host/guest)

2. **Property**
   - id (PK)
   - title
   - description
   - location
   - price_per_night
   - host_id (FK → User)

3. **Booking**
   - id (PK)
   - user_id (FK → User)
   - property_id (FK → Property)
   - check_in_date
   - check_out_date
   - total_amount

4. **Review**
   - id (PK)
   - user_id (FK → User)
   - property_id (FK → Property)
   - rating
   - comment

5. **Payment**
   - id (PK)
   - booking_id (FK → Booking)
   - amount
   - payment_status
   - payment_date

**Relationships**
- A User can have multiple Properties.  
- A Property can have many Bookings and Reviews.  
- A Booking belongs to one Property and one User.  
- Each Booking has one Payment.


## Feature Breakdown

### User Management
Users can register, log in, and manage their profiles. Hosts can list properties, while guests can book them.

### Property Management
Hosts can create, update, and delete property listings with details like images, descriptions, and pricing.

### Booking System
Guests can search for available properties, make reservations, and manage their bookings.

### Reviews and Ratings
Guests can review properties they’ve stayed in, helping build trust and reliability in the platform.

### Payment System
Handles secure transactions, payment confirmation, and refund processes.


## API Security

Key Security Measures:
- **Authentication** – Using JWT or OAuth2 for user identity verification.  
- **Authorization** – Restricts access to resources based on roles (e.g., host vs. guest).  
- **Rate Limiting** – Prevents abuse by limiting API request frequency.  
- **Data Encryption** – Secures sensitive data during transmission and storage.  
- **Input Validation** – Prevents SQL injection and other common attacks.

**Why Security Matters**
Protects user data, prevents unauthorized access, and ensures secure handling of payments and personal information.



## API Security

Key Security Measures:
- **Authentication** – Using JWT or OAuth2 for user identity verification.  
- **Authorization** – Restricts access to resources based on roles (e.g., host vs. guest).  
- **Rate Limiting** – Prevents abuse by limiting API request frequency.  
- **Data Encryption** – Secures sensitive data during transmission and storage.  
- **Input Validation** – Prevents SQL injection and other common attacks.

**Why Security Matters**
Protects user data, prevents unauthorized access, and ensures secure handling of payments and personal information.


## CI/CD Pipeline

**Continuous Integration (CI):** Automatically tests and validates new code on every push or pull request.

**Continuous Deployment (CD):** Automates deployment to production or staging environments after tests pass.

**Tools Used**
- **GitHub Actions** – Automates builds and tests.  
- **Docker** – Ensures consistent environments.  
- **Heroku / AWS** – Can be used for deploying the backend application.

**Importance**
CI/CD pipelines enhance reliability, speed up delivery, and minimize human errors during deployment.















## UI/UX Design Planning

### Design Goals
- Create intuitive booking flow
- Maintain visual consistency
- Ensure fast loading times
- Prioritize mobile responsiveness

### Key Features
- Property search and filtering
- Detailed property view
- Secure checkout process
- User authentication

| Page | Description |
|------|--------------|
| Property Listing View | Shows all listings in a grid with filters |
| Listing Detailed View | Shows property details, images, reviews |
| Simple Checkout View | Streamlined booking and payment page |

### Importance
A user-friendly design reduces booking friction and increases trust and satisfaction.





### Figma Design Specifications

**Colors**
- Primary: #FF5A5F
- Secondary: #008489
- Background: #FFFFFF
- Text: #222222
- Secondary Text: #717171

**Typography**
- Primary Font: Circular, Medium (500), 16px
- Headings: Circular, Bold (700), 24px–32px
- Secondary Text: Circular, Book (400), 14px

**Why this matters:**
Identifying design properties ensures a consistent and professional look across the app.
