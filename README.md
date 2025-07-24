# Secure Password Reset System

This project was developed during my internship to allow employees to reset their Active Directory passwords securely without contacting the IT department. The application is built using **Java** and **Spring Boot**, with identity verification handled through an **H2 database**, and password reset operations performed via **PowerShell** commands integrated through **LDAP**.

## Features
- Identity verification using TC ID, registry number, or username
- Secure random password generation (uppercase, lowercase, digit, special character)
- LDAP connection to Active Directory
- Password reset via PowerShell (executed from Java with `ProcessBuilder`)
- HTML form interface for user interaction
- Localhost testing (port 8080)
- Simulated data via H2 database

## Technologies Used
- **Java** (Spring Boot, Lombok)
- **H2 Database**
- **LDAP** (Javax)
- **PowerShell**
- **HTML**
- **Postman** – for API testing
- **draw.io** – system flowchart

## Project Structure
- `ResetControllerV2`: Handles HTTP requests
- `AuthService`: Verifies user identity
- `ActiveDirectoryService`: Connects to AD and resets password
- `RandomPasswordServiceGenerator`: Creates secure passwords
- `application.properties`: Configuration for DB and LDAP
- `LDIF`: Used for LDAP structure definition

## Notes
Due to internal security policies, real user data could not be accessed. The system was tested using a simulated environment with an H2 in-memory database. LDAP integration and PowerShell-based password reset were successfully implemented. The application is currently stored in a private GitHub repository and will be shared publicly.
