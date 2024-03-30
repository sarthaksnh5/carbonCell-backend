# Carbon Cell Backend Application

This repository contains the backend application for Carbon Cell, a Node.js application with three APIs: user registration, user login, and accessing public data from authenticated public APIs.

## APIs

### 1. User Registration

Endpoint: `/register`

- Method: `POST`
- Description: Register a new user.
- Request Body:
  - `fullName`: Full name of the user.
  - `email`: Email address of the user.
  - `password`: Password for the user account.
- Response:
  - `201`: Successful registration. Returns a user instance.

### 2. User Login

Endpoint: `/login`

- Method: `POST`
- Description: Authenticate and login an existing user.
- Request Body:
  - `email`: Email address of the user.
  - `password`: Password for the user account.
- Response:
  - `200`: Successful login. Returns a JSON Web Token (JWT) for authentication.

### 3. Get Public API Data

Endpoint: `/public-api`

- Method: `GET`
- Description: Fetch data from a public API.
- Authentication: JWT token in the header.
- Query Parameters (Optional):
  - `title`: Filter by title.
  - `category`: Filter by category.
  - `description`: Filter by description.

## Libraries Used

- **Queryman**: Library for handling query parameters.
- **Express**: Web application framework for Node.js.
- **Bcrypt**: Library for hashing passwords securely.
- **BodyParser**: Middleware for parsing request bodies.
- **JsonWebToken**: Library for generating and verifying JSON Web Tokens for authentication.
- **MongoDB**: Database used for storing user information.

## Usage

1. Clone the repository.
2. Install dependencies: `npm install`.
3. Start the server: `npm start`.

## Authentication

To access the public API, include the JWT token in the header of your request.

Example:
```
Authorization: your_token_here
```

## Database

This application uses MongoDB as the database to store user information. Make sure you have MongoDB installed and running on your system.

## Contributions

Contributions are welcome! Feel free to submit issues or pull requests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.