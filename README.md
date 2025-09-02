# Airbnb Clone Project
This repository contains the project blueprint for a comprehensive, real-world Airbnb clone. The primary goal is to design and document the backend systems, database structure, API, and security for a robust booking platform. This project focuses on planning a scalable web application before implementation.
The tech stack for this project includes Django, MySQL, GraphQL, Docker, and GitHub Actions.

## Team Roles
Based on the project overview and insights from the ITRexGroup blog, the team roles are as follows:

### Backend Developer: Responsible for building the server-side logic, developing the RESTful APIs using Django, and ensuring the application performs well.
### Database Administrator: Manages the MySQL database, including designing the schema, ensuring data integrity, and optimizing queries for performance.
### DevOps Engineer: Oversees the CI/CD pipeline using GitHub Actions and Docker, automating the build, testing, and deployment processes to ensure smooth and efficient releases.
### Security Specialist: Focuses on implementing and documenting API security measures, protecting user data, and securing payment transactions.

## Technology Stack
This project uses a modern technology stack to build a scalable and efficient application.

### Django: A high-level Python web framework used for building the backend and RESTful APIs quickly and securely.
### MySQL: A reliable open-source relational database used to store and manage all application data, including users, properties, and bookings.
### GraphQL: A query language for APIs that enables the frontend to request exactly the data it needs, improving efficiency.
### Docker: A containerization platform used to package the application and its dependencies, ensuring consistency across development and production environments.
### GitHub Actions: A CI/CD tool used to automate workflows for building, testing, and deploying the application directly from the GitHub repository

## Database Design
The database will be structured around several key entities to manage the platform's data effectively.

### Users: Manages user accounts and personal information.
### Fields: user_id, username, email, password_hash, full_name.
### Properties: Contains details about the listings available for rent.
### Fields: property_id, owner_id (foreign key to Users), title, description, price_per_night.
A User can have multiple Properties.
### Bookings: Stores information about reservations made by users.
### Fields: booking_id, user_id (foreign key to Users), property_id (foreign key to Properties), start_date, end_date.
A Booking belongs to one Property and one User.
### Reviews: Holds user feedback for properties.
### Fields: review_id, booking_id (foreign key to Bookings), rating, comment.
### Payments: Tracks payment information for bookings.
### Fields: payment_id, booking_id (foreign key to Bookings), amount, status, timestamp.

## Feature Breakdown
The application will include the following core features to provide a complete user experience:
### User Management: This feature handles user registration, login, and profile management. It's the foundation of the platform, enabling secure access and personalized experiences for users.
### Property Management: Allows property owners to list, edit, and manage their properties. This includes uploading photos, setting prices, and describing amenities, which is essential for attracting renters.
### Booking System: Enables users to search for properties, check availability, and make reservations. This is the core business logic of the application, directly facilitating transactions between renters and owners.


