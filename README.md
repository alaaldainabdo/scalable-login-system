# 🔐 Scalable Login System

A production-ready, scalable authentication system built using **Node.js**, **Express**, **MongoDB**, **JWT**, and **bcrypt**.  
This project demonstrates how to build a secure, scalable, and maintainable login & registration backend API.

---

## 🚀 Features

✔ User Registration  
✔ User Login  
✔ Hashed Passwords with bcrypt  
✔ JWT Authentication (Access Token)  
✔ MongoDB Database Integration  
✔ Modular Code Structure  
✔ Environment Variables Support  
✔ Error Handling  
✔ Ready for Scaling (Load Balancers, Replicas, Horizontal Scaling)

---

## 📁 Project Structure

```

scalable-login-system/
│── models/
│   └── users.js
│── routes/
│   └── auth.js
│── .env
│── server.js
│── package.json
│── README.md

```

---

## ⚙️ Technologies Used

| Tech             | Purpose                     |
| ---------------- | --------------------------- |
| **Node.js**      | Backend runtime             |
| **Express**      | Web framework               |
| **MongoDB**      | NoSQL database              |
| **Mongoose**     | ODM for MongoDB             |
| **bcrypt**       | Password hashing            |
| **jsonwebtoken** | Token generation            |
| **CORS**         | Allow cross-origin requests |
| **dotenv**       | Environment variables       |

---

## 🔧 Installation & Setup

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/alaaldainabdo/scalable-login-system.git
cd scalable-login-system
```

### 2️⃣ Install Dependencies

```bash
npm install
```

### 3️⃣ Create a `.env` File

```
MONGO_URI=mongodb://localhost:27017/scalable-login
JWT_SECRET=your_jwt_secret_key
PORT=5000
```

### 4️⃣ Start MongoDB (Windows)

```bash
net start MongoDB
```

### 5️⃣ Start the Server

```bash
node server.js
```

Server runs at:

```
http://localhost:5000
```

---

## 🧪 API Testing

### ✔ Register User

**POST** `http://localhost:5000/auth/register`

#### Request Body:

```json
{
  "name": "Ali",
  "email": "ali@example.com",
  "password": "123456"
}
```

#### Successful Response:

```json
{
  "message": "User created",
  "user": "Ali"
}
```

---

### ✔ Login User

**POST** `http://localhost:5000/auth/login`

#### Request Body:

```json
{
  "email": "ali@example.com",
  "password": "123456"
}
```

#### Successful Response:

```json
{
  "message": "Login successful",
  "token": "YOUR_JWT_TOKEN"
}
```

---

## 🔐 Password Encryption

All passwords are automatically encrypted using:

```
bcrypt.hash(password, 10)
```

This ensures no plain-text passwords are stored in the database.

---

## 🎟 JWT Token

After successful login, the API returns a JWT token that expires in **1 hour**:

```js
jwt.sign({ id: user._id }, process.env.JWT_SECRET, { expiresIn: "1h" });
```

Use this token for authentication in future requests.

---

## 🛢 MongoDB Data Example

A user saved in MongoDB looks like this:

```json
{
  "_id": "675f21d31c9a",
  "name": "Ali",
  "email": "ali@example.com",
  "password": "$2b$10$E5Rvu1E1...",
  "__v": 0
}
```

✔ Password is encrypted
✔ Email is unique
✔ Data is clean and secure

---

## 📌 Scaling the System

This project supports future scaling:

### Horizontal Scaling:

- Add load balancers (NGINX / AWS ALB)
- Run multiple Node.js instances
- Use clustered MongoDB (Replica Set)

### Vertical Scaling:

- Increase server CPU/RAM

### Database Scaling:

- Sharding
- Replication
- Index optimization

---

## 🧭 Future Improvements

🚀 Add Refresh Tokens
🚀 Add Role-Based Access Control (RBAC)
🚀 Add Email Verification
🚀 Add Password Reset via Email
🚀 Add Rate Limiting
🚀 Add Unit Tests

---

## 👨‍💻 Author

**Ala AlDain Abdo**
Full-Stack Developer | Software Architecture & System Design
GitHub: [https://github.com/alaaldainabdo](https://github.com/alaaldainabdo)

---

## ⭐ Support

If you like this project, don’t forget to:

- ⭐ Star the repository
- 🔁 Fork it
- 🤝 Contribute

---

```

---

# 🎉 جاهز للنشر الآن
إذا تريد أحول لك الـ README إلى:

✅ ملف Word
✅ PDF
✅ أضيف صور توضيحية
✅ أضيف Diagram Architecture
فقط قل: **"أريد نسخة للـ Word"** أو **"أريد نسخة PDF"**.
```
