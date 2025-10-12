# Pharmacy Revenue Management System

A comprehensive web application built with React, FastAPI, and Tauri for managing pharmacy revenue data, analytics, and reporting.

## 🚀 Features

### 📊 Dashboard
- **Revenue Overview**: Total revenue, pharmacy count, doctor count, and growth rate
- **Interactive Charts**: Revenue by pharmacy and doctor with bar charts
- **Real-time Data**: Live updates and refresh functionality

![Dashboard](https://github.com/Zubair121Md/pharmacy-revenue-app/blob/master/screenshots/dashboard.png)

### 📁 File Upload
- **Drag & Drop Interface**: Easy Excel file uploads
- **Multiple File Types**: Support for invoice files and master mapping data
- **File Validation**: Automatic validation of uploaded files

![File Upload](https://github.com/Zubair121Md/pharmacy-revenue-app/blob/master/screenshots/file-upload.png)

### 📈 Analytics
- **Multiple Revenue Views**: Revenue by pharmacy, doctor, rep, HQ, area, and product
- **Chart Types**: Bar charts and pie charts for data visualization
- **Data Distribution**: Comprehensive analytics with detailed breakdowns
- **Product Revenue**: Specialized product revenue analysis

![Analytics](https://github.com/Zubair121Md/pharmacy-revenue-app/blob/master/screenshots/analytics.png)

### 🔍 Unmatched Records
- **Record Management**: Review and manage unmatched pharmacy records
- **Search & Filter**: Advanced search and filtering capabilities
- **Status Tracking**: Track pending, processed, and completed records

![Unmatched Records](https://github.com/Zubair121Md/pharmacy-revenue-app/blob/master/screenshots/unmatched-records.png)

### 📋 Recent Uploads
- **Upload History**: Track all recent file uploads
- **Processing Summary**: Detailed processing statistics
- **Export Options**: CSV and Excel export functionality

![Recent Uploads](https://github.com/Zubair121Md/pharmacy-revenue-app/blob/master/screenshots/recent-uploads.png)

### ⚙️ Admin Panel
- **User Management**: Add, edit, and delete users
- **System Overview**: Monitor system health and performance
- **System Settings**: Configure application settings

![Admin Panel](https://github.com/Zubair121Md/pharmacy-revenue-app/blob/master/screenshots/admin-panel.png)

## 🛠️ Tech Stack

### Frontend
- **React 18**: Modern UI framework
- **Redux Toolkit**: State management
- **Chart.js**: Data visualization
- **Tauri**: Desktop application wrapper
- **Ant Design**: UI component library

### Backend
- **FastAPI**: High-performance Python web framework
- **SQLite**: Lightweight database
- **Pydantic**: Data validation
- **Uvicorn**: ASGI server

### Development Tools
- **ESLint**: Code linting
- **Prettier**: Code formatting
- **Git**: Version control

## 📦 Installation

### Prerequisites
- Node.js 18+ 
- Python 3.8+
- Rust (for Tauri)

### Backend Setup
```bash
cd backend
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
python -m uvicorn app.main_complete:app --host 127.0.0.1 --port 8000 --reload
```

### Frontend Setup
```bash
cd frontend
npm install
npm start
```

### Tauri Desktop App
```bash
npm run tauri dev
```

## 🚀 Quick Start

1. **Clone the repository**
   ```bash
   git clone https://github.com/Zubair121Md/pharmacy-revenue-app.git
   cd pharmacy-revenue-app
   ```

2. **Start the backend**
   ```bash
   cd backend
   source venv/bin/activate
   python -m uvicorn app.main_complete:app --host 127.0.0.1 --port 8000 --reload
   ```

3. **Start the frontend**
   ```bash
   cd frontend
   npm start
   ```

4. **Access the application**
   - Web: http://localhost:3000
   - API: http://localhost:8000
   - API Docs: http://localhost:8000/docs

## 📊 API Endpoints

### Authentication
- `POST /api/v1/auth/login` - User login
- `POST /api/v1/auth/logout` - User logout

### Analytics
- `GET /api/v1/analytics/revenue-by-pharmacy` - Pharmacy revenue data
- `GET /api/v1/analytics/revenue-by-doctor` - Doctor revenue data
- `GET /api/v1/analytics/revenue-by-product` - Product revenue data
- `GET /api/v1/analytics/dashboard` - Dashboard overview

### File Management
- `POST /api/v1/files/upload` - Upload files
- `GET /api/v1/files/recent` - Recent uploads
- `GET /api/v1/files/unmatched` - Unmatched records

## 🔧 Configuration

### Environment Variables
Create a `.env` file in the backend directory:
```env
DATABASE_URL=sqlite:///./pharmacy_revenue.db
SECRET_KEY=your-secret-key-here
DEBUG=True
```

### Database
The application uses SQLite by default. Database file: `backend/pharmacy_revenue.db`

## 📱 Desktop Application

The application can be packaged as a desktop app using Tauri:

```bash
npm run tauri build
```

This creates platform-specific installers in the `src-tauri/target/release/` directory.

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Authors

- **Zubair Ishaq** - *Initial work* - [Zubair121Md](https://github.com/Zubair121Md)

## 🙏 Acknowledgments

- React team for the amazing framework
- FastAPI team for the high-performance backend
- Tauri team for the desktop app capabilities
- Chart.js for data visualization

## 📞 Support

For support, email zubairishaq@example.com or create an issue in the repository.

---

**Pharmacy Revenue Management System** - Streamlining pharmacy revenue tracking and analytics.