﻿# Authorization_NodeJS
# User Authentication API

This API provides endpoints for user registration, login, password reset, change password, and retrieving logged-in user details.

This API provides endpoints for user registration, login, password reset, change password, and retrieving logged-in user details.

## Setup

1. Clone the repository to your local machine.
2. Install backend dependencies by navigating to the backend directory and running `npm install`.
3. Run the backend server using `npm run dev`. The server will start on port 8000.
4. Open the frontend directory in your code editor.
5. Ensure that your frontend application (index.html) is set to run on port 5500 using live server.

## Postman Collection

A Postman collection is included in the backend folder for testing the API endpoints.

1. Open Postman and import the provided collection (`ExpressAuthJWTAPI.postman_collection.json`).
2. Use the collection to test each API endpoint with different scenarios.

## Routes

### Public Routes

#### 1. User Registration

- **Route:** `POST /api/register`
- **Description:** Register a new user with provided details.
- **Request Body:**
  - `first_name`: User's first name.
  - `last_name`: User's last name.
  - `email`: User's email address.
  - `password`: User's password.
- **Response:** 
  - `message`: Success or error message.

#### 2. User Login

- **Route:** `POST /api/login`
- **Description:** Authenticate user and generate JWT token.
- **Request Body:**
  - `email`: User's email address.
  - `password`: User's password.
- **Response:**
  - `access_token`: JWT token for authenticated user.
  - `message`: Success or error message.

#### 3. Send Reset Password Email

- **Route:** `POST /api/send-reset-password-email`
- **Description:** Send email to user with password reset link.
- **Request Body:**
  - `email`: User's email address.
- **Response:**
  - `status`: Success or failure.
  - `message`: Success or error message.

#### 4. User Password Reset

- **Route:** `POST /api/reset-password/:id/:token`
- **Description:** Reset user's password using reset token.
- **Request Parameters:**
  - `id`: User's ID.
  - `token`: Reset token received in email.
- **Request Body:**
  - `password`: New password.
  - `password_confirmation`: Confirm new password.
- **Response:**
  - `status`: Success or failure.
  - `message`: Success or error message.

### Protected Routes

#### 1. Change User Password

- **Route:** `POST /api/changepassword`
- **Description:** Change user's password after authentication.
- **Request Body:**
  - `new_password`: New password.
  - `confirm_password`: Confirm new password.
- **Response:**
  - `status`: Success or failure.
  - `message`: Success or error message.

#### 2. Logged User Details

- **Route:** `GET /api/loggeduser`
- **Description:** Retrieve details of logged-in user.
- **Request Headers:**
  - `Authorization`: Bearer token.
- **Response:**
  - User details (first name, last name, email, etc.).


If stuck somewhere, Fell free to reach at [am6840957@gmail.com](am6840957@gmail.com)

