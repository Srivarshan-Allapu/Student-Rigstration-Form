Here’s the text for the README file:  

---

# Student Registration System

## Overview
The **Student Registration System** is a Java-based desktop application designed for managing student registration, login, and data storage with a PostgreSQL database. It provides a user-friendly GUI using the Swing framework for registration, login, and viewing student details.

---

## Features

1. **Registration Page:**
   - Collects personal, familial, and address details.
   - Validates passwords and allows password creation.
   - Saves data to a PostgreSQL database.

2. **Login Page:**
   - Secure login functionality.
   - Password visibility toggle.
   - "Forgot Password" feature for recovery using security questions.

3. **Details Page:**
   - Displays all stored student details after successful login.

4. **Forgot Password:**
   - Verifies the user via a security question.
   - Allows resetting the password securely.

---

## Technologies Used

- **Java (Swing Framework):** For GUI development.
- **PostgreSQL:** Database management.
- **JDBC:** For connecting Java with the PostgreSQL database.

---

## Prerequisites

1. Java Development Kit (JDK) 8 or higher.
2. PostgreSQL installed and running.
3. PostgreSQL JDBC Driver (v42.7.1).

---

## Setup Instructions

1. **Database Configuration:**
   - Create a PostgreSQL database named `java gui`.
   - Run the following SQL script to create the required table:
     ```sql
     CREATE TABLE Students (
         "Full Name" VARCHAR(100),
         "Hall No" VARCHAR(10),
         "Phone No" VARCHAR(15),
         "Father Name" VARCHAR(100),
         "Father Occupation" VARCHAR(100),
         "Mother Name" VARCHAR(100),
         "Mother Occupation" VARCHAR(100),
         "Gender" VARCHAR(10),
         "Password" VARCHAR(100),
         "Email" VARCHAR(100) UNIQUE,
         "Date of Birth" VARCHAR(20),
         "Country" VARCHAR(50),
         "State" VARCHAR(50),
         "City" VARCHAR(50),
         "Village" VARCHAR(50),
         "Pincode" VARCHAR(10),
         "House No" VARCHAR(50),
         "Religion" VARCHAR(50),
         "Caste" VARCHAR(50),
         "Caste Name" VARCHAR(50),
         "Blood Group" VARCHAR(10),
         "Identification Marks1" VARCHAR(200),
         "Identification Marks2" VARCHAR(200),
         "security_question" VARCHAR(200),
         "answer" VARCHAR(200)
     );
     ```

2. **Driver Configuration:**
   - Ensure the PostgreSQL JDBC driver (`postgresql-42.7.1.jar`) is available in your classpath.

3. **Code Configuration:**
   - Update the following constants in `project.java` with your database credentials:
     ```java
     private static final String DB_URL = "jdbc:postgresql://<your-host>:<your-port>/<your-database>";
     private static final String DB_USER = "<your-username>";
     private static final String DB_PASSWORD = "<your-password>";
     ```

4. **Running the Application:**
   - Compile the Java file:
     ```bash
     javac project.java
     ```
   - Run the application:
     ```bash
     java project
     ```

---

## Usage

1. **Register a New User:**
   - Fill in the form and click "Register."
   - Ensure all fields are complete and passwords match.

2. **Login:**
   - Enter your email and password.
   - Use "Forgot Password" if you cannot log in.

3. **View Details:**
   - After logging in, view your personal and contact details.

---

## Troubleshooting

1. **Database Connection Issues:**
   - Ensure PostgreSQL is running.
   - Verify database credentials in the code.

2. **Driver Not Found:**
   - Make sure the PostgreSQL JDBC driver is properly added to the classpath.

3. **GUI Not Launching:**
   - Ensure Java is installed and properly configured.

---

## Future Enhancements

1. Adding role-based access control.
2. Encrypting sensitive data in the database.
3. Deploying the application as a web-based service.

---

## License
This project is open-source and free to use under the MIT License.
