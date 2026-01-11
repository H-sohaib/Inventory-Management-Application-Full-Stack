# Equipment Reservation System - Full Stack Application

![Home Page](./gestion%20stock.png)

## 📋 Table of Contents

- [Overview](#overview)
- [Screenshots](#screenshots)
- [Tech Stack](#tech-stack)
- [Features](#features)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Running the Application](#running-the-application)
- [User Roles](#user-roles)
- [API Endpoints](#api-endpoints)
- [License](#license)

## 🎯 Overview

The **Equipment Reservation System** is a comprehensive full-stack web application designed for Moulay Ismail University to streamline equipment management and reservation processes. The system provides role-based access for students, technicians, and managers, enabling efficient tracking, booking, and maintenance of laboratory and technical equipment.

### Key Objectives

- Simplify equipment reservation workflow for students
- Enable efficient inventory management for technicians
- Provide oversight and approval mechanisms for managers
- Reduce equipment loss and improve maintenance tracking
- Implement real-time notifications and status updates

### Student Dashboard

Features equipment browsing, reservation cart, and calendar view for managing bookings.

### Technician Dashboard

Equipment inventory management with QR code generation and repair status tracking.

### Manager Dashboard

Reservation approval system with stock monitoring and usage history analytics.

## 🛠 Tech Stack

### Frontend

- **React.js 19.1.0** - Component-based UI library
- **React Router DOM 7.5.0** - Client-side routing
- **React Big Calendar 1.18.0** - Calendar views for reservations
- **QRCode.react 4.2.0** - QR code generation for equipment
- **Moment.js 2.30.1** - Date/time manipulation
- **CSS3** - Custom styling with glassmorphism effects

### Backend

- **Node.js** - JavaScript runtime environment
- **Express.js** - Web application framework
- **PostgreSQL** - Relational database management
- **Nodemailer** - Email notification service
- **Multer** - File upload middleware

## ✨ Features

### For Students (Etudiant)

- 📦 **Equipment Browsing** - Search and filter available equipment by category
- 🛒 **Shopping Cart System** - Add multiple items before checkout
- 📅 **Reservation Calendar** - View upcoming reservations in calendar/list format
- 🔔 **Real-time Notifications** - Status updates and approval alerts
- 📜 **Reservation History** - Track past and current reservations
- ❓ **Help & FAQ** - Comprehensive guidance system

### For Technicians (Technicien)

- ➕ **Equipment Management** - Add, update, and delete equipment entries
- 📊 **Dual Inventory Types** - Manage stockable and solo equipment separately
- 🔧 **Status Tracking** - Mark equipment as available, in repair, or unavailable
- 📷 **Image Uploads** - Attach photos to equipment entries
- 🔗 **Datasheet Links** - Include technical documentation URLs
- 📱 **QR Code Generation** - Create scannable codes linking to datasheets or info
- 🔔 **Notification Center** - Track equipment-related alerts

### For Managers (Responsable)

- ✅ **Approval Workflow** - Approve or reject reservation requests
- 📊 **Stock Monitoring** - Track equipment quantities and low-stock alerts
- 📈 **Usage Analytics** - View activity history and usage patterns
- 🔍 **Equipment Filtering** - Filter by status, category, and availability
- 📧 **Email Notifications** - Automated alerts to students on status changes
- 📋 **Multi-tab Interface** - Pending, confirmed, and usage history views

### System-Wide Features

- 🌓 **Dark/Light Mode** - User preference persistence
- 📱 **Responsive Design** - Mobile-friendly interface
- 🔐 **Role-based Authentication** - Secure access control
- 📧 **Contact Form** - Direct communication channel
- ⬆️ **Back-to-Top Navigation** - Enhanced user experience
- 🎨 **Glassmorphism UI** - Modern aesthetic design

## 📂 Project Structure

```
.
├── client/                      # React frontend application
│   ├── public/
│   │   ├── index.html          # Main HTML template
│   │   ├── manifest.json       # PWA configuration
│   │   └── robots.txt          # SEO crawler rules
│   ├── src/
│   │   ├── App.jsx             # Main app component with routing
│   │   ├── index.jsx           # React DOM entry point
│   │   ├── css/                # Stylesheets
│   │   │   ├── index.css       # Global styles and variables
│   │   │   ├── home.css        # Landing page styles
│   │   │   ├── login.css       # Authentication page styles
│   │   │   ├── etudiant.css    # Student dashboard styles
│   │   │   ├── technicien.css  # Technician dashboard styles
│   │   │   └── responsable.css # Manager dashboard styles
│   │   ├── pages/              # Page components
│   │   │   ├── home.jsx        # Landing page
│   │   │   ├── login.jsx       # Login page
│   │   │   ├── etudiant.jsx    # Student dashboard
│   │   │   ├── technicien.jsx  # Technician dashboard
│   │   │   └── responsable.jsx # Manager dashboard
│   │   └── svg/                # SVG assets
│   ├── package.json            # Frontend dependencies
│   └── README.md               # Frontend documentation
│
└── server/                      # Express backend API
    ├── config/
    │   └── dbConfig.js         # Database connection configuration
    ├── controllers/            # Business logic handlers
    │   ├── contactController.js        # Contact form processing
    │   ├── equipmentController.js      # Equipment CRUD operations
    │   ├── notificationController.js   # Notification management
    │   ├── reservationController.js    # Reservation workflow
    │   └── userController.js           # User authentication
    ├── db/                     # Database scripts
    │   ├── generate.sql        # Schema creation
    │   ├── seed.sql            # Initial data population
    │   └── migration/          # Database migrations
    ├── middleware/
    │   └── uploadMiddleware.js # File upload handling (Multer)
    ├── routes/                 # API endpoint definitions
    │   └── contactRoutes.js    # Contact form routes
    ├── utilities/
    │   └── templates/
    │       └── contactEmail.js # Email template for contacts
    ├── uploads/                # Uploaded files storage
    ├── public/                 # Static assets
    ├── .env                    # Environment variables
    ├── server.js               # Express server entry point
    └── package.json            # Backend dependencies
```

## 🚀 Installation

### Prerequisites

- Node.js (v14 or higher)
- PostgreSQL (v12 or higher)
- npm or yarn package manager

### Step 1: Clone the Repository

```sh
git clone <repository-url>
cd "Inventory Management Application - Full Stack"
```

### Step 2: Install Server Dependencies

```sh
cd server
npm install
```

### Step 3: Install Client Dependencies

```sh
cd ../client
npm install
```

### Step 4: Configure Environment Variables

Create a `.env` file in the `server/` directory:

```env
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_password
DB_NAME=GESTION_STOCK
EMAIL_USER=your_email@gmail.com
EMAIL_PASSWORD=your_app_password
EMAIL_CONTACT=admin@example.com
PORT=8080
```

### Step 5: Initialize the Database

```sh
cd server/db
psql -U postgres -f generate.sql
psql -U postgres -f seed.sql
```

## 🎬 Running the Application

### Start the Backend Server

```sh
cd server
npm start
```

The server will run on `http://localhost:8080`

### Start the Frontend Application

Open a new terminal:

```sh
cd client
npm start
```

The client will run on `http://localhost:3000`

### Access the Application

Navigate to `http://localhost:3000` in your web browser.

## 👥 User Roles

### Student (Etudiant)

- **Purpose**: Reserve equipment for academic projects
- **Permissions**: Browse equipment, create reservations, view history
- **Login**: Student credentials from database

### Technician (Technicien)

- **Purpose**: Manage equipment inventory and maintenance
- **Permissions**: Full CRUD on equipment, generate QR codes, update status
- **Login**: Technician credentials from database

### Manager (Responsable)

- **Purpose**: Oversee reservations and stock levels
- **Permissions**: Approve/reject reservations, monitor inventory, view analytics
- **Login**: Manager credentials from database

## 🔌 API Endpoints

### Authentication

- `POST /api/users/login` - User authentication

### Equipment

- `GET /api/equipments` - Retrieve all equipment
- `POST /api/equipments` - Add new equipment (Technician)
- `PUT /api/equipments/:id` - Update equipment (Technician)
- `DELETE /api/equipments/:id` - Delete equipment (Technician)

### Reservations

- `GET /api/reservations` - Get all reservations
- `POST /api/reservations` - Create reservation (Student)
- `PATCH /api/reservations/:id` - Update status (Manager)

### Notifications

- `GET /api/notifications/:userId` - Get user notifications
- `PATCH /api/notifications/:id` - Mark as read

### Contact

- `POST /api/contact` - Submit contact form

## 📄 License

MIT License - Feel free to use this project for educational purposes.

---

**Developed by GP Solutions** | Moulay Ismail University, Meknes, Morocco
