# Overview of AirBnB Clone
## Objective
   The backend for the Airbnb Clone project is designed to provide a robust and scalable foundation for managing user interactions, property listings, bookings, and payments. This backend will support various functionalities required to mimic the core features of Airbnb, ensuring a smooth experience for users and hosts.
## Project goals
   - **User Management**: Implement a secure system for user registration, authentication, and profile management.

   - **Property Management**: Develop features for property listing creation, updates, and retrieval.

   - **Booking System**: Create a booking mechanism for users to reserve properties and manage booking details.

   - **Payment Processing**: Integrate a payment system to handle transactions and record payment details.

   - **Review System**: Allow users to leave reviews and ratings for properties.

   - **Data Optimization**: Ensure efficient data retrieval and storage through database optimizations.


## Features Overview
- ### API Documentation
    - **OpenAPI Standard**: The backend APIs are documented using the OpenAPI standard to ensure clarity and ease of integration.
    - **Django REST Framework**: Provides a comprehensive RESTful API for handling CRUD operations on user and property data.
    - **GraphQL**: Offers a flexible and efficient query mechanism for interacting with the backend.
- ### User Authentication
    - **Endpoints**: `/users/`, `/users/{user_id}/`
    - **Features**: Register new users, authenticate, and manage user profiles.

- ### Property Management
    - **Endpoints**: `/properties/`, `/properties/{property_id}/`
    - **Features**: Create, update, retrieve, and delete property listings.

- ### Booking System
    - **Endpoints**: `/bookings/`, `/bookings/{booking_id}/`
    - **Features**: Make, update, and manage bookings, including check-in and check-out details.

- ### Payment Processing
    - **Endpoints**: `/payments/`
    - **Features**: Handle payment transactions related to bookings.

- ### Review System
    - **Endpoints**: `/reviews/`, `/reviews/{review_id}/`

- ### Database Optimizations
    - **Indexing**: Implement indexes for fast retrieval of frequently accessed data.
    - **Caching**: Use caching strategies to reduce database load and improve performance.

## Team Roles

- **Business analyst (BA)**:s Defines project requirements and translates them into technical specifications.
- **Project manager (PM)**: Oversees the project, ensuring timely delivery and adherence to project requirements.
- **UI/UX designer**: Transforms a product vision into user-friendly designs, Creates user journeys for the best user experience and highest conversion rates
- **Frontend Developer**: Develops the user interface, ensuring a responsive and interactive experience.
- **Backend Developer**: Responsible for implementing API endpoints, database schemas, and business logic.
- **Database Administrator**: Manages database design, indexing, and optimizations.
- **DevOps Engineer**: Handles deployment, monitoring, and scaling of the backend services.
- **QA Engineer**: Ensures the backend functionalities are thoroughly tested and meet quality standards.

## Technology Stack
- **Django**: A high-level Python web framework used for building the RESTful API.
- **Django REST Framework**: Provides tools for creating and managing RESTful APIs.
- **PostgreSQL**: A powerful relational database used for data storage.
- **GraphQL**: Allows for flexible and efficient querying of data.
- **Celery**: For handling asynchronous tasks such as sending notifications or processing payments.
- **Redis**: Used for caching and session management.
- **Docker**: Containerization tool for consistent development and deployment environments.
- **CI/CD Pipelines**: Automated pipelines for testing and deploying code changes.

## Database Design
- ### Users
    - **Fields**: email, password, first_name, last_name, 
    - **relationships**: can have many bookings, can have many reviews, can have many properties, can have many payments
- ### Properties
    - **Fields**: name, description, address, price_per_night, max_guests, 
    - **relationships**: can have many bookings, can have many reviews, can have many payments
- ### Bookings
    - **Fields**: start_date, end_date, total_price, 
    - **relationships**: belongs to a property, belongs to a user
- ### Reviews
    - **Fields**: rating, comment,
    - **relationships**: belongs to a property, belongs to a user

- ### Payments
    - **Fields**: amount, payment_method, status,
    - **relationships**: belongs to a booking, belongs to a user
    