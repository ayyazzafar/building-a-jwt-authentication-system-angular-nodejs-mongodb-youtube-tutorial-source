# Angular JWT Authentication Demo

This repository contains the complete source code for the YouTube tutorial “[Build JWT Authentication with Angular & Node.js](https://youtu.be/wyvnIb-oiAo)”. The project demonstrates how to build a secure login and signup system using Angular for the frontend and Node.js (Express) for the backend, all secured with JWT-based authentication.

## Overview

The project is divided into two main parts:

### Backend (Node.js + Express)
- **API Endpoints:**
  - **POST /api/signup:** Register new users by securely hashing passwords using bcrypt.
  - **POST /api/login:** Authenticate users and return a JWT token on successful login.
  - **GET /api/profile:** A protected route that returns user profile data only when a valid JWT is provided.
- **Technologies:**
  - **Express:** Web framework for building the REST API.
  - **Mongoose:** MongoDB object modeling tool for schema definition and database interaction.
  - **JWT & bcrypt:** For generating tokens and hashing passwords securely.
  
### Frontend (Angular)
- **Pages:**
  - **Login Page:** Allows users to log in and stores the JWT token on successful authentication.
  - **Signup Page:** Provides a form for new users to register.
  - **Profile Page:** A protected route accessible only to authenticated users, displaying user profile data.
- **Features:**
  - **Angular Services:** Handles HTTP requests to the backend and manages authentication state.
  - **HTTP Interceptor:** Automatically attaches the JWT token to API requests.
  - **Route Guard:** Protects routes by ensuring only authenticated users can access them.
  - **Plain CSS:** Used for basic styling, ensuring a clean and modern UI.

## Prerequisites

- [Node.js](https://nodejs.org/) and npm installed.
- [MongoDB](https://www.mongodb.com/) running locally or a connection string for MongoDB Atlas.
- [Angular CLI](https://angular.io/cli) installed globally.

## Installation & Setup

### Backend Setup
1. Navigate to the `auth-backend` directory.
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the server:
   ```bash
   node server.js
   ```
   The server will run on `http://localhost:3000`.

### Frontend Setup
1. Navigate to the `auth-frontend` directory.
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the Angular development server:
   ```bash
   ng serve
   ```
   The app will be accessible at `http://localhost:4200`.

## How It Works

1. **User Registration:** New users register with their email and password. The password is hashed using bcrypt and stored securely in MongoDB.
2. **User Login:** Existing users log in. If credentials are valid, the backend returns a JWT token.
3. **Token Storage & Usage:** The Angular app stores the JWT token (typically in localStorage) and uses an HTTP interceptor to attach it to subsequent API requests.
4. **Protected Routes:** Angular’s AuthGuard checks for a valid token to allow access to protected routes such as the Profile page.
5. **Logout:** The user can log out, which clears the stored JWT and prevents access to protected routes.

## Video Tutorial

Watch the full tutorial on YouTube: [Build JWT Authentication with Angular & Node.js](https://youtu.be/wyvnIb-oiAo)

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contributing

Contributions, issues, and feature requests are welcome! Feel free to open an issue or submit a pull request.

---

Happy coding!