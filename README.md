# 🏦 Bank Transaction System

A backend banking application built with **Node.js**, **Express.js**, and **MongoDB** that simulates core banking operations such as user authentication, account management, and secure fund transfers.

The project follows a modular REST API architecture and uses a **ledger-based accounting system** to record every debit and credit entry, providing a reliable audit trail for all transactions.

---

## ✨ Features

- 👤 User registration and login
- 🔐 JWT-based authentication
- 🔑 Secure password hashing with bcrypt
- 🏦 Bank account creation and management
- 💰 Check account balance
- 🔄 Secure fund transfers between accounts
- 📒 Ledger-based transaction recording
- 🛡️ Idempotent transactions to prevent duplicate transfers
- 📧 Email notifications for successful transactions
- 🧩 Modular MVC architecture

---

## 🛠️ Tech Stack

- **Backend:** Node.js, Express.js
- **Database:** MongoDB
- **ODM:** Mongoose
- **Authentication:** JWT (JSON Web Token)
- **Password Hashing:** bcrypt
- **Email Service:** Nodemailer

---

## 📁 Project Structure

```text
Bank-Transaction-System/
│
├── src/
│   ├── config/
│   ├── controllers/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── services/
│   └── app.js
│
├── server.js
├── package.json
├── package-lock.json
└── .env
```

---

## 🚀 Installation

### Install dependencies

```bash
npm install
```

### Configure environment variables

Create a `.env` file in the root directory.

```env
MONGO_URI=your_mongodb_connection_string
JWT_SECRET_KEY=your_jwt_secret
CLIENT_ID
CLIENT_SECRET
EMAIL_USER=your_email
REFRESH_TOKEN
```

### Run the server

Development mode:

```bash
npm run dev
```

Production mode:

```bash
npm start
```

---

## 📒 Ledger-Based Accounting

Instead of storing a separate transaction history, every transfer is recorded as **ledger entries**.

Each transaction creates:

- ➖ A debit entry for the sender
- ➕ A credit entry for the receiver

This approach provides:

- Immutable records
- Complete audit trail
- Accurate balance calculation
- Clear debit/credit tracking

---

## 🛡️ Security Features

- JWT authentication
- Password hashing with bcrypt
- Protected API routes
- Input validation
- Idempotency keys for safe retries

---

## 📌 Example Transaction Request

```http
POST /api/transaction
Content-Type: application/json
Authorization: Bearer <token>

{
  "fromAccount": "64f1...",
  "toAccount": "64f2...",
  "amount": 500,
  "idempotencyKey": "txn-12345"
}
```

---

## 🔮 Future Improvements

- 👥 Role-based access control
- 📄 Pagination for ledger entries
- 📊 Transaction filtering
- 🚦 Rate limiting
- 🧪 Unit and integration tests
- 🐳 Docker support
- 📚 Swagger API documentation
- ⚙️ CI/CD pipeline

---

## 

**Vijay Khetwal**

🔗 GitHub: https://github.com/VijaySingh092
