# 🍔 Self Food Order System

A full-stack web application that enables users to browse food items, add them to a cart, and place orders seamlessly. The system is designed with scalability, performance, and real-time interaction in mind.

---

## 🚀 Features

- 🧾 Browse food menu with categories
- 🛒 Add to cart & manage items
- 💳 Place orders with dynamic total calculation
- ⚡ Real-time updates (if Socket.io integrated)
- 🔐 User authentication (if implemented)
- 📦 Order tracking & management
- 📊 Scalable backend architecture

---

## 🛠️ Tech Stack

### Backend:
- Node.js
- Express.js
- MySQL / MongoDB (based on your implementation)
- Socket.io (for real-time features)
- Redis (for caching / session management)

### Frontend:
- HTML / CSS / JavaScript
*(or React.js if used)*

---

## 📁 Project Structure

```
self-food-order-system/
├── backend/
│   ├── controllers/
│   │   ├── authController.js
│   │   ├── orderController.js
│   │   └── menuController.js
│   ├── models/
│   │   ├── User.js
│   │   ├── Order.js
│   │   └── MenuItem.js
│   ├── routes/
│   │   ├── auth.js
│   │   ├── orders.js
│   │   └── menu.js
│   ├── middleware/
│   │   ├── authMiddleware.js
│   │   └── errorHandler.js
│   ├── config/
│   │   ├── db.js
│   │   └── redis.js
│   ├── socket/
│   │   └── socketHandler.js
│   ├── .env
│   ├── server.js
│   └── package.json
├── frontend/
│   ├── assets/
│   │   ├── images/
│   │   └── icons/
│   ├── css/
│   │   └── style.css
│   ├── js/
│   │   ├── cart.js
│   │   ├── menu.js
│   │   └── order.js
│   └── index.html
├── .gitignore
├── docker-compose.yml
└── README.md
```

---

## ⚙️ Getting Started

### Prerequisites

Make sure you have the following installed:

- [Node.js](https://nodejs.org/) (v16 or above)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)
- MySQL or MongoDB
- Redis (optional, for caching)

### Installation

1. **Clone the repository**

```bash
git clone https://github.com/your-username/self-food-order-system.git
cd self-food-order-system
```

2. **Install backend dependencies**

```bash
cd backend
npm install
```

3. **Configure environment variables**

Create a `.env` file in the `backend/` directory:

```env
PORT=5000
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=yourpassword
DB_NAME=food_order_db
REDIS_URL=redis://localhost:6379
JWT_SECRET=your_jwt_secret
```

4. **Start the backend server**

```bash
npm start
```

5. **Open the frontend**

Open `frontend/index.html` in your browser, or serve it using a static server.

---

## 📡 API Endpoints

| Method | Endpoint             | Description              |
|--------|----------------------|--------------------------|
| GET    | `/api/menu`          | Fetch all menu items     |
| GET    | `/api/menu/:category`| Fetch items by category  |
| POST   | `/api/orders`        | Place a new order        |
| GET    | `/api/orders/:id`    | Get order details        |
| POST   | `/api/auth/register` | Register a new user      |
| POST   | `/api/auth/login`    | Login and get JWT token  |

---

## 🔄 Real-Time Features (Socket.io)

The system uses Socket.io to push live updates:

- 🟢 Order status changes (e.g., Preparing → Ready → Delivered)
- 🔔 New order notifications for kitchen/admin
- 📊 Live cart sync across tabs (if enabled)

---


## 🐳 Docker Support

Run the full stack using Docker Compose:

```bash
docker-compose up --build
```

The `docker-compose.yml` should include services for the Node.js app, MySQL/MongoDB, and Redis.

---

## 🧪 Testing

```bash
# Run unit tests
npm test

# Run with coverage
npm run test:coverage
```

---



## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 👨‍💻 Author

**Your Name**
- GitHub: [@your-username](https://github.com/girraj12)
---

> ⭐ If you found this project helpful, please give it a star!
