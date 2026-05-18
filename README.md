# Webthism Internship Task 3 - Restaurant API

This project contains the backend API for a restaurant booking and menu system as part of Week 3 tasks.

## Deliverables Completed:
1. **Database Schema Diagram**: See `schema-diagram.md` for the Mermaid ER diagram representing relationships between Users, Restaurants, Menus, Items, and Orders.
2. **Database Migration Files**: Built with Prisma and SQLite. Migrations are stored in `prisma/migrations/`.
3. **Working Authentication System**: Implemented `/api/auth/signup` and `/api/auth/login` using `bcryptjs` and `jsonwebtoken`.
4. **Clean Commits**: Initialized Git repository.

## Tech Stack
- **Node.js** with **Express.js**
- **Prisma ORM**
- **SQLite** database
- **JWT** (JSON Web Tokens) for authentication
- **Bcrypt.js** for password hashing

## Setup & Running the Project

1. Install dependencies:
   ```bash
   npm install
   ```

2. Run Database Migrations:
   ```bash
   npx prisma migrate dev
   ```

3. Start the server (Dev mode with Nodemon):
   ```bash
   npm run dev
   ```
   Or start normally:
   ```bash
   node server.js
   ```

## API Endpoints
- **GET /** : API Health Check
- **POST /api/auth/signup** : Register a new user
  - Body: `{ "name": "John Doe", "email": "john@example.com", "password": "password123", "role": "CUSTOMER" }`
- **POST /api/auth/login** : Login existing user
  - Body: `{ "email": "john@example.com", "password": "password123" }`
