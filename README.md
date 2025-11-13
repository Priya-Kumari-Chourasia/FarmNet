# 🧑‍🌾 FarmNet – Blockchain-Based Agricultural Marketplace

FarmNet is a blockchain-powered decentralized marketplace that directly connects farmers and consumers, ensuring transparency, traceability, and fair trade.
Built with Next.js, Node.js, Express.js, MongoDB, and Hardhat (Local Ethereum Network), it uses smart contracts to secure and verify transactions.

## 🚀 Features

- ✅ Direct farmer–consumer trade
- ✅ Transparent blockchain-based transactions
- ✅ Smart contract–powered product verification
- ✅ Secure user authentication (bcrypt.js)
- ✅ Load-balanced backend servers for performance
- ✅ Cart and order management
- ✅ Dashboard analytics for farmers

## 🧱 Tech Stack
| Layer                       | Technologies                                       |
| --------------------------- | -------------------------------------------------- |
| **Frontend (Presentation)** | Next.js, React, TailwindCSS                        |
| **Backend (Application)**   | Node.js, Express.js                                |
| **Database**                | MongoDB (Mongoose)                                 |
| **Blockchain**              | Hardhat (Local Ethereum Network) + Smart Contracts |
| **Authentication**          | JWT + bcrypt.js                                    |
| **Infrastructure**          | HTTP Proxy Load Balancer                           |

## 🏗️ Architecture

FarmNet follows a Layered MVC Architecture integrated with blockchain components.

Layers:

- Presentation Layer (View) – Built with React/Next.js for user and farmer dashboards.

- Application Layer (Controller) – Express routes and controllers handle business logic.

- Service Layer (Model) – Mongoose schemas and blockchain interaction services.

- Blockchain Layer – Smart contracts (FarmNetOrder, ProductTracking, OrderVerifier) deployed using Hardhat.

- Load Balancer Layer – Custom HTTP proxy distributing requests across multiple backend servers.

- Database Layer – MongoDB stores user, product, and order data.

## 🧩 Quality Attributes
🔐 1. Security (bcrypt.js)

- Passwords are hashed using bcrypt.js before storage.

- Prevents credential leaks in case of data breaches.

- Combined with JWT for secure session handling.

⚖️ 2. Scalability & Availability (Load Balancer)

- Implemented using http-proxy.

- Distributes traffic evenly among servers (localhost:5000, 5001, 5002).

- Ensures smooth user experience under high load.

⚡ 3. Transparency (Blockchain Smart Contracts)

- Every transaction and order is recorded on the local Hardhat blockchain.

- Immutable transaction history ensures consumer trust.

🧠 4. Maintainability

- Clear MVC separation between Models, Controllers, and Routes.

- Modular code structure allows independent feature updates.

🧩 5. Interoperability

- Uses Web3.js for connecting MetaMask wallet and blockchain.

- Both farmers and consumers use MetaMask for verified transactions.

## 🛠️ Installation Guide

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/FarmNet.git
cd FarmNet
```

### 2. Install dependencies
```
# Backend

cd backend
npm install

# Frontend

cd ../frontend
npm install

```

### 3. Setup environment variables

Create .env files in both backend and frontend with appropriate configurations.

### 4. Start local blockchain (Hardhat)
```
cd backend/blockchain
npx hardhat node
```

### 5. Deploy contracts
```
npx hardhat run scripts/deploy.js --network localhost
```

### 6. Start backend servers
Run three backend servers for load balancing:
```
# Terminals 1, 2, and 3
PORT=5000 node server.js
PORT=5001 node server.js
PORT=5002 node server.js
```

### 7. Start load balancer
```
node loadBalancer.js
```

### 8. Start frontend
```
cd frontend
npm run dev
```
Now open 👉 http://localhost:3000 to access FarmNet.

## 🌐 How It Works

### 🧑‍🌾 Farmer Registration & Login
- Farmers register using **name, email, and phone number**.
- Passwords are securely hashed using **`bcrypt.js`** before being stored in the database for enhanced security.

### 📊 Farmer Dashboard
- Farmers can **add products** with details like *name, price, and quantity*.
- Product data is stored in **MongoDB**.
- The dashboard allows farmers to manage their inventory efficiently.

### 👩‍💻 User Login
- Users log in and connect their **MetaMask wallet**.
- Wallet connection is used to enable blockchain-based order recording and verification.

### 🛒 Market Page
- Displays all available products listed by farmers.
- Users can **select products**, specify quantity, and **place an order**.

### ⛓️ Blockchain Transaction
- When an order is placed, the **order details are recorded** on the **local Hardhat blockchain**.
- A **transaction hash** is generated and displayed to the user.
- This ensures **transparency** and **immutability** of all transactions.

### ⚙️ Load Balancer in Action
- All incoming requests (like `/orders`) are routed through a **load balancer** (`loadBalancer.js`).
- The load balancer uses **Round-Robin distribution** to forward requests to backend servers running on **ports 5000, 5001, and 5002**.
- This improves **performance, fault tolerance, and scalability**.

### 🚚 Order Tracking
- Users can view their order details, including:
  - Product name and price
  - Quantity
  - Transaction ID
  - Blockchain confirmation status
  - Delivery status (e.g., *Pending*, *Delivered*)

---



## 🧠 Architectural Pattern

FarmNet follows a Layered MVC Pattern with Blockchain Integration — combining:

MVC for web application logic

Decentralized ledger for trust and traceability

Load balancing for scalability

Service abstraction for maintainability

## 🧩 System Architecture

  




👨‍💻 Developed By

Priya Kumari
Final Year Project – Blockchain-Enabled Agricultural Marketplace
