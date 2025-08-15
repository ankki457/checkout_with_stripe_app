# 🛍️ Mini E-Commerce Website – SDE Internship Assignment

This is a fully functional **mini e-commerce application** built as part of the **SDE Developer Intern assignment** for Nua.  
It is developed using **React.js** for the frontend and **Node.js + Express** for the backend.  
The app integrates **Stripe Checkout** for secure payments in INR and uses **MongoDB** to store order details.

---

## 📌 Features

### **1. Product Listing (`/`)**
- Responsive product grid layout (image, title, price).
- Search bar for filtering products by title.
- Category-based filtering using API endpoint.
- Loading indicators and error handling.

### **2. Product Detail (`/product/:id`)**
- Displays product image(s), title, description, price, and rating.
- Quantity selector (1–5).
- "Add to Cart" button to store product in global state.

### **3. Shopping Cart (`/cart`)**
- Lists added items with thumbnail, title, unit price, quantity, and subtotal.
- Quantity selector (1–10) and item removal option.
- Grand total calculation.
- "Proceed to Checkout" button.

### **4. Checkout (`/checkout`)**
- Order summary with total price.
- Simple checkout form with validation (name, email, address).
- Places order, processes payment via Stripe, clears cart, and shows confirmation.

### **5. Data Caching**
- Caches product lists/details in **localStorage** to prevent redundant API calls.

### **6. State Management**
- Global state managed using **React Context API**.

---

## 🛠️ Tech Stack

**Frontend**
- React.js
- Axios
- Context API
- React Router DOM

**Backend**
- Node.js
- Express.js
- MongoDB + Mongoose
- Stripe API (Test Mode)

---

## 📂 Folder Structure

checkout_with_stripe_app/ │ ├── client/                # Frontend React app │   ├── public/ │   ├── src/ │   │   ├── components/    # Reusable UI components │   │   ├── pages/         # Page components (Home, Product, Cart, Checkout) │   │   ├── context/       # Global state management │   │   ├── utils/         # Helper functions │   │   └── App.js │   ├── package.json │ ├── server/                # Backend Node.js app │   ├── models/            # Mongoose schemas │   ├── routes/            # API routes │   ├── controllers/       # Business logic │   ├── server.js          # App entry point │   ├── package.json │ └── README.md              # Documentation


## 🚀 Setup Instructions

### 1️⃣ Clone the repo
```bash
git clone https://github.com/ankki457/checkout_with_stripe_app.git
cd checkout_with_stripe_app

2️⃣ Setup environment variables

Create a .env file in the /server directory:

PORT=5000
MONGO_URI=your_mongodb_connection_string
STRIPE_SECRET=sk_test_...
CLIENT_URL=http://localhost:3000
STRIPE_WEBHOOK_SECRET=whsec_...

3️⃣ Install dependencies

Backend

cd server
npm install

Frontend

cd ../client
npm install

4️⃣ Run the project

Start Backend

cd server
npm start

Start Frontend

cd client
npm start

Visit: http://localhost:3000


---

📦 Webhook Setup (Optional for Local Testing)

If you want to test Stripe webhooks locally:

stripe login
stripe listen --forward-to localhost:5000/webhook

Copy the webhook secret and update .env.


---

🖼️ Screenshots
Here is ScreenShoot - 

![2025-05-19_16h36_21](https://github.com/user-attachments/assets/db1b8746-b695-4050-bcdb-fa22e73e45d1)
![2025-05-19_16h36_58](https://github.com/user-attachments/assets/82e3e48b-27fd-4ea6-abdf-f3e1eedbffb5)
![2025-05-19_16h37_19](https://github.com/user-attachments/assets/803f1708-dcd8-475a-9135-dd8d3e879967)
![2025-05-19_16h38_04](https://github.com/user-attachments/assets/93986764-f800-45c2-b2a5-16e8eca0f802)
![2025-05-19_16h41_39](https://github.com/user-attachments/assets/0fd65015-a180-461e-8dce-cd81f1d9cd27)
![2025-05-19_16h41_21](https://github.com/user-attachments/assets/019e1b51-85c8-4758-82f3-c9d3a19d6b94)
