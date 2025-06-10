# 🗳️ Voting_App-(backend)

A secure backend API for an online voting system built with Node.js, Express, and MongoDB. This project allows citizens to vote once using their Aadhar Card Number and lets an admin manage candidates securely.

---

## 🔗 GitHub Repository

**URL:** [https://github.com/AK-GUPTA-20/Voting_App-(backend)](https://github.com/AK-GUPTA-20/Voting_App-(backend))

---

## ✨ Features

- ✅ User sign-up & login using **Aadhar Card Number** (12-digit)
- 🔐 Passwords hashed with **bcrypt**
- 🔒 Authentication with **JWT**
- 👤 Users can:
  - View all candidates
  - Vote once
  - Update their password
- 👮 Admin can:
  - Add, update, delete candidates
  - View all candidates
  - **Cannot vote**
- 📊 Live vote count for each party

---

## ⚙️ Tech Stack

- Node.js
- Express.js
- MongoDB (Mongoose)
- JWT (Authentication)
- bcrypt (Password encryption)
- dotenv (Environment management)

---

## 🚀 Getting Started

### 🔧 Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/AK-GUPTA-20/Voting_App-(backend).git
   cd Voting_App-(backend)
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Create a `.env` file** in the root directory:
   ```env
   PORT=3000
   MONGODB_URI=mongodb://localhost:27017/voting_app
   JWT_SECRET=yourSecretKey
   ```

4. **Start the server:**
   ```bash
   npm start
   ```

---

## 📬 API Endpoints

### 🔐 Authentication

#### `POST /user/signup`
Register a user (or admin)
```json
{
  "name": "John Doe",
  "aadharCardNumber": "123456789012",
  "password": "securePassword",
  "role": "user" // or "admin"
}
```

#### `POST /user/login`
Login user with Aadhar and password
```json
{
  "aadharCardNumber": "123456789012",
  "password": "securePassword"
}
```

---

### 👤 User Profile

#### `GET /user/profile`
Fetch user profile *(JWT required)*

#### `PUT /user/profile/password`
Update user password *(JWT required)*
```json
{
  "currentPassword": "oldPassword",
  "newPassword": "newSecurePassword"
}
```

---

### 🧑‍💼 Candidate Management (Admin Only)

#### `POST /candidate/`
Add a new candidate
```json
{
  "name": "Candidate Name",
  "party": "Party Name"
}
```

#### `PUT /candidate/:candidateID`
Update candidate details

#### `DELETE /candidate/:candidateID`
Delete a candidate

#### `GET /candidate/`
Get all candidates (names and parties)

---

### 🗳️ Voting System

#### `GET /candidate/vote/:candidateID`
Vote for a candidate *(User only)*  
- One-time vote per user  
- Admins cannot vote

#### `GET /candidate/vote/count`
Get vote counts for each party
```json
[
  { "party": "Alpha", "count": 12 },
  { "party": "Beta", "count": 8 }
]
```

---

## 🔐 Token-Based Authentication

Use the JWT token received on login/signup in the request headers:

```
Authorization: Bearer <your_token>
```

---

## 🗂️ Folder Structure

```
Voting_App-(backend)/
│
├── models/
│   ├── user.js
│   └── candidate.js
│
├── routes/
│   ├── userRoutes.js
│   └── candidateRoutes.js
│
├── jwt.js
├── app.js
├── db.js
├── .env
└── package.json
```

---

## ✅ Requirements

- Node.js ≥ v14
- MongoDB running locally or via Atlas
- Aadhar must be unique and 12 digits
- Only one admin allowed in the system

---

## 📌 Future Improvements (Optional)

- OTP/email verification
- Admin dashboard UI
- Voter ID/Aadhar verification via API

---

## 🧑‍💻 Author

**Akshat Gupta**  
GitHub: [@AK-GUPTA-20](https://github.com/AK-GUPTA-20)

---

## 📝 License


