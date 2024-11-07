
# Blogging App

A full-featured blogging application built with the MERN (MongoDB, Express, React, Node.js) stack. This app includes authentication, user profiles, CRUD operations for posts and comments, and an admin panel.

## Features

- User authentication (login, register, and logout)
- JWT-based authentication with cookies
- Admin and user roles for managing content
- CRUD operations for blog posts and comments
- Responsive UI with React
- Image upload functionality
- User-specific blog views and interactions
- Search feature for blog posts

## Tech Stack

- **Frontend**: React, Axios
- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Authentication**: JWT and bcrypt for password hashing

## Getting Started

Follow these steps to set up the project locally:

### Prerequisites

- Node.js and npm installed
- MongoDB installed and running locally

### Installation

1. **Clone the repository**:
   ```bash
   [git clone https://github.com/your-username/blogging-app.git](https://github.com/saahmuskan/Blog-Market.git)
   cd Blog-Market
   ```

2. **Install dependencies** for both the client and server:
   ```bash
   cd client
   npm install
   cd ../server
   npm install
   ```

3. **Set up environment variables**:
   - In the `/server` directory, create a `.env` file with the following details:
     ```env
     MONGO_URI=mongodb://localhost:27017/bloggingApp
     PORT=8080
     SECRET=yourSecretKey
     DEV_MODE=development
     ```
   - In the `/client` directory, create a `.env` file with these details:
     ```env
     VITE_URL="http://localhost:8080"
     VITE_IF="http://localhost:8080/images/"
     ```

4. **Run MongoDB** if it's not running:
   ```bash
   mongod
   ```

5. **Run the server**:
   ```bash
   cd server
   npm run dev
   ```
   The server should be running at [http://localhost:8080](http://localhost:8080).

6. **Run the client**:
   ```bash
   cd client
   npm run dev
   ```
   The client should be running at [http://localhost:5173](http://localhost:5173).

### Usage

- Access the application in your browser at [http://localhost:5173](http://localhost:5173).
- Register or login to create, edit, or delete blog posts and comments.

### API Routes

The application exposes several routes on the backend to manage authentication, users, posts, and comments:

- **Authentication**: `/api/auth/` (login, register, logout)
- **User Management**: `/api/users/`
- **Posts**: `/api/posts/`
- **Comments**: `/api/comments/`

### Project Structure

```bash
blogging-app/
├── client/               # React frontend
├── server/               # Express backend
│   ├── config/           # Database configuration
│   ├── controllers/      # Route controllers
│   ├── models/           # Mongoose models
│   ├── routes/           # Express routes
│   └── verifyToken.js    # JWT middleware
├── .env                  # Environment variables
└── README.md
```

### Important Notes

- Ensure that MongoDB is running locally.
- Replace `yourSecretKey` in `.env` with a strong, random secret key.

### Troubleshooting

- **500 Internal Server Error on login**: Make sure `.env` variables are properly set up, especially `SECRET` and `MONGO_URI`.
- **CORS Issues**: Check that the CORS configuration in `server.js` matches the frontend's URL.
- **Token Errors**: Ensure cookies are set to `withCredentials: true` on the client-side requests.

## License

This project is licensed under the MIT License.
