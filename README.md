# 🏥 Pharmacy Revenue Management System

A comprehensive full-stack application for managing pharmacy revenue, doctor allocations, and sales analytics with advanced ID-based matching and flexible data processing, designed to operate offline after initial setup.

## 🎯 Overview

The Pharmacy Revenue Management System processes pharmacy invoice data with flexible column mapping, matches invoices with master data using a deterministic ID generation algorithm, and generates comprehensive revenue analytics and visualizations.

### Key Features
- **ID Generation**: Creates unique Pharmacy_IDs (e.g., "GM-CAL-001") from pharmacy names
- **Flexible Mapping**: Handles various Excel column name variations
- **Revenue Analytics**: Comprehensive dashboards with role-based access
- **Offline Operation**: All dependencies bundled locally
- **Role-Based Access**: Super Admin, Admin, User permissions
- **Data Export**: Excel, CSV, PDF with data masking

## 🏗️ Architecture

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Frontend      │    │   Backend       │    │   Database      │
│   (React)       │◄──►│   (FastAPI)     │◄──►│   (PostgreSQL)  │
│   Port: 3000    │    │   Port: 8000    │    │   Port: 5432    │
└─────────────────┘    └─────────────────┘    └─────────────────┘
         │                       │                       │
         ▼                       ▼                       ▼
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Nginx         │    │   Redis         │    │   ML Models     │
│   (Reverse      │    │   (Cache)       │    │   (Fallback)    │
│    Proxy)       │    │   Port: 6379    │    │                 │
└─────────────────┘    └─────────────────┘    └─────────────────┘
```

## 🚀 Quick Start

### Prerequisites
- Docker 24.0+
- Docker Compose 2.20+
- 8GB RAM minimum, 16GB recommended

### Installation

1. **Clone and setup**:
```bash
cd pharmacy-revenue-app
chmod +x deploy.sh
./deploy.sh
```

2. **Access the application**:
- Frontend: https://localhost:3000
- Backend API: https://localhost:8000
- API Docs: https://localhost:8000/docs

### Default Login
- **Super Admin**: admin / admin123
- **Admin**: manager / manager123
- **User**: user / user123

## 📊 Sample Data

### Master Data Format
```
REP_Names | Doctor_Names | Doctor_ID | Pharmacy_Names | Pharmacy_ID | Product_Names | Product_ID | Product_Price | HQ | AREA
VIKRAM    | DR SHAJIKUMAR | DR_SHA_733| Gayathri Medicals | GM_CAL_001 | ENDOL 650 | PRD_6824 | 13.46 | CL | CALICUT
```

### Invoice Data Format
```
Pharmacy_Name | Product | Quantity | Amount
Gayathri Medicals | ENDOL 650 | 20 | 269.2
```

## 🔧 Configuration

### Environment Variables
```bash
# Database
POSTGRES_DB=pharmacy_revenue
POSTGRES_USER=pharmacy_user
POSTGRES_PASSWORD=pharmacy_password

# JWT
SECRET_KEY=your-secret-key
ALGORITHM=HS256
ACCESS_TOKEN_EXPIRE_MINUTES=30

# License
LICENSE_KEY=your-license-key
```

## 📁 Project Structure

```
pharmacy-revenue-app/
├── frontend/                 # React application
├── backend/                  # FastAPI application
├── dependencies/             # Offline dependencies
├── docker-compose.yml        # Docker orchestration
├── deploy.sh                # Deployment script
└── README.md                # This file
```

## 🛠️ Development

### Backend Development
```bash
cd backend
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
uvicorn app.main:app --reload
```

### Frontend Development
```bash
cd frontend
npm install
npm start
```

## 📞 Support

For technical support:
1. Check the troubleshooting section
2. Review logs in `backend/logs/`
3. Export logs via the UI for support

## 📄 License

This project is proprietary software. All rights reserved.

---

**Version**: 2.0  
**Last Updated**: December 2024
