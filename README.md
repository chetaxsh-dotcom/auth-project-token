# 🔐 User Authentication & Authorization with Bearer Token

A secure backend authentication system built using **Node.js, Express.js, MongoDB Atlas, JWT, and bcrypt**.

This project demonstrates how to implement user registration, login, password hashing, JWT-based authentication, protected routes, and deployment using industry best practices.

---

## 🚀 Live Deployment

🌍 Deployed on Render  
👉 https://your-render-url.onrender.com

---

## 🛠 Tech Stack

- Node.js
- Express.js
- MongoDB Atlas
- Mongoose
- JSON Web Token (JWT)
- bcryptjs
- dotenv
- Render (Deployment)

---

## 📂 Project Structure (MVC Pattern)

```
project-root/
│
├── controllers/
│   └── authController.js
│
├── middleware/
│   └── authMiddleware.js
│
├── models/
│   └── User.js
│
├── routes/
│   └── authRoutes.js
│
├── server.js
├── package.json
└── .env
```

---

## 🔑 Features

✔ User Registration  
✔ Password Hashing using bcrypt  
✔ User Login  
✔ JWT Token Generation  
✔ Bearer Token Authorization  
✔ Protected Routes  
✔ Token Expiration (1 Hour)  
✔ MongoDB Atlas Cloud Database  
✔ MVC Architecture  
✔ Environment Variable Configuration  
✔ Production Deployment on Render  

---

## 📌 API Endpoints

### 1️⃣ Register User

```
POST /api/auth/register
```

**Body (JSON):**
```json
{
  "username": "chetan",
  "email": "chetan@gmail.com",
  "password": "123456"
}
```

---

### 2️⃣ Login User

```
POST /api/auth/login
```

**Body (JSON):**
```json
{
  "email": "chetan@gmail.com",
  "password": "123456"
}
```

**Response:**
```json
{
  "message": "Login successful",
  "token": "your_jwt_token_here"
}
```

---

### 3️⃣ Get Logged In User (Protected Route)

```
GET /api/auth/me
```

**Headers Required:**
```
Authorization: Bearer your_jwt_token_here
```

**Response Example:**
```json
{
  "id": "6999b5dfada3874086db6382",
  "email": "chetan@gmail.com",
  "iat": 1771693550,
  "exp": 1771697150
}
```

---

## 🔐 Authentication Flow

1. User registers → Password is hashed using bcrypt.
2. User logs in → JWT token is generated.
3. Token contains user ID and email.
4. Client sends token in Authorization header:
   ```
   Bearer <token>
   ```
5. Middleware verifies token before allowing access to protected routes.
6. Token expires automatically after 1 hour.

---

## ⚙ Environment Variables

Create a `.env` file in the root directory:

```
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_secret_key
```

⚠ Never commit `.env` file to GitHub.

---

## 💻 Installation & Setup

Clone the repository:

```
git clone https://github.com/your-username/your-repo-name.git
```

Install dependencies:

```
npm install
```

Run in development mode:

```
npm run dev
```

Run in production:

```
npm start
```

---

## 🧠 Learning Objectives

This project demonstrates:

- Secure password storage
- Stateless authentication using JWT
- Middleware-based route protection
- REST API best practices
- Environment variable security
- Cloud database integration
- Deployment of backend applications

---

## 🌟 Future Improvements

- Role-based authorization (Admin/User)
- Refresh token implementation
- Email verification
- Password reset functionality
- Frontend integration (React)

---

## 📜 License

This project is created for educational and portfolio purposes.

## Author 🥷 --

## Chetan sharma ##
