🍔 Food Delivery Platform - Group 5
A multi-platform online food ordering and delivery system connecting Customers, Stores (Partners), and System Administrators. The project is built upon a Service-Oriented Architecture (SOA) with scalability towards Microservices.

🚀 Key Features
The system consists of 3 main subsystems for 3 types of users:

1. Customer - frontend/public-client
Search & Discovery: Search for foods, restaurants, and view featured listings.

Ordering: Add items to cart, apply discount codes, select delivery addresses.

Order Tracking: Real-time order status tracking (Preparing, Delivering, Delivered).

AI Support: Virtual assistant for food recommendations (integrated AI Agent).

Interaction: Rate foods, follow favorite stores.

2. Store Manager - frontend/store-client
Menu Management: Add/Edit/Delete food items, manage Categories.

Order Management: Accept, reject, or update order statuses.

Customization: Configure toppings and food options.

Statistics: View revenue and order reports.

Staff: Manage store staff accounts.

3. Administrator - frontend/admin-client
Dashboard: System overview, user and store statistics.

User Management: View, ban, or unban accounts.

Store Management: Approve new store registration requests.

Support System (Ticket): Handle complaints and support requests.

🛠️ Tech Stack
Backend
Language: JavaScript (Node.js).

Framework: Express.js.

Database: PostgreSQL.

ORM: Sequelize.

Services:

admin-service: Administration logic.

customer-service: Customer logic.

store-service: Store partner logic.

images-service: Image upload handling (Supabase/Local).

public-service: Public APIs.

Frontend
Framework: React (Vite).

UI Library: Shadcn UI, Tailwind CSS.

State Management: Context API.

HTTP Client: Axios.

DevOps & Infrastructure
Containerization: Docker, Docker Compose.

📂 Project Structure
group5-s-project/
├── backend/                # Backend Source Code (Monolith/Core)
├── deploy/                 # Nginx Configuration
├── frontend/
│   ├── admin-client/       # Web App for Administrators
│   ├── public-client/      # Web App for Customers
│   └── store-client/       # Web App for Store Managers
├── services/               # Independent Microservices
│   ├── admin-service/
│   ├── customer-service/
│   ├── store-service/
│   └── ...
├── init.sql                # Database Initialization Script
├── docker-compose.yml      # Main Docker Configuration
└── docker-compose.micro.yml # Docker Configuration for Microservices

🔧 Installation Guide (Local Development)
Option 1: Using Docker (Recommended)
Ensure Docker and Docker Compose are installed on your machine.
1. Clone the repository:
   git clone <repository_url>
cd group5-s-project
2. Start the entire system:
   docker-compose up --build
3. Access:
   Backend API: http://localhost:3000 (or the configured port)
   Public Client: http://localhost:5173
   Store Client: http://localhost:5174
   Admin Client: http://localhost:5175
