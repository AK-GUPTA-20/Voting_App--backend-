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

1. Clone the repository:
   ```bash
   git clone https://github.com/AK-GUPTA-20/Voting_App-(backend).git
   cd Voting_App-(backend)
   
2.Install dependencies:

```bash
  npm install

3.Create a .env file in the root directory:

  PORT=3000
  MONGODB_URI=mongodb://localhost:27017/voting_app
  JWT_SECRET=yourSecretKey

4.Start the server:
```bash
  npm start



