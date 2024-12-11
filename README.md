# SecureKart

---

# MERN Stack E-commerce Backend

## Introduction

This repository contains the backend implementation for an e-commerce platform built using the **MERN stack**. The backend is responsible for managing APIs that handle user authentication, product management, order processing, and other server-side operations. The **frontend development is currently in progress**.

The main folder for the backend is the **`api`** directory, which houses all the backend logic, routes, and configurations.

## Features (Backend)

- **User Authentication**: Secure registration, login, and token-based authentication using JWT.
- **Product Management**: 
  - Fetch all products or retrieve individual product details.
- **Order Management**:
  - Place orders and update payment status.
  - Retrieve user-specific orders and individual order details.
- **Profile Management**: Get and update user profile securely.

## Technologies Used (Backend)

- **Node.js**: JavaScript runtime for building server-side applications.
- **Express.js**: Web framework for creating robust APIs.
- **MongoDB**: NoSQL database for data storage.
- **Mongoose**: ODM for MongoDB to interact with the database.
- **jsonwebtoken (JWT)**: Used for secure authentication and session management.
- **bcrypt.js**: For hashing passwords and ensuring data security.
- **Express-Async-Handler**: For efficient error handling in asynchronous operations.

## Backend Structure

- **`api/routes`**: Contains all the API routes (e.g., `users`, `products`, `orders`).
- **`api/models`**: MongoDB schemas and models.
- **`api/middleware`**: Middleware functions like authentication.
- **`api/server.js`**: Entry point for the backend server.

## API Endpoints

### User Routes
- `POST /api/users/login`: Authenticate a user and return a token.
- `POST /api/users`: Register a new user.
- `GET /api/users/profile`: Get user profile details (protected route).
- `PUT /api/users/profile`: Update user profile details (protected route).

### Product Routes
- `GET /api/products`: Retrieve all products.
- `GET /api/products/:id`: Retrieve product details by ID.

### Order Routes
- `POST /api/orders`: Place a new order (protected route).
- `PUT /api/orders/:id/payment`: Update order payment status (protected route).
- `GET /api/orders`: Retrieve all orders for the logged-in user (protected route).
- `GET /api/orders/:id`: Retrieve a specific order by ID (protected route).

## Installation and Setup (Backend)

### Prerequisites
- **Node.js**: Install from [Node.js official website](https://nodejs.org/).
- **MongoDB**: Ensure MongoDB is installed and running locally or on a cloud service.

### Steps to Run Backend Locally
1. Clone the repository:
   ```bash
   git clone <repository_url>
   cd <repository_name>/api
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Add environment variables:
   - Create a `.env` file in the `api` directory with the following:
     ```
     MONGO_URI=<Your MongoDB URI>
     JWT_SECRET=<Your JWT Secret>
     ```
4. Start the backend server:
   ```bash
   npm run server
   ```
5. Access the backend APIs at `http://localhost:3000/api`.

## Contribution

Contributions to the backend are welcome! To contribute:
1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature-name
   ```
3. Make changes and commit:
   ```bash
   git commit -m "Add new feature"
   ```
4. Push to your forked repository and create a pull request.


---