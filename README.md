# 🛍️ Online Handicraft Store

## 📌 Project Overview

**Online Handicraft Store** is a role-based e-commerce platform developed to connect handicraft sellers and customers on a single marketplace. The platform supports four different user roles:

* **Super Admin**
* **Admin**
* **Seller**
* **User**

The system allows users to browse handicraft products, add products to the cart, and place orders using either online payment or Cash on Delivery (COD). Sellers can create shops and upload products after receiving approval from Admin or Super Admin. Admins and Super Admin manage sellers, shops, products, and overall platform activities.

---

# 🚀 Features

## 👤 User Features

* User Registration and Login
* Browse Handicraft Products
* Search and View Product Details
* Add Products to Cart
* Place Orders
* Online Payment Support
* Upload Payment Screenshot for Verification
* Cash on Delivery (COD) Option
* View Order History and Status

---

## 🏪 Seller Features

* Seller Registration
* Seller Account Approval by Admin/Super Admin
* Create and Manage Shops
* Shop Approval Workflow
* Add/Edit/Delete Products
* Upload Product Images
* Manage Product Pricing and Details
* Add Payment URL
* Automatic QR Code Generation from Payment URL
* View Customer Orders
* Verify Online Payments
* Confirm Orders

---

## 🛠️ Admin Features

* Admin Login
* Manage Sellers
* Approve or Reject Seller Accounts
* Approve or Reject Seller Shops
* Monitor Seller Activities
* Manage Platform Operations

---

## 👑 Super Admin Features

* Full System Control
* Create and Manage Admin Accounts
* Manage Sellers
* Approve Admin Accounts
* Approve Seller Accounts and Shops
* Monitor Entire Platform Activities

---

# 🏗️ System Architecture

The application follows a **Three-Layer Architecture**.

## Frontend Layer

* Developed using **ReactJS**
* Responsive and user-friendly interface
* Role-based dashboard implementation

## Backend Layer

* Developed using **Spring Boot** and **Java**
* RESTful API development
* Authentication and authorization
* Business logic implementation

## Database Layer

* MySQL Database
* Stores user, seller, shop, product, order, and payment information

### Architecture Flow

```text
User
  ↓
React Frontend
  ↓
Spring Boot REST APIs
  ↓
MySQL Database
```

---

# 💻 Tech Stack

## Frontend

* ReactJS
* HTML5
* CSS3
* JavaScript

## Backend

* Java
* Spring Boot
* Spring Security
* JWT Authentication

## Database

* MySQL

## Tools

* GitHub
* VS Code
* Postman
* Maven

---

# 🔄 Application Workflow

## User Order Flow

1. User registers and logs in.
2. User browses products uploaded by approved sellers.
3. User adds products to cart.
4. User places an order.
5. User selects payment method:

   * Online Payment
   * Cash on Delivery (COD)

### Online Payment

1. User scans QR Code or uses payment link.
2. User completes payment.
3. User uploads payment screenshot.
4. Seller verifies payment.
5. Seller confirms order.

### Cash on Delivery

1. User selects COD.
2. Order is placed directly.
3. Seller processes and confirms the order.

---

    ↓
Database Validation
    ↓
JWT Token Generation
    ↓
Response to Frontend


---

# 🗄️ Database Schema

## Users Table

| Field    | Description        |
| -------- | ------------------ |
| user_id  | Primary Key        |
| name     | User Name          |
| email    | Email Address      |
| password | Encrypted Password |
| role     | User Role          |

---

## Seller Table

| Field           | Description               |
| --------------- | ------------------------- |
| seller_id       | Primary Key               |
| user_id         | Foreign Key               |
| approval_status | Pending/Approved/Rejected |

---

## Shop Table

| Field           | Description               |
| --------------- | ------------------------- |
| shop_id         | Primary Key               |
| seller_id       | Foreign Key               |
| shop_name       | Shop Name                 |
| approval_status | Pending/Approved/Rejected |

---

## Product Table

| Field        | Description         |
| ------------ | ------------------- |
| product_id   | Primary Key         |
| shop_id      | Foreign Key         |
| product_name | Product Name        |
| price        | Product Price       |
| image        | Product Image       |
| description  | Product Description |
| payment_url  | UPI/Payment Link    |

---

## Cart Table

| Field      | Description      |
| ---------- | ---------------- |
| cart_id    | Primary Key      |
| user_id    | Foreign Key      |
| product_id | Foreign Key      |
| quantity   | Product Quantity |

---

## Orders Table

| Field          | Description                 |
| -------------- | --------------------------- |
| order_id       | Primary Key                 |
| user_id        | Foreign Key                 |
| payment_method | Online/COD                  |
| order_status   | Pending/Confirmed/Delivered |

---

## Payment Table

| Field          | Description        |
| -------------- | ------------------ |
| payment_id     | Primary Key        |
| order_id       | Foreign Key        |
| screenshot     | Payment Screenshot |
| payment_status | Pending/Verified   |

---

# 📱 QR Code Generation

The seller provides a payment URL while adding a product.

The system automatically:

1. Reads the payment URL.
2. Generates a QR Code.
3. Displays the QR Code to the customer during checkout.
4. Customer scans the QR Code and completes payment.

---


# 🔮 Future Enhancements

* Payment Gateway Integration (Razorpay/Stripe)
* Automatic Payment Verification
* Cash on Delivery Additional Charges
* Real-Time Order Tracking
* AI-Based Product Recommendation System
* Email Notifications
* SMS Notifications
* Product Reviews and Ratings
* Multi-Language Support
* Sales Analytics Dashboard
* Inventory Management
* Seller Performance Reports

---

# 👨‍💻 Developed By

**Pranavi Baad**
**Github:https://github.com/PranaviBaad04/Online_Handicraft_Store**



# 📄 License

This project is developed for educational and learning purposes.
