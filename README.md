# airbnb-clone-project

## 🏠 Project Overview
The **AirBnB Clone Project** aims to replicate the core functionalities of the AirBnB platform — allowing users to create, view, and book listings. The project will focus on both backend logic and frontend integration, simulating a real-world web application environment.

### 🎯 Project Goals
- Build a scalable and maintainable web application.
- Implement CRUD operations for users, places, and bookings.
- Learn collaboration and version control using Git and GitHub.
- Develop both frontend and backend components as a team.

### 🧰 Tech Stack
- **Backend:** Python, Flask (or Django)
- **Frontend:** HTML, CSS, JavaScript
- **Database:** MySQL (or PostgreSQL)
- **Version Control:** Git & GitHub
- **Deployment:** Docker / AWS (optional for later stages)

---

## 👥 Team Roles

### 1. Backend Developer
Responsible for developing the core application logic, API endpoints, and integrations between the database and frontend.

### 2. Frontend Developer
Designs and implements the user interface, ensuring the website is responsive, user-friendly, and visually appealing.

### 3. Database Administrator (DBA)
Designs and manages the database schema, handles migrations, ensures data integrity, and optimizes database performance.

### 4. DevOps Engineer
Handles deployment, continuous integration (CI/CD), version control, and server configurations.

### 5. QA Engineer / Tester
Tests all system components to ensure they meet project requirements and quality standards.

### 6. Project Manager
Oversees project progress, assigns tasks, manages deadlines, and facilitates team communication.

---

## ⚙️ Technology Stack

Below is a list of the key technologies and tools used in this project, along with their specific roles.

### 🐍 Python
A powerful, high-level programming language used for backend development. It helps in building robust logic for handling user authentication, data management, and server-side operations.

### 🌐 Django
A high-level Python web framework that simplifies building scalable web applications. It’s used to manage URL routing, handle requests/responses, and structure the project in an organized MVC pattern.

### 🗃️ PostgreSQL
An open-source relational database management system (RDBMS). It stores structured data like users, properties, and booking information, providing efficient data retrieval and relationships.

### 🔄 GraphQL
A query language for APIs that allows clients to request exactly the data they need. It improves data fetching efficiency between the frontend and backend.

### 🧱 HTML5
The standard markup language for structuring web pages and web applications. It defines the content layout for the AirBnB Clone interface.

### 🎨 CSS3
Used to style the frontend interface — controls the layout, colors, fonts, and responsiveness, ensuring a visually appealing user experience.

### ⚡ JavaScript
Adds interactivity to the web application, enabling dynamic elements like form validation, booking actions, and smooth page updates without reloading.

### 🐳 Docker
A containerization tool that ensures the application runs smoothly in any environment by packaging all dependencies together.

### 🧩 Git & GitHub
Used for version control and collaboration. Git tracks code changes, while GitHub hosts the project repository and manages team contributions.

### ☁️ AWS (Amazon Web Services)
Optional for deployment — provides cloud hosting for the web application, ensuring scalability and reliability.

---

## 🗄️ Database Design

The database for the AirBnB Clone Project is designed to efficiently store and manage information related to users, properties, bookings, reviews, and payments.  
It uses **PostgreSQL** as the primary database system.

### 🧍‍♂️ 1. Users
Represents the individuals using the platform — both hosts and guests.

**Key Fields:**
- `id`: Unique identifier for each user.
- `name`: Full name of the user.
- `email`: User’s email address (unique).
- `password_hash`: Encrypted user password.
- `role`: Defines if the user is a host or guest.

**Relationships:**
- A **user** can list multiple **properties**.
- A **user** can make multiple **bookings**.
- A **user** can write multiple **reviews**.

---

### 🏠 2. Properties
Represents the listings (apartments, houses, rooms) that users can rent.

**Key Fields:**
- `id`: Unique identifier for each property.
- `title`: The name or headline of the listing.
- `description`: Details about the property.
- `location`: Address or city of the property.
- `price_per_night`: Rental cost per night.
- `host_id`: References the user who owns the property.

**Relationships:**
- A **property** belongs to one **user (host)**.
- A **property** can have multiple **bookings** and **reviews**.

---

### 📅 3. Bookings
Tracks reservation details between guests and property owners.

**Key Fields:**
- `id`: Unique identifier for each booking.
- `user_id`: References the user (guest) who made the booking.
- `property_id`: References the property being booked.
- `check_in`: Start date of the booking.
- `check_out`: End date of the booking.
- `status`: Indicates whether the booking is pending, confirmed, or cancelled.

**Relationships:**
- A **booking** belongs to one **user** and one **property**.
- A **booking** can have one **payment record**.

---

### 💬 4. Reviews
Stores user feedback and ratings for properties.

**Key Fields:**
- `id`: Unique identifier for each review.
- `user_id`: References the reviewer.
- `property_id`: References the reviewed property.
- `rating`: Numeric score (e.g., 1–5).
- `comment`: Text feedback from the user.

**Relationships:**
- A **review** belongs to one **user** and one **property**.

---

### 💳 5. Payments
Handles transaction records for confirmed bookings.

**Key Fields:**
- `id`: Unique payment identifier.
- `booking_id`: References the booking related to this payment.
- `amount`: Payment amount.
- `payment_date`: Timestamp of when payment was made.
- `payment_method`: e.g., credit card, PayPal, etc.
- `status`: Indicates if payment was successful, pending, or failed.

**Relationships:**
- A **payment** belongs to one **booking**.
- A **booking** can have one **payment**.

---

### 🔗 Entity Relationships Summary

- A **User** can own multiple **Properties**.  
- A **Property** can have multiple **Bookings** and **Reviews**.  
- A **Booking** belongs to one **User** and one **Property**.  
- A **Booking** can have one **Payment**.  
- A **Review** belongs to one **User** and one **Property**.

---

### 📊 Visual Summary (Optional Later)
When you advance, you can add an **ERD (Entity Relationship Diagram)** showing these tables and their relationships using tools like **draw.io**, **Lucidchart**, or **dbdiagram.io**.
