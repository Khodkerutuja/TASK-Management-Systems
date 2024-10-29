# Task Management System

## Introduction

The **Task Management System** is a web application designed for collaborative team projects, allowing users to manage various tasks within a team efficiently. It is developed using Spring Boot for the backend and Angular v7 for the frontend, with a MySQL database for data persistence.

This project focuses primarily on handling document-based projects, where each "User" can be part of multiple Programs, and each Program can have several User members associated with it. The application includes robust security through JWT-based Authentication for all APIs, ensuring secure access and operations.

> **Note**: The project is in an early development stage and requires further enhancements and bug fixes for production use. However, it can serve as a valuable template for learners and contributors interested in building a functional task management application.

## TODO

- UI/UX improvements
- New features: Program settings, custom project themes, user settings, and edit options
- Pagination for task lists and user picker lists for better user experience

## Dependencies

- **Java 8 JDK**
- **Embedded Tomcat 9 server**
- **MySQL Database**
- **Node Package Manager (NPM)**
- **Maven**

## Installation

### Backend Setup

1. **Clone the Repository**: Clone the repository and open the backend project in **Eclipse** or a similar IDE.
   
2. **Import as a Maven Project**:
   - Choose the "Import Existing Maven Project" option to import the backend module.
   - Build the Maven project to install all required dependencies.

3. **Set Up the MySQL Database**:
   - Install MySQL and create a new database (e.g., `tms`).
   - Update the following fields in the `application.properties` file located in the `/resources` folder:
     ```properties
     spring.datasource.url=jdbc:mysql://localhost:3306/tms
     spring.datasource.username=root
     spring.datasource.password=root
     ```

4. **Email Configuration**:
   - Configure email services via SMTP for functionalities requiring email notifications. Update the following fields in `application.properties`:
     ```properties
     spring.mail.host=smtp.gmail.com
     spring.mail.smtp.ssl.trust=smtp.gmail.com
     spring.mail.port=587
     spring.mail.transport.protocol=smtp
     spring.mail.username=your.email@gmail.com
     spring.mail.password=your-email-password
     ```
   - For additional support, refer to [Google SMTP common issues](https://support.google.com/mail/answer/7126229).

5. **Run the Backend**:
   - Run the application using `BackendApplication.java` in your IDE. The required database tables will initialize upon first run.
   - Execute `roles.sql` on your MySQL database to configure necessary user roles.

### Frontend Setup

1. **Install Node.js**: Ensure Node.js is installed on your system.

2. **Run the Frontend**:
   - Navigate to the `frontend` directory in the command prompt.
   - Use `npm start` (instead of `ng serve`) as a custom port number (8001) is configured for the frontend.
   - Open the application at [http://localhost:8001](http://localhost:8001) in your browser (only for development).

## Project Structure

```plaintext
task-management-system/
├── backend/
│   ├── src/
│   └── BackendApplication.java
├── frontend/
│   ├── src/
│   └── index.html
└── README.md
