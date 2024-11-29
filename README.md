# RBAC Web Application

RBAC Web Application 
The RBAC (Role-Based Access Control) web application is designed to provide secure user authentication and authorization with user roles, ensuring access to certain pages or functionalities is restricted based on role permissions. Below are detailed insights into each aspect of the application:

---

## 🌟 Features

1. User Registration
Functionality: Allows new users to sign up by providing necessary details (e.g., email, password, username).
Validation: Ensures proper data input such as email format validation and password strength checks.
Backend Workflow:
Stores user details in the database with role defaults (e.g., guest or user).
Hashes passwords securely before saving using libraries like bcrypt.
2. User Login
Secure Authentication: Users log in with their credentials, which are verified against the database.
JWT: A token is issued to the user upon successful login, containing claims such as userId and role.
Token Storage: Tokens are stored securely in HTTP-only cookies, preventing cross-site scripting (XSS) attacks.
3. Role-Based Access Control
Role Management: Roles like admin, user, or viewer define access rights.
Access Restriction: Middleware on the backend intercepts API calls to verify user roles and grant/deny access to resources.
Use Cases:
Dashboard Access: Available only for admin or elevated roles.
Page Restrictions: Certain UI components are conditionally rendered based on the user role.
4. Modern UI with TailwindCSS
Responsive Design: The app adapts beautifully across various screen sizes.
Clean and Minimalistic: TailwindCSS simplifies styling and ensures consistent UI elements with minimal custom CSS.
User Feedback: Offers clear error/success messages for actions like login failures or restricted access.
5. Secure Token Management
HTTP-Only Cookies: Prevents tokens from being accessed by JavaScript on the client side.
Session Management: Tokens expire after a defined time to enhance security and prevent prolonged unauthorized access.
Refresh Tokens: Optionally implemented to extend sessions securely.

---

##  Technologies Used

Frontend
React:

Used to build dynamic and interactive user interfaces for the application.
Enables efficient component-based development, ensuring reusability and scalability.
React Router:

Implements seamless navigation and routing between pages, such as Login, Dashboard, and other restricted or public views.
Supports protected routes for role-based access, ensuring secure navigation.
TailwindCSS:

A utility-first CSS framework used to create a responsive, modern, and clean UI.
Simplifies styling by providing pre-designed utility classes, reducing the need for custom CSS.
Backend
Node.js:

Provides a JavaScript runtime environment for server-side development.
Handles asynchronous requests efficiently, enabling fast and scalable backend operations.
Express.js:

Simplifies backend development with an easy-to-use routing system and middleware support.
Used to create RESTful APIs for features like login, user registration, and role-based access.
Authentication
JWT (JSON Web Tokens):
Used to securely authenticate users by issuing signed tokens containing user details (e.g., roles).
Tokens are compact, portable, and tamper-proof, making them ideal for stateless authentication.
HTTP Requests
Axios:
A promise-based HTTP client for handling frontend-backend communication.
Used for making API calls like user login, registration, and fetching data from secured endpoints.

---


## 🛠️ Installation



   ```
   Navigate to frontend Directory then
   ```bash
   npm install
   npm start

   Similarly navigate to Backend Directory
   ```bash
   npm install
   npm start
   ```
   

