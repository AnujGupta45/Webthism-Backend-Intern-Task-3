# 🍽️ Restaurant Booking & Menu Management API

Hey there! 👋 Welcome to my backend internship project. This is a RESTful API built for managing restaurant operations, including menus, table bookings, and order processing. 

I built this project to get hands-on experience with backend architecture, database modeling, and secure authentication. It's designed to be modular, clean, and scalable!

## ✨ Features
- **Secure Authentication**: User signup and login with hashed passwords (bcrypt) and JWT-based session management.
- **Role-Based Access**: Separation of concerns between `Admin`/`Owner` and regular `User` roles.
- **Restaurant & Menu Management**: CRUD operations to create restaurants, add menu categories, and manage individual food items.
- **Booking & Order System**: Endpoints to place table bookings and food orders, track their statuses, and fetch user-specific histories.

## 🛠️ Tech Stack
- **Node.js** & **Express.js** — Fast and minimalist web framework.
- **MongoDB** & **Mongoose** — NoSQL database and object modeling. (Note: The local setup in this repo uses Prisma & SQLite, but the schema design is easily adaptable).
- **JWT (JSON Web Tokens)** — For secure, stateless authentication.
- **bcryptjs** — For hashing user passwords.
- **dotenv** — Environment variable management.

## 📂 Folder Structure
Here's a quick look at how the code is organized:

```text
backend/
├── config/         # Database connection setup
├── controllers/    # Core business logic for routes
├── middleware/     # JWT verification and role checks
├── models/         # Database schemas and models
├── routes/         # API endpoint definitions
├── utils/          # Helper functions and error handlers
├── .env            # Environment variables (not tracked in Git)
└── server.js       # Main application entry point
```

## 🚀 Installation Steps

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/restaurant-management-api.git
   cd restaurant-management-api
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Set up environment variables:**
   Create a `.env` file in the root directory (see the section below for details).

4. **Start the development server:**
   ```bash
   npm run dev
   ```
   The server should now be running on `http://localhost:5000`!

## 🔐 Environment Variables Setup
Create a `.env` file in the root directory and add the following keys:

```env
PORT=5000
MONGO_URI=mongodb+srv://<username>:<password>@cluster.mongodb.net/restaurant_db
JWT_SECRET=your_super_secret_jwt_key
```

## 🛣️ API Endpoints (Sample)

### Authentication
* `POST /api/auth/signup` - Register a new user
* `POST /api/auth/login` - Login and get JWT token

### Restaurants & Menus (Protected)
* `GET /api/restaurants` - Get all restaurants
* `POST /api/restaurants` - Create a new restaurant (Admin/Owner)
* `GET /api/menu/:restaurantId` - Get a restaurant's menu
* `POST /api/menu/item` - Add a new menu item (Admin/Owner)

### Bookings & Orders (Protected)
* `POST /api/bookings` - Book a table
* `GET /api/bookings/my-bookings` - View user booking history
* `POST /api/orders` - Place a food order

## 🗄️ Database Collections
* **Users**: Stores name, email, hashed password, and role.
* **Restaurants**: Stores restaurant details (name, address, cuisine) and links to the owner.
* **Menus & Items**: Stores categories and specific food items with prices and availability.
* **Bookings & Orders**: Links a user to a restaurant along with the reservation date or order items and total price.

## 🔄 Authentication Flow
1. A user signs up providing their details and password.
2. The password is encrypted using `bcrypt` before saving to the database.
3. Upon logging in, the server compares the credentials. If valid, a **JWT token** is generated and sent to the client.
4. For protected routes (like making a booking), the client must include the JWT token in the `Authorization` header as a Bearer token.
5. The `authMiddleware` intercepts the request, verifies the token, and grants access if valid.

## 🌱 Future Improvements
There's always room to grow! Here are some features I plan to add:
- Integration with Stripe for payment processing.
- Advanced search and filtering (e.g., finding restaurants by specific cuisines or location).
- Real-time order tracking using WebSockets (Socket.io).
- Automated email confirmations for bookings.

## 👨‍💻 Author
Built with ❤️ by **Anuj Gupta**  
Feel free to reach out to me on [LinkedIn](https://www.linkedin.com/in/anujgupta45/) or check out my other projects on [GitHub](https://github.com/AnujGupta45).
