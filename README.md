# 🍽️ Mozzo Bazar – Server Side

This is the **backend server** for Mozzo Bazar, a modern restaurant web application.  
It provides **RESTful APIs** for authentication, role management, orders, cart system, payments, and reviews.  

---

## 🚀 Features
- 🌐 **REST API** with Express.js  
- 🛢 **Database**: MongoDB (Mongoose ODM)  
- 🔐 **Authentication & Authorization**: Firebase JWT / Custom JWT  
- 👥 **Role Management**: Separate roles for **User** and **Admin**  
- 💳 **Payment Integration**: Stripe API for secure payments  
- 🛒 **Cart System**: Add, remove, and checkout items  
- 📝 **Reviews API** – Users can post & view reviews  
- 📊 **Admin Controls** – Manage users, menu items, and orders  

---

## 🛠️ Tech Stack
- **Backend Framework:** Express.js  
- **Database:** MongoDB with Mongoose  
- **Authentication:** Firebase / JWT  
- **Payment:** Stripe  
- **Environment:** Node.js  

---

## 📂 Project Structure
```
mozzo-bazar-server/
├── src/
│   ├── app/
│   │   ├── models/        # Mongoose schemas
│   │   ├── routes/        # Express routes
│   │   ├── controllers/   # Business logic
│   │   └── services/      # Database queries
│   ├── config/            # DB & JWT config
│   ├── index.js           # Server entry point
│   └── utils/             # Helper functions
├── .env.example           # Example environment variables
├── package.json           # Dependencies
└── README.md              # Documentation
```

---

## ⚡ Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/Alok4D/bistro-boss-server
   cd mozzo-bazar-server
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment Variables**
   Create a `.env` file in the root directory:
   ```env
   PORT=5000
   DATABASE_URL=mongodb+srv://<username>:<password>@cluster0.mongodb.net/mozzoBazar
   JWT_SECRET=yourSecretKey
   STRIPE_SECRET_KEY=yourStripeSecret
   ```

4. **Run the server**
   ```bash
   npm run dev
   ```
   The server will start on `http://localhost:5000`

---

## 📡 API Endpoints

### 🔑 Auth
- `POST /auth/signup` – Register user  
- `POST /auth/login` – Login & get JWT  
- `GET /auth/profile` – Get logged-in user info  

### 🛒 Cart
- `GET /cart?email=user@example.com` – Get user cart  
- `POST /cart` – Add to cart  
- `DELETE /cart/:id` – Remove item  

### 🍴 Menu
- `GET /menu` – Get all menu items  
- `POST /menu` (Admin) – Add new item  
- `PATCH /menu/:id` (Admin) – Update item  
- `DELETE /menu/:id` (Admin) – Delete item  

### 💳 Payment
- `POST /create-payment-intent` – Stripe payment intent  
- `POST /payments` – Save payment info  

### 📝 Reviews
- `GET /reviews` – Get all reviews  
- `GET /reviews?email=user@example.com` – Get user-specific reviews  
- `POST /reviews` – Add a review  

### 👥 Users (Admin Only)
- `GET /users` – Get all users  
- `PATCH /users/:id` – Update role (Admin/User)  
- `DELETE /users/:id` – Remove user  

---

## 👥 Role Management
- **User**: Can browse menu, manage cart, make payments, post reviews  
- **Admin**: Full control – manage items, users, and track orders  

👉 Demo Credentials same as **frontend**  
- User: `mozzouser@gmail.com` / `@MozzoUser1`  
- Admin: `mozzoadmin@gmail.com` / `@MozzoAdmin1`  

---

## 🌍 Deployment
- **Backend Hosting:** Render / Railway / Vercel Serverless  
- **Database:** MongoDB Atlas  
- **Payment:** Stripe  

---

## 👨‍💻 Author
- **Alok**  
  📧 alokroy602701@gmail.com  
  🔗 [Portfolio](https://alok-roy-portfolio.vercel.app/)  
  🐙 [GitHub](https://github.com/Alok4D)  
```

