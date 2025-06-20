# AirBnB Clone Project

This project is a simplified clone of the AirBnB web application, developed as part of the Holberton School curriculum.

## 🌟 Project Goals

- Recreate key features of the AirBnB platform.
- Practice building full-stack web applications.
- Gain experience with teamwork, version control, and agile practices.

## 🛠 Tech Stack

- **Languages**: Python3, JavaScript, HTML5, CSS3
- **Frameworks**: Flask
- **Database**: MySQL
- **Version Control**: Git & GitHub
- **Others**: Jinja2, API development

## 📁 Structure

- `models/`: Data models
- `web_static/`: Static files (HTML/CSS)
- `console.py`: Command-line interface

## 👥 Team Roles

In this project, we adopted a collaborative software development structure. Below are the key roles and responsibilities, adapted from our project goals and industry best practices as outlined by ITRexGroup:

### 🔧 Backend Developer
Responsible for building the server-side logic of the application. Implements APIs, connects to databases, handles business logic, and ensures the system performs efficiently.

### 🗃️ Database Administrator (DBA)
Manages the database architecture and ensures data is correctly structured, stored, backed up, and retrieved efficiently. Also monitors performance and optimizes queries.

### 🎨 Frontend Developer
Implements the visual elements of the application that users interact with. Converts design mockups into HTML/CSS and connects UI to backend via JavaScript and APIs.

### 🧪 QA Engineer (Quality Assurance)
Tests the application at various stages of development to ensure all features work as intended. Writes test cases, performs manual and automated testing, and reports bugs.

### 👩‍💼 Project Manager (PM)
Oversees the entire development process. Sets deadlines, ensures communication among team members, tracks progress, and makes sure the project meets the defined goals and timelines.

### 🧠 UX/UI Designer
Designs user interfaces that are intuitive and aesthetically pleasing. Focuses on the overall user experience, accessibility, and visual consistency.

### 📄 DevOps Engineer (optional in small teams)
Automates deployment, manages servers, monitors system health, and ensures continuous integration and delivery (CI/CD) pipelines are in place.

## 🛠 Technology Stack

Below is a breakdown of the technologies used in this project and their purpose:

### 🐍 Django
A high-level Python web framework that simplifies the process of building robust, secure web applications. Used for handling backend logic, URL routing, and server-side rendering.

### 🐘 PostgreSQL
A powerful, open-source object-relational database system used to store and manage application data. Chosen for its reliability and support for complex queries.

### 🔍 GraphQL
A query language for APIs that allows clients to request exactly the data they need. Used to optimize data fetching between the frontend and backend.

### 🌐 HTML5 & CSS3
Core web technologies used to structure and style the user interface of the application. Essential for responsive and accessible design.

### 💻 JavaScript
Used to add interactivity on the frontend, handle dynamic content updates, and communicate with the backend via API calls.

### 🧪 Pytest
A testing framework for Python used to ensure the reliability of backend logic through automated tests.

### 🐳 Docker
Containerization platform used to package the application and its dependencies, ensuring consistent environments across development and deployment.

### 🔁 Git & GitHub
Version control tools used for tracking changes, managing branches, and collaborating with team members.

## 🗄️ Database Design

The AirBnB Clone project requires a well-structured relational database. Below are the key entities, their essential fields, and how they relate to one another:

### 👤 Users
Represents the users of the platform.

- `id` (Primary Key)
- `name`
- `email`
- `password_hash`
- `date_joined`

**Relationships**:
- A user can own multiple properties.
- A user can make multiple bookings.
- A user can leave multiple reviews.
- A user can make multiple payments.

---

### 🏠 Properties
Represents listings posted by hosts.

- `id` (Primary Key)
- `title`
- `description`
- `location`
- `price_per_night`
- `host_id` (Foreign Key → Users)

**Relationships**:
- A property belongs to one user (host).
- A property can have multiple bookings.
- A property can have multiple reviews.

---

### 📅 Bookings
Represents reservations made by users.

- `id` (Primary Key)
- `property_id` (Foreign Key → Properties)
- `user_id` (Foreign Key → Users)
- `check_in_date`
- `check_out_date`
- `total_price`

**Relationships**:
- A booking is made by one user.
- A booking is for one property.

---

### ✍️ Reviews
Represents user feedback for properties.

- `id` (Primary Key)
- `user_id` (Foreign Key → Users)
- `property_id` (Foreign Key → Properties)
- `rating` (1–5)
- `comment`

**Relationships**:
- A review is made by one user.
- A review is for one property.

---

### 💳 Payments
Represents transactions made for bookings.

- `id` (Primary Key)
- `user_id` (Foreign Key → Users)
- `booking_id` (Foreign Key → Bookings)
- `amount`
- `payment_date`
- `payment_status`

**Relationships**:
- A payment is made by one user.
- A payment is tied to one booking.

## 🚀 Feature Breakdown

The Airbnb Clone project replicates key functionalities of the original Airbnb platform. Below is a breakdown of the core features and their roles in the system:

### 👤 User Management
Handles user registration, login, profile updates, and authentication. Ensures that each user has a secure account and can manage their own activities on the platform.

### 🏘️ Property Management
Allows hosts to list new properties with descriptions, images, prices, and availability. Hosts can edit or remove their listings, helping them maintain accurate and up-to-date rental options.

### 📅 Booking System
Enables users to select available dates and reserve properties. The system checks for conflicts, calculates pricing, and stores booking records linked to the user and property.

### 💬 Review System
Allows guests to leave ratings and comments after their stay. Reviews help future guests make informed decisions and encourage quality service from hosts.

### 💳 Payment Processing
Supports simulated payment workflows tied to confirmed bookings. This feature helps ensure that reservations are backed by a transaction, which is important for trust and accountability.

### 🔍 Search and Filtering
Provides users with the ability to search properties by location, price range, date availability, and more. This enhances the user experience by allowing quick discovery of suitable accommodations.

### 🛠 Admin Panel (optional)
For project or developer use, an admin panel can provide access to manage users, properties, and bookings directly. Useful for testing, debugging, and backend control.

