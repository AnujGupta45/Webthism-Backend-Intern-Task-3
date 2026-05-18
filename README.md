# Webthism Internship - Task 3 (Backend) 🚀

Hello! I'm **Anuj Gupta**, and this is my submission for Week 3 of the Backend Development Internship at Webthism. 

For this task, I was assigned to build the backend for a **Restaurant Booking & Menu Management System**. This project really helped me apply my theoretical knowledge and practice building RESTful APIs, designing databases, and handling secure user authentication.

## 📚 What I Learned & Implemented
During this task, I got hands-on experience with:
- **API Development**: Creating modular REST endpoints using `Node.js` and `Express.js`.
- **Database Design**: Planning and connecting tables (Users, Restaurants, Menus, Orders) using `Prisma ORM` and `SQLite`. I also drew out an Entity-Relationship (ER) diagram for this structure!
- **Security**: Setting up user registration and login endpoints, hashing passwords securely using `bcryptjs`, and handling sessions with `JSON Web Tokens (JWT)`.

## 🛠️ Tech Stack Used
- **Node.js** & **Express.js** 
- **Prisma ORM** & **SQLite**
- **JWT (jsonwebtoken)**
- **Bcrypt.js** 

## 📂 Project Structure
Here is how I organized my code:
```text
/ 
├── controllers/      # Logic for the routes (like authController.js)
├── prisma/           # Database schema and migration files
├── routes/           # API route definitions
├── schema-diagram.md # The ER Diagram for my database design
├── .env              # Environment variables
└── server.js         # Main server entry point
```

## 🚀 How to Run My Code Locally

If you want to test my code on your machine, just follow these steps:

1. **Clone the repo:**
   ```bash
   git clone https://github.com/AnujGupta45/Webthism-Backend-Intern-Task-3.git
   cd Webthism-Backend-Intern-Task-3
   ```
2. **Install all packages:**
   ```bash
   npm install
   ```
3. **Set up the database:** (This will run the Prisma migrations)
   ```bash
   npx prisma migrate dev
   ```
4. **Start the server:**
   ```bash
   npm run dev
   ```
   *The server will start running at `http://localhost:5000`.*

## 🔗 How to Test the Endpoints
You can use Postman or Thunder Client to test the authentication system I built:
- **Server Check**: `GET http://localhost:5000/`
- **Signup**: `POST http://localhost:5000/api/auth/signup`
  *(Requires JSON body: name, email, password)*
- **Login**: `POST http://localhost:5000/api/auth/login`
  *(Requires JSON body: email, password)*

## 👨‍🎓 About Me
Built by **Anuj Gupta** as part of the Webthism Internship Program.
- Let's connect on LinkedIn: [Anuj Gupta](https://www.linkedin.com/in/anujgupta45/)
- Check out my GitHub: [AnujGupta45](https://github.com/AnujGupta45)

*Thank you to the mentors at Webthism for the task!*
