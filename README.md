🧑‍🌾 FarmNet – Blockchain-Based Agricultural Marketplace

FarmNet is a blockchain-powered decentralized marketplace that directly connects farmers and consumers, ensuring transparency, traceability, and fair trade.
Built with Next.js, Node.js, Express.js, MongoDB, and Hardhat (Local Ethereum Network), it uses smart contracts to secure and verify transactions.

🚀 Features

✅ Direct farmer–consumer trade
✅ Transparent blockchain-based transactions
✅ Smart contract–powered product verification
✅ Secure user authentication (bcrypt.js)
✅ Load-balanced backend servers for performance
✅ Cart and order management
✅ Dashboard analytics for farmers

🧱 Tech Stack
Layer	Technologies
Frontend (Presentation)	Next.js, React, TailwindCSS
Backend (Application)	Node.js, Express.js
Database	MongoDB (Mongoose)
Blockchain	Hardhat (Local Ethereum Network) + Smart Contracts
Authentication	JWT + bcrypt.js
Infrastructure	HTTP Proxy Load Balancer
🏗️ Architecture

FarmNet follows a Layered MVC Architecture integrated with blockchain components.

Layers:

Presentation Layer (View) – Built with React/Next.js for user and farmer dashboards.

Application Layer (Controller) – Express routes and controllers handle business logic.

Service Layer (Model) – Mongoose schemas and blockchain interaction services.

Blockchain Layer – Smart contracts (FarmNetOrder, ProductTracking, OrderVerifier) deployed using Hardhat.

Load Balancer Layer – Custom HTTP proxy distributing requests across multiple backend servers.

Database Layer – MongoDB stores user, product, and order data.

🧩 Quality Attributes
🔐 1. Security (bcrypt.js)

Passwords are hashed using bcrypt.js before storage.

Prevents credential leaks in case of data breaches.

Combined with JWT for secure session handling.

⚖️ 2. Scalability & Availability (Load Balancer)

Implemented using http-proxy.

Distributes traffic evenly among servers (localhost:5000, 5001, 5002).

Ensures smooth user experience under high load.

⚡ 3. Transparency (Blockchain Smart Contracts)

Every transaction and order is recorded on the local Hardhat blockchain.

Immutable transaction history ensures consumer trust.

🧠 4. Maintainability

Clear MVC separation between Models, Controllers, and Routes.

Modular code structure allows independent feature updates.

🧩 5. Interoperability

Uses Web3.js for connecting MetaMask wallet and blockchain.

Both farmers and consumers use MetaMask for verified transactions.

⚙️ Installation & Setup
1. Clone the repository
git clone https://github.com/yourusername/FarmNet.git
cd FarmNet

2. Install dependencies
cd backend
npm install

cd ../frontend
npm install

3. Setup environment variables

Create .env files in both backend and frontend with appropriate configurations.

4. Start local blockchain (Hardhat)
npx hardhat node

5. Deploy contracts
npx hardhat run scripts/deploy.js --network localhost

6. Start backend servers
node server1.js
node server2.js
node server3.js

7. Start load balancer
node loadBalancer.js

8. Start frontend
npm run dev

🌐 How It Works

User Registration
Users and Farmers register securely (passwords hashed with bcrypt.js).

Login
Users login and connect MetaMask wallet.

Add Products (Farmer)
Farmers list their crops or products through dashboard.

Purchase (User)
Consumers buy directly via smart contracts; blockchain verifies and records.

Order Tracking
Orders are visible in dashboard with status and blockchain transaction ID.

🧠 Architectural Pattern

FarmNet follows a Layered MVC Pattern with Blockchain Integration — combining:

MVC for web application logic

Decentralized ledger for trust and traceability

Load balancing for scalability

Service abstraction for maintainability

👨‍💻 Developed By

Priya Kumari
Final Year Project – Blockchain-Enabled Agricultural Marketplace
