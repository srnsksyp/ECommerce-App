# 🛒 Full-Stack E-Commerce Platform

A modern full-stack e-commerce web application built with **React**, **Node.js**, **Express**, **MongoDB**, and seamless payment integration via **Stripe (USD)** and **Razorpay (INR)**. Designed for scalability, polished UX, and real-world use cases.

---

## 🚀 Features

### 🔧 Backend (Express + MongoDB)
- Secure **JWT Authentication** for users & admins
- Complete **Order Management** (place, list, update status)
- Multi-gateway **Payment Integration**:
  - 💳 Stripe (USD — global)
  - 🪙 Razorpay (INR — domestic)
- Dynamic **Cart Logic** with atomic updates
- Address collection & normalized delivery flow
- Admin-side: order listing & status updates
- Razorpay verification via receipt/orderId
- Stripe success/failure routing with backend sync

### 🎨 Frontend (React + Tailwind CSS)
- Clean & responsive layout optimized for mobile and desktop
- Dynamic cart sidebar with live quantity control
- Form-validated checkout with real-time delivery details
- Payment method selection and conditional routing
- Order history display with UI polish
- Toast-based feedback and error handling

### 🎨 Admin (React + Tailwind CSS)
- Clean, responsive layout for seamless desktop and mobile admin experience
- Secure login with environment-based credential validation and JWT protection
- Role-based route gating to restrict access to admin-only functionality
- Product creation form with image preview, field validation, and toast notifications
- Product list view with edit/delete controls, pagination, and polished UI states
- Order tracking dashboard with status filters and real-time updates
- User management with access control, search, and sorting
- Integration-ready structure for analytics, CMS, or inventory insights
- Robust error handling with informative feedback for each admin action

---

## ⚙️ Tech Stack

| Layer       | Tools/Frameworks                        |
|-------------|-----------------------------------------|
| Frontend    | React (Hooks + Context), Vite, Tailwind |
| Backend     | Express, Node.js, JWT                   |
| Database    | MongoDB with Mongoose                   |
| Payments    | Stripe (Checkout Sessions), Razorpay    |
| Styling     | Tailwind CSS                            |
| Utilities   | Axios, React Toastify, dotenv           |

---

## 📦 Installation & Setup

### 1. Clone the repo
```bash
git clone https://github.com/srnsksyp/ECommerce-App.git
cd ecommerce-app
```

### 2. Setup Backend
```bash
cd backend
npm install
```

Create a `.env` file inside your backend folder with the following structure:

```env
PORT=4000
MONGODB_URI=your-mongodb-uri
JWT_SECRET=your-jwt-secret

CLOUDINARY_API_KEY=your-cloudinary-key
CLOUDINARY_SECRET_KEY=your-cloudinary-secret
CLOUDINARY_NAME=your-cloudinary-name

STRIPE_SECRET_KEY=your-stripe-secret-key
RAZORPAY_KEY_ID=your-razorpay-key-id
RAZORPAY_KEY_SECRET=your-razorpay-key-secret

ADMIN_EMAIL=your-admin-email
ADMIN_PASSWORD=your-admin-password
```

start server: 
```bash
npm run server
```

### 3. Setup Frontend
```bash
cd frontend
npm install
```

Create a `.env` file inside your frontend folder with the following structure:

```env
VITE_BACKEND_URL = your-backend-url
VITE_RAZORPAY_KEY_ID = your-razorpay-key-id
```

start server: 
```bash
npm run dev
```

### 4. Setup Admin
```bash
cd admin
npm install
```

Create a `.env` file inside your frontend folder with the following structure:

```env
VITE_BACKEND_URL = your-backend-url
```

start server: 
```bash
npm run dev
```

---

## ✅ Final Notes & Recommendations

### 👨‍💼 Seed Admin User (Optional)
To enable protected admin routes and dashboard access from the start, invoke the `seedAdmin()` utility during server initialization. This creates a default admin account using credentials from your `.env`.

### 🔐 Environment Management
- Create an `.env.example` file for team guidance and onboarding.
- Avoid committing sensitive data by excluding `.env` from version control:
  ```bash
  echo ".env" >> .gitignore

### 🚀 Deployment Tips
- Prepare separate .env.production and .env.development files.
- Use platforms like Render, Vercel, or Railway for hosting.
- Define environment variables through their dashboards.
📈 Future Enhancements
- 🧮 Dashboard analytics for revenue/orders
- 📦 Inventory tracking with stock alerts
- 🗂️ Modular access roles: moderators, vendors
- 🔍 Search, filtering, and sorting for admin table
