# CoreControl - MERN Admin Dashboard

> A production-ready internal administration console built with the MERN stack for managing customers, inventory, and sales orders through a modern dashboard.

---

## 📌 Overview

CoreControl is a full-stack MERN application designed to simplify internal business operations from a single interface.

The platform enables administrators to:

- Manage customer information
- Maintain product inventory
- Create and track sales orders
- Monitor business statistics in real time

The application follows a decoupled client-server architecture where the React frontend communicates with an Express REST API backed by MongoDB Atlas.

---

# 🚀 Features

### Customer Management

- Create customer accounts
- View customer details
- Update customer information
- Delete customer records
- Search customers instantly

---

### Product Management

- Add new inventory items
- Edit existing products
- Delete products
- Stock management
- Category support
- Availability tracking

---

### Order Management

- Create customer orders
- Link customers with products
- Automatic total price calculation
- Track order status
- View complete order history

---

### Dashboard

- Total Customers
- Total Products
- Total Orders
- Responsive analytics cards

---

### Additional Features

- Responsive UI
- Confirmation dialogs before deletion
- Search functionality
- RESTful API
- Modular architecture
- Reusable React components

---

# 🛠 Tech Stack

## Frontend

- React.js
- Vite
- Tailwind CSS
- Axios
- React Router

---

## Backend

- Node.js
- Express.js
- MongoDB
- Mongoose
- dotenv
- CORS

---

## Database

- MongoDB Atlas

---

## Version Control

- Git
- GitHub

---

# 🏗 Architecture

```
React Client
      │
      │ HTTP Requests (JSON)
      ▼
Express REST API
      │
      ▼
Controllers
      │
      ▼
Mongoose Models
      │
      ▼
MongoDB Atlas
```

---

# 📂 Project Structure

```
Root/
│
├── backend/
│   ├── src/
│   │   ├── config/
│   │   ├── controllers/
│   │   ├── models/
│   │   ├── routes/
│   │   └── middleware/
│   │
│   ├── server.js
│   ├── package.json
│   └── .env
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── services/
│   │   ├── hooks/
│   │   └── assets/
│   │
│   ├── vite.config.js
│   ├── package.json
│   └── .env
│
└── README.md
```

---

# 🗄 Database Schema

## Customer

```javascript
{
  name: String,
  email: String,
  age: Number
}
```

---

## Product

```javascript
{
  name: String,
  description: String,
  price: Number,
  category: String,
  stock: Number,
  available: Boolean
}
```

---

## Order

```javascript
{
  customer: ObjectId,
  products: [
    {
      product: ObjectId,
      quantity: Number
    }
  ],
  totalPrice: Number,
  status: String
}
```

---

# 🔄 Data Relationships

```
Customer
    │
    │ 1:N
    ▼
Orders
    │
    │ N:M
    ▼
Products
```

---

# ⚙ Installation

## Clone Repository

```bash
git clone https://github.com/srikar2908/mernexus-admin-dashboard.git
```

---

# Backend Setup

```bash
cd backend
```

Install dependencies

```bash
npm install
```

Create a `.env`

```env
PORT=3000

MONGODB_URL=your_mongodb_connection_string
```

Run the server

```bash
npm run dev
```

---

# Frontend Setup

```bash
cd frontend
```

Install packages

```bash
npm install
```

Create `.env`

```env
VITE_API_BASE_URL=http://localhost:3000
```

Start the client

```bash
npm run dev
```

---

# 📡 REST API

## Customers

| Method | Endpoint | Description |
|---------|----------|-------------|
| POST | /users | Create customer |
| GET | /users | Get all customers |
| GET | /users/:id | Get customer |
| PUT | /users/:id | Update customer |
| DELETE | /users/:id | Delete customer |

---

## Products

| Method | Endpoint | Description |
|---------|----------|-------------|
| POST | /products | Create product |
| GET | /products | Get all products |
| GET | /products/:id | Get product |
| PUT | /products/:id | Update product |
| DELETE | /products/:id | Delete product |

---

## Orders

| Method | Endpoint | Description |
|---------|----------|-------------|
| POST | /orders | Create order |
| GET | /orders | Get all orders |
| GET | /orders/:id | Get order |
| PUT | /orders/:id | Update order |
| DELETE | /orders/:id | Delete order |

---

# 🎯 Future Improvements

- JWT Authentication
- Role-Based Access Control (RBAC)
- Image Upload Support
- Pagination
- Advanced Filtering
- Search Optimization
- Order Analytics
- Dashboard Charts
- Inventory Alerts
- Unit Testing
- Integration Testing
- GitHub Actions CI/CD
- Docker Support
- Deployment on Render/Vercel

---

# 📸 Screenshots

> Add screenshots of your dashboard here.

```
Dashboard

Customers

Products

Orders
```

---

# 🤝 Contributing

Contributions are welcome.

1. Fork the repository

2. Create a feature branch

```bash
git checkout -b feature-name
```

3. Commit your changes

```bash
git commit -m "Added feature"
```

4. Push to GitHub

```bash
git push origin feature-name
```

5. Open a Pull Request

---

# 📜 License

This project is open-source and available under the MIT License.

---

# 👨‍💻 Author

**Naresh Gorinta**

- GitHub: https://github.com/nareshgorinta
- LinkedIn: *(Add your LinkedIn profile)*

---

## ⭐ If you like this project

Give the repository a **Star ⭐** on GitHub to support the project.
