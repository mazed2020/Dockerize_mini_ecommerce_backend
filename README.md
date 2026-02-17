# 🛒 Mini E-Commerce Backend API

A scalable and secure RESTful backend API for a Mini E-Commerce platform  
built using **Node.js**, **Express.js**, and **MongoDB**.

---

## 🚀 Features

### 🔐 Authentication & Authorization
- User Registration
- User Login
- Role-Based Access Control:
  - Admin
  - Customer
- Fraud prevention mechanisms (e.g., preventing repeated order cancellations causing stock misuse)

---

### 📦 Product Management (Admin Only)
- Add new products
- Update product details
- Delete products
- Manage and update product stock

---

### 🛒 Customer Features
- Add product to cart
- Remove product from cart
- Place order

---

## 🏗 Tech Stack

- Node.js
- Express.js
- MongoDB + Mongoose
- JWT
- bcrypt
- Cloudinary
- dotenv
- Nodemon
- multer
- Zod
- Docker

---

## 📂 Project Structure

```
├── node_modules/
├── public/
│   ├── dummydataset/
│   └── temp/ER-Diagram/
├── src/
│   ├── controllers/
│   ├── db/
│   ├── middleware/
│   ├── models/
│   ├── routes/
│   ├── utils/
│   ├── validators/
│   ├── app.js
│   ├── constants.js
│   └── index.js
```

---

# 🐳 Docker Setup (Live Deployment)

## 1️⃣ Clone Dockerized Repository

```bash
git clone https://github.com/mazed2020/Dockerize_mini_ecommerce_backend.git
cd Dockerize_mini_ecommerce_backend
```

## 2️⃣ Create `.env` File

Create a `.env` file in the root directory:

```
MONGODB_URI=mongodb://admin:password123@mongo:27017/Mini-Ecommerce?authSource=admin
PORT=5000
CORS_ORIGIN=*

SECRETE_KEY=your_jwt_secret
EXPIERY_KEY=10d
REFRESH_TOKEN_SECRE=your_refresh_secret
REFRESH_EXPIERE=1d

CLOUD_NAME=your_cloud_name
API_KEY=your_cloudinary_key
API_SECRET=your_cloudinary_secret
```

## 3️⃣ Build & Run Containers

```bash
docker compose up -d --build
```

---

## 🌐 Access API

### 🔹 Local Development
```
http://localhost:5001/api/v1/
```

### 🔹 VPS Deployment
```
http://72.61.116.162:5001/api/v1
```

 

---

## 🗄 MongoDB UI (mongo-express)

If enabled:

```
http://72.61.116.162:8082/
```

Default credentials:
```
Username: admin
Password: pass
```

---

# ⚙ Local Installation (Without Docker)

## 1️⃣ Clone the Repository

```bash
git clone https://github.com/mazed2020/Mini-Ecommerce-Backend.git
cd Mini-Ecommerce-Backend
```

## 2️⃣ Install Dependencies

```bash
npm install
```

## 3️⃣ Create `.env` File

```
MONGODB_URI=mongodb://127.0.0.1:27017
PORT=5000
CORS_ORIGIN=*
EXPIERY_KEY=10d
REFRESH_TOKEN_SECRE=dfbdjbfajbsid
REFRESH_EXPIERE=1d
SECRETE_KEY=jKPCFPlJN9IVW9uA7KVcLIedkmM
CLOUD_NAME=dr3lsbx2k
API_KEY=185859713928424
API_SECRET=your_cloudinary_secret
```

## 4️⃣ Run Development Server

```bash
npm run dev
```

---

# 📌 API Endpoints

## 🔐 Authentication

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/v1/auth/register` | Register new user |
| POST | `/api/v1/auth/login` | Login user |

---

## 📦 Products

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/v1/products/getAllProducts` | Get all products (Public) |
| GET | `/api/v1/products/getProductById/:id` | Get product by ID |
| POST | `/api/v1/products/createProduct` | Create product (Admin) |
| PUT | `/api/v1/products/updateProductById/:id` | Update product |
| DELETE | `/api/v1/products/deleteProductById/:id` | Delete product |

---

## 🛒 Cart

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/v1/carts/getAllCardItems` | Get all cart items |
| POST | `/api/v1/carts/addToCardItems` | Add item to cart |
| DELETE | `/api/v1/carts/deleteItemsByProductId/:productId` | Remove item |
| DELETE | `/api/v1/carts/clearCart` | Clear cart |

---

## 📑 Orders

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/v1/orders/checkoutOrder` | Checkout order |
| GET | `/api/v1/orders/getMyOrder` | Get user's orders |
| GET | `/api/v1/orders/getOrderById/:id` | Get order by ID |
| PATCH | `/api/v1/orders/:id/cancelOder` | Cancel order |

---

# 🔑 Authentication

Protected routes require:

```
Authorization: Bearer <access_token>
```

---

# 🧪 API Testing & Documentation

🔗 **Live API Docs (Postman):**  
👉 https://documenter.getpostman.com/view/34409474/2sBXcBm26C

 

---

# 👨‍💻 Author

**Mazed**

Local Version:  
https://github.com/mazed2020/Mini-Ecommerce-Backend

Dockerized Live Version:  
https://github.com/mazed2020/Dockerize_mini_ecommerce_backend

---

# 📄 License

This project is licensed under the MIT License.
