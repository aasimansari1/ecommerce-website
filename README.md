# ShopHub - Ecommerce Website

A full-stack ecommerce web application built with React, Express, and MongoDB.

## Features

- **Product Catalog** - Browse 12+ products with search, category filtering, and sorting
- **Product Details** - View product info, ratings, stock status, and add to cart
- **Shopping Cart** - Add/remove items, adjust quantities, view totals
- **Checkout** - Shipping address form with order summary
- **User Authentication** - Register and login with JWT-based auth
- **User Dashboard** - View order history and order status
- **Admin Panel** - Manage products (add/edit/delete), orders (mark delivered), and users

## Tech Stack

| Layer      | Technology                        |
|------------|-----------------------------------|
| Frontend   | React 18, React Router v6, Axios |
| Backend    | Express.js, Node.js              |
| Database   | MongoDB, Mongoose                |
| Auth       | JWT (JSON Web Tokens), bcryptjs  |

## Project Structure

```
ecommerce/
├── client/                 # React frontend
│   └── src/
│       ├── api/            # Axios instance
│       ├── components/     # Navbar, Footer, ProductCard
│       ├── context/        # AuthContext, CartContext
│       └── pages/          # Home, Products, Cart, Checkout, Login, Register, Dashboard, Admin
├── server/                 # Express backend
│   ├── config/             # Database connection
│   ├── middleware/         # Auth middleware
│   ├── models/            # User, Product, Order schemas
│   ├── routes/            # API routes (auth, products, orders, users)
│   ├── seed.js            # Database seeder
│   └── server.js          # Entry point
└── package.json
```

## Getting Started

### Prerequisites

- Node.js (v18+)
- MongoDB

### Installation

1. Clone the repository
   ```bash
   git clone https://github.com/aasimansari1/ecommerce-website.git
   cd ecommerce-website
   ```

2. Install dependencies
   ```bash
   npm install
   ```

3. Seed the database
   ```bash
   npm run seed
   ```

4. Start the development servers
   ```bash
   npm run dev
   ```

5. Open http://localhost:3000 in your browser

### Available Scripts

| Command           | Description                              |
|-------------------|------------------------------------------|
| `npm run dev`     | Start both frontend and backend servers  |
| `npm run server`  | Start backend only (port 5000)           |
| `npm run client`  | Start frontend only (port 3000)          |
| `npm run seed`    | Seed database with sample products       |

## API Endpoints

| Method | Endpoint             | Description          |
|--------|----------------------|----------------------|
| POST   | `/api/auth/register` | Register a new user  |
| POST   | `/api/auth/login`    | Login user           |
| GET    | `/api/products`      | Get all products     |
| GET    | `/api/products/:id`  | Get single product   |
| POST   | `/api/orders`        | Create an order      |
| GET    | `/api/orders`        | Get user orders      |
| GET    | `/api/users`         | Get all users (admin)|
