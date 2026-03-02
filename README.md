# VibeCoding Starter Kit 2.0 - GoClean Web Application

A comprehensive, production-ready full-stack web application starter kit built with modern technologies and best practices. This monorepo provides a complete foundation for building scalable web applications with Go Fiber backend and React frontend.

## 🚀 Overview

VibeCoding Starter Kit 2.0 is a meticulously crafted starter template for developing modern web applications. It features:

- **Backend**: Go Fiber v2 with GORM, JWT authentication, and PostgreSQL
- **Frontend**: React 18+ with TypeScript, Vite, Tailwind CSS, and Shadcn UI
- **Architecture**: Clean Architecture principles with modular separation
- **Deployment**: Dockerized deployment ready for Railway
- **Development**: Comprehensive development workflows and skills system

## 🏗️ Project Structure

```
vibecoding-starterkit2/
├── rules/                 # Coding standards and best practices
│   ├── backend-rules.md  # Go Fiber backend standards
│   ├── frontend-rules.md # React/Tailwind frontend standards
│   └── documentation-rules.md # Documentation guidelines
├── skills/               # Development skills and capabilities
│   ├── backend_dev/      # Go backend development
│   ├── frontend_dev/     # React frontend development
│   ├── crud_generator/   # CRUD operation generation
│   ├── backend_security/ # Security implementation
│   ├── asset_generator/  # Asset creation and management
│   ├── app_runner/       # Application execution
│   ├── git_manager/      # Git operations
│   ├── documentation/    # Documentation generation
│   └── prd/              # Product requirements
├── workflows/            # Step-by-step development workflows
│   ├── 01_backend-setup.md           # Backend initialization
│   ├── 02_frontend-landing-page.md   # Landing page creation
│   ├── 03_admin-dashboard-integration.md # Admin dashboard
│   ├── 04_testing-and-debugging.md   # Testing procedures
│   ├── 05_admin-user-management.md   # User management
│   ├── 06_deployment-to-railway.md   # Deployment to Railway
│   ├── 07_documentation-maintenance.md # Documentation
│   └── 08_testing-playground.md      # Testing environment
└── README.md             # This file
```

## 🛠️ Technology Stack

### Backend Technologies

- **Go 1.21+**: High-performance programming language
- **Fiber v2**: Express-inspired web framework
- **GORM**: ORM for database operations
- **PostgreSQL**: Production-ready relational database
- **JWT**: JSON Web Token authentication
- **Bcrypt**: Secure password hashing
- **Godotenv**: Environment variable management

### Frontend Technologies

- **React 18+**: Modern UI library with hooks
- **TypeScript**: Type-safe JavaScript
- **Vite 6+**: Fast build tool and dev server
- **Tailwind CSS 3+**: Utility-first CSS framework
- **Shadcn UI**: Beautiful UI component library
- **Framer Motion**: Smooth animations
- **Zustand**: Lightweight state management
- **TanStack Table**: Advanced data tables
- **Axios**: HTTP client for API calls

### Development & Deployment

- **Docker**: Containerization for deployment
- **Railway**: Cloud deployment platform
- **PWA**: Progressive Web App capabilities
- **ESLint & Prettier**: Code quality tools

## 📋 Core Features

### Backend Features

- ✅ Modular Clean Architecture
- ✅ JWT Authentication System
- ✅ Password Hashing with Bcrypt
- ✅ PostgreSQL Database Integration
- ✅ CORS Configuration
- ✅ Structured Error Handling
- ✅ Environment Configuration
- ✅ Middleware Support (Auth, Logger, CORS)
- ✅ RESTful API Design
- ✅ Soft Delete Implementation

### Frontend Features

- ✅ Responsive Landing Page
- ✅ Admin Dashboard with Sidebar
- ✅ Multi-tab Navigation System
- ✅ User Authentication Flow
- ✅ Protected Routes
- ✅ Data Tables with Pagination
- ✅ Export Functionality (CSV, XLSX, PDF)
- ✅ Modern UI Components
- ✅ PWA Configuration
- ✅ Mobile-First Design

### Admin Dashboard Features

- ✅ User Management (CRUD Operations)
- ✅ Service Management
- ✅ Transaction Tracking
- ✅ Statistics and Analytics
- ✅ Bulk Operations
- ✅ Advanced Filtering and Sorting
- ✅ Data Export Capabilities
- ✅ Role-Based Access Control

## 🚀 Quick Start

### Prerequisites

- Go 1.21+ installed
- Node.js 18+ and npm
- PostgreSQL database
- Git

### Installation & Setup

1. **Clone the repository**

   ```bash
   git clone <repository-url>
   cd vibecoding-starterkit2
   ```

2. **Setup Backend**

   ```bash
   # Navigate to backend directory
   cd backend

   # Initialize Go module
   go mod init GoClean-backend

   # Install dependencies
   go get -u github.com/gofiber/fiber/v2
   go get -u gorm.io/gorm
   go get -u gorm.io/driver/postgres
   go get -u github.com/joho/godotenv
   go get -u github.com/golang-jwt/jwt/v5
   go get -u golang.org/x/crypto/bcrypt
   go get -u github.com/google/uuid

   # Create project structure
   mkdir -p cmd config database handlers middleware models routes utils
   ```

3. **Setup Frontend**

   ```bash
   # Navigate to frontend directory
   cd frontend

   # Install dependencies
   npm install
   npm install --legacy-peer-deps framer-motion lucide-react react-helmet-async clsx tailwind-merge vite-plugin-pwa react-router-dom @types/node
   npm install -D tailwindcss@^3.4 postcss autoprefixer

   # Initialize Tailwind CSS
   npx tailwindcss init -p
   ```

4. **Environment Configuration**

   Backend (.env):

   ```env
   DB_HOST=localhost
   DB_PORT=5432
   DB_USER=postgres
   DB_PASSWORD=your_password
   DB_NAME=goclean
   JWT_SECRET=your_jwt_secret
   PORT=8080
   ```

   Frontend (.env):

   ```env
   VITE_API_URL=http://localhost:8080/api
   ```

5. **Run the Application**

   ```bash
   # Start backend
   cd backend
   go run cmd/main.go

   # Start frontend (in new terminal)
   cd frontend
   npm run dev
   ```

## 📖 Development Workflows

The project includes comprehensive workflows for different development scenarios:

### 1. Backend Setup (`01_backend-setup.md`)

- Go module initialization
- Dependency installation
- Project structure creation
- Database configuration
- Authentication setup

### 2. Frontend Landing Page (`02_frontend-landing-page.md`)

- Vite project initialization
- Tailwind CSS configuration
- Component creation
- PWA setup
- Asset management

### 3. Admin Dashboard Integration (`03_admin-dashboard-integration.md`)

- API client setup
- State management with Zustand
- Sidebar navigation
- Multi-tab system
- Protected routes

### 4. Testing & Debugging (`04_testing-and-debugging.md`)

- End-to-end testing
- Browser automation
- Error handling
- Production troubleshooting

### 5. User Management (`05_admin-user-management.md`)

- CRUD operations
- Data table implementation
- Export functionality
- Bulk operations

### 6. Deployment (`06_deployment-to-railway.md`)

- Docker configuration
- Railway deployment
- Production environment setup
- Health checks

## 🛡️ Security Features

- **JWT Authentication**: Secure token-based authentication
- **Password Hashing**: Bcrypt for secure password storage
- **CORS Protection**: Proper CORS configuration
- **Input Validation**: Comprehensive input sanitization
- **Environment Variables**: Secure secret management
- **SQL Injection Prevention**: GORM parameterized queries
- **XSS Protection**: Frontend input sanitization

## 📊 Database Schema

The application uses PostgreSQL with the following core tables:

### Users Table

- `id` (UUID, Primary Key)
- `name` (String)
- `email` (String, Unique)
- `password` (String, Hashed)
- `role` (String)
- `created_at` (Timestamp)
- `updated_at` (Timestamp)
- `deleted_at` (Timestamp, Soft Delete)

### Services Table

- `id` (UUID, Primary Key)
- `name` (String)
- `description` (Text)
- `price` (Decimal)
- `duration` (Integer)
- `is_active` (Boolean)

### Transactions Table

- `id` (UUID, Primary Key)
- `user_id` (UUID, Foreign Key)
- `service_id` (UUID, Foreign Key)
- `amount` (Decimal)
- `status` (String)
- `payment_method` (String)
- `created_at` (Timestamp)

## 🎨 UI/UX Design

The application follows modern design principles:

### Color Scheme

- **Primary**: Sky Blue (#0ea5e9)
- **Secondary**: Light Blue (#f0f9ff)
- **Background**: White (#ffffff)
- **Foreground**: Dark Slate (#0f172a)

### Typography

- **Primary Font**: Inter (Sans-serif)
- **Responsive**: Mobile-first design approach
- **Consistent**: Unified spacing and sizing

### Components

- **Shadcn UI**: Pre-built accessible components
- **Custom Components**: Tailored for specific use cases
- **Responsive**: Works on all device sizes

## 🔧 Development Skills System

The project includes a comprehensive skills system for different development tasks:

### Available Skills

1. **Backend Development**: Go Fiber and GORM expertise
2. **Frontend Development**: React and Tailwind CSS mastery
3. **CRUD Generation**: Automated CRUD operation creation
4. **Security Implementation**: Authentication and authorization
5. **Asset Generation**: Logo and image creation
6. **App Runner**: Application execution and management
7. **Git Management**: Version control operations
8. **Documentation**: Comprehensive documentation creation
9. **PRD Creation**: Product requirement documentation

## 🚀 Deployment

### Railway Deployment

The application is configured for seamless deployment on Railway:

1. **Docker Support**: Both backend and frontend are dockerized
2. **Health Checks**: Automatic health monitoring
3. **Environment Variables**: Secure configuration management
4. **Build Optimization**: Efficient build processes
5. **Scalability**: Ready for production traffic

### Deployment Steps

1. **Backend Deployment**

   ```dockerfile
   # Build and deploy backend
   docker build -t backend .
   railway deploy
   ```

2. **Frontend Deployment**
   ```dockerfile
   # Build and deploy frontend
   npm run build
   railway deploy
   ```

## 🧪 Testing

The project includes comprehensive testing strategies:

### Backend Testing

- Unit tests for handlers and services
- Integration tests for API endpoints
- Database transaction testing
- Authentication flow testing

### Frontend Testing

- Component testing with React Testing Library
- End-to-end testing with Browser automation
- User interaction testing
- Responsive design testing

### Manual Testing Flows

1. **Landing Page Verification**: Navigation and layout
2. **Admin Login Flow**: Authentication process
3. **Dashboard Testing**: Interactive features
4. **User Management**: CRUD operations
5. **Export Functionality**: Data export validation

## 📈 Performance Optimization

### Backend Optimization

- Connection pooling for database
- JWT token caching
- Efficient query optimization
- Middleware optimization

### Frontend Optimization

- Code splitting with Vite
- Image optimization
- Bundle size reduction
- PWA caching strategies

### Database Optimization

- Index optimization
- Query performance monitoring
- Connection management
- Migration strategies

## 🤝 Contributing

### Development Guidelines

1. Follow the established coding standards
2. Use the provided workflows for development
3. Maintain comprehensive documentation
4. Write tests for new features
5. Follow security best practices

### Code Review Process

1. Backend code follows Go standards
2. Frontend code uses TypeScript strictly
3. Database migrations are backward compatible
4. Security review for all authentication code
5. Performance considerations for new features

## 📚 Documentation

The project maintains extensive documentation:

### Rule Documents

- `backend-rules.md`: Backend development standards
- `frontend-rules.md`: Frontend development standards
- `documentation-rules.md`: Documentation guidelines

### Workflow Documents

- Step-by-step development guides
- Deployment procedures
- Testing methodologies
- Troubleshooting guides

### API Documentation

- RESTful endpoint documentation
- Request/response formats
- Authentication requirements
- Error handling patterns

## 🆘 Support

### Common Issues

1. **CORS Errors**: Check backend CORS configuration
2. **Database Connection**: Verify PostgreSQL is running
3. **JWT Issues**: Validate secret configuration
4. **Build Errors**: Check Node.js and Go versions
5. **Deployment Issues**: Review Railway configuration

### Troubleshooting

- Check application logs
- Verify environment variables
- Test database connectivity
- Validate JWT token generation
- Review browser console errors

## 📄 License

This project is proprietary software developed for modern web application development. All rights reserved.

## 🏆 Acknowledgments

- **Go Fiber Team**: For the excellent web framework
- **Tailwind CSS**: For the utility-first CSS framework
- **Shadcn UI**: For beautiful UI components
- **Vite Team**: For the fast build tool
- **React Team**: For the incredible UI library

---

**Version**: 2.0.0  
**Last Updated**: March 2025  
**Status**: Production Ready
