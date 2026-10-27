# Project Report: Secure Login System

## 1. Abstract
The Secure Login System is a beginner-friendly web application built with Python Flask and SQLite. It demonstrates account registration, secure password hashing, basic input validation, parameterized database queries, session-based login, protected dashboard access, and logout.

## 2. Problem Statement
Web applications need a reliable way to authenticate users and protect private pages. Storing plain-text passwords or accepting unvalidated inputs can put accounts at risk.

## 3. Objectives
- Provide registration and login pages.
- Store password hashes instead of plain-text passwords.
- Validate usernames and password confirmation.
- Use parameterized SQL queries to reduce SQL injection risk.
- Protect the dashboard using a login session.
- Support logout and session clearing.

## 4. Proposed System
The user registers with a unique username and password. The server validates the input and stores a password hash in SQLite. During login, the submitted password is checked against the stored hash. A valid login creates a session; only authenticated users can access the dashboard.

## 5. Modules
1. Registration module
2. Login/authentication module
3. Password hashing module
4. SQLite database module
5. Session management module
6. Protected dashboard and logout module
7. User interface module

## 6. Workflow
Start → Register account → Validate input → Hash password → Save user record → Login → Verify password hash → Create session → Open protected dashboard → Logout and clear session → End.

## 7. Technology Stack
- Python 3.9+
- Flask
- SQLite
- Werkzeug password hashing
- HTML and CSS

## 8. Security Features
- Passwords stored as scrypt hashes.
- Username validation and password confirmation.
- Parameterized SQL statements.
- Session-based access control.
- HttpOnly and SameSite session cookie settings.
- Logout clears the session.

## 9. Limitations
This is an educational mini project. It does not include two-factor authentication, password reset, email verification, login rate limiting, or full CSRF protection. Production systems require HTTPS, a strong secret key, security monitoring, CSRF protection, rate limiting, and a production WSGI server.

## 10. Expected Outcome
A working web app where users can create accounts, log in, view a protected dashboard, and log out. Passwords are not stored in plain text.

## 11. Conclusion
The project introduces core web authentication concepts and shows how password hashing, input validation, database parameterization, and session handling can improve account security.
