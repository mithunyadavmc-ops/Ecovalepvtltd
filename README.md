<div align="center">
<img width="1200" height="475" alt="GHBanner" src="https://github.com/user-attachments/assets/0aa67016-6eaf-458a-adb2-6e31a0763ed6" />
</div>

# Ecovale HR Management System

> **Production-ready Enterprise HR Platform** • Full-stack TypeScript/Java • Spring Boot 3.2 + React 18 + MySQL 8

[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.2.1-brightgreen.svg)](https://spring.io/projects/spring-boot)
[![React](https://img.shields.io/badge/React-18-blue.svg)](https://reactjs.org/)
[![Java](https://img.shields.io/badge/Java-17-orange.svg)](https://openjdk.java.net/)
[![MySQL](https://img.shields.io/badge/MySQL-8.0-blue.svg)](https://www.mysql.com/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.2-blue.svg)](https://www.typescriptlang.org/)

---

## 🌐 Live Demo

<div align="center">
<table>
<tr>
<td align="center" width="50%">

### 🖥️ **Frontend Demo**
**[https://ecovale-hr.netlify.app](https://ecovale-hr.netlify.app)**  
*(Replace with your Netlify URL)*

</td>
<td align="center" width="50%">

### ⚙️ **Backend API**
**[https://ecovale-hr.railway.app](https://ecovale-hr.railway.app)**  
*(Replace with your Railway URL)*

</td>
</tr>
</table>
</div>

### 🔑 Demo Credentials - Try It Now!

```
👤 Admin Account (Full Access)
   Username: demo_admin
   Password: Demo@2026!Secure

👔 Manager Account (Approval Rights)
   Username: john_manager
   Password: Manager@2026!

👨‍💻 Employee Account (Standard User)
   Username: alice_employee
   Password: Employee@2026!
```

**📖 More test accounts available in [DEMO-CREDENTIALS.md](DEMO-CREDENTIALS.md)**

---

## 📋 Table of Contents

- [Live Demo](#-live-demo)
- [Why This Project Matters](#-why-this-project-matters)
- [Overview](#-overview)
- [Key Features](#-key-features)
- [Technology Stack](#-technology-stack)
- [Quick Start (Local Development)](#-quick-start-local-development)
- [Deploy Your Own (5 Minutes)](#-deploy-your-own-5-minutes)
- [Architecture](#-architecture)
- [API Documentation](#-api-documentation)
- [Testing & Quality](#-testing--quality)
- [Documentation](#-documentation)
- [Contributing](#-contributing)
- [Support](#-support)

---

## 💡 Why This Project Matters

### For Recruiters & Technical Evaluators

This project demonstrates **production-ready full-stack development skills** with real-world complexity:

**🏗️ Enterprise Architecture**
- Clean 3-tier architecture (Presentation → Business → Data)
- RESTful API design with versioning (`/api/v1`)
- JWT authentication with role-based access control (RBAC)
- Comprehensive audit logging for compliance

**💻 Modern Tech Stack**
- **Backend:** Spring Boot 3.2, Java 17, MySQL 8.0, Flyway migrations
- **Frontend:** React 18, TypeScript 5.2, Vite build system
- **Security:** JWT tokens, BCrypt hashing, rate limiting
- **DevOps:** Docker, CI/CD ready, cloud deployment configs

**📈 Production Best Practices**
- Database migrations with rollback support (Flyway)
- Health checks & monitoring (Prometheus/Grafana)
- API documentation (OpenAPI/Swagger)
- Comprehensive testing (unit, integration, load tests)
- Security hardening (CORS, CSRF, SQL injection prevention)

**🎯 Real-World Problem Solving**
- Complex business logic (two-level leave approvals, payroll calculations)
- Data integrity (overlapping leave detection, audit trails)
- Scalability considerations (connection pooling, caching strategies)
- User experience (responsive design, error handling)

**📚 Documentation Quality**
- 59 KB of technical documentation
- Architecture diagrams (Mermaid.js)
- Deployment guides for multiple platforms
- API examples and testing scenarios

### Business Value

This HR system solves real organizational challenges:
- ✅ Streamlined employee onboarding and offboarding
- ✅ Automated leave approval workflows reducing HR workload
- ✅ Accurate payroll processing with audit trails
- ✅ Compliance reporting for labor regulations
- ✅ Self-service employee portal reducing HR inquiries

---

## 🎯 Overview

A **complete, production-ready HR management platform** built with modern enterprise technologies. This system manages the entire employee lifecycle from onboarding to offboarding, with advanced features like automated leave workflows, payroll processing, and comprehensive compliance reporting.

**What Makes This System Enterprise-Ready:**
- 🔐 **Bank-grade security:** JWT authentication, BCrypt password hashing, rate limiting
- 📊 **Built to scale:** Horizontal scaling, connection pooling, optimized database queries
- 🔍 **Full observability:** Prometheus metrics, structured logging, health checks
- 📱 **Modern UX:** Responsive React UI with TypeScript for type safety
- 🚀 **API-first design:** RESTful API with OpenAPI documentation
- 🔄 **CI/CD ready:** Automated testing, Docker containers, cloud deployment configs

---

## ✨ Key Features

### 👥 Employee Management
- **Complete Lifecycle Management:** Onboarding, profile updates, designation changes, offboarding
- **Organizational Structure:** Department and designation hierarchies
- **Document Management:** Secure storage for contracts, certificates, ID proofs
- **Salary Administration:** CTC breakdowns, allowances, deductions

### 🏖️ Leave Management (Featured Module)
- **Two-Level Approval Workflow:** Manager approval → Admin approval
- **9 Leave Types:** Casual, Sick, Earned, Maternity, Paternity, Unpaid, Compensatory, Bereavement, Marriage
- **Smart Validations:** Overlapping leave detection, balance verification, future date checks
- **Statistics Dashboard:** Leave trends, utilization rates, pending approvals
- **Audit Trail:** Complete history of submissions, approvals, rejections

### 📅 Attendance & Time Tracking
- **Clock In/Out:** Daily attendance recording with timestamps
- **Overtime Calculation:** Automatic computation based on work hours
- **Reports & Analytics:** Monthly attendance summaries, late arrivals, early departures
- **Payroll Integration:** Direct feed to salary calculation engine

### 💰 Payroll & Financial Management
- **Automated Salary Processing:** Monthly payslip generation with breakdowns
- **Loan Management:** EMI calculation, repayment tracking, interest computation
- **Advance Payments:** Request workflow, deduction scheduling
- **Tax Support:** Basic tax calculation framework (extensible for local regulations)
- **Annexure Generation:** PDF export for salary statements

### 📝 Audit & Compliance
- **Comprehensive Logging:** Every action logged with user, timestamp, details (Spring AOP)
- **Tamper-Proof:** Admin-only access to audit logs
- **Compliance Reports:** Data for labor law compliance, salary registers
- **Data Integrity:** Foreign key constraints, transaction management

### 🔐 Security & Authentication
- **JWT-Based Auth:** 24-hour access tokens, 7-day refresh tokens
- **Role-Based Access Control:** 4 roles (ADMIN, MANAGER, HR, EMPLOYEE) with granular permissions
- **Password Security:** BCrypt hashing (strength 12), minimum complexity requirements
- **API Protection:** Rate limiting (100 req/min), CORS configuration, CSRF protection
- **Session Management:** Stateless architecture, secure token storage

---

## 🏗️ Architecture

The system follows a modern three-tier architecture with clear separation of concerns:

```
┌─────────────────────────────────────────────────────────────┐
│                     Client Layer                            │
│  React SPA (Vite) → Nginx Reverse Proxy → SSL/TLS          │
└─────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────┐
│                   Application Layer                          │
│  Spring Boot REST API → Spring Security → JWT Auth          │
│  Spring Data JPA → Spring AOP (Audit) → Flyway Migrations  │
└─────────────────────────────────────────────────────────────┘
                              ↓
┌─────────────────────────────────────────────────────────────┐
│                      Data Layer                              │
│  MySQL 8.0 → Automated Backups → Read Replicas             │
└─────────────────────────────────────────────────────────────┘
```

**📐 For detailed architecture diagrams, see [ARCHITECTURE.md](ARCHITECTURE.md)**:
- System architecture diagram
- JWT authentication flow
- CI/CD pipeline workflow
- Production deployment architecture
- Data flow diagrams

---

## 🚀 Quick Start (Local Development)

**⏱️ Total setup time: ~10 minutes**

### Prerequisites Checklist

Before you begin, ensure you have these installed:

- [ ] **Java 17** or higher → [Download](https://adoptium.net/)
- [ ] **Maven 3.9+** → Verify with `mvn -version`
- [ ] **MySQL 8.0** → [Download](https://dev.mysql.com/downloads/mysql/)
- [ ] **Node.js 18+** → [Download](https://nodejs.org/)
- [ ] **Git** → [Download](https://git-scm.com/)

### Step 1: Clone & Database Setup

```bash
# Clone the repository
git clone https://github.com/ecovale/hr-system.git
cd hr-system

# Start MySQL and create database
mysql -u root -p
# Enter your MySQL root password when prompted
```

```sql
-- In MySQL shell:
CREATE DATABASE ecovale_hr;
EXIT;
```

### Step 2: Configure Backend Environment

```bash
cd backend

# Option A: Using environment variables (Recommended)
export DB_HOST=localhost
export DB_PORT=3306
export DB_NAME=ecovale_hr
export DB_USERNAME=root
export DB_PASSWORD=yourpassword
export JWT_SECRET=your-secret-key-minimum-32-characters-long

# Option B: Edit application.properties directly
# Open: src/main/resources/application.properties
# Update the database connection details
```

### Step 3: Build & Run Backend

```bash
# Install dependencies and build
mvn clean install

# Start the Spring Boot application
mvn spring-boot:run

# ✅ Backend running at: http://localhost:8080
# ✅ Swagger UI available at: http://localhost:8080/swagger-ui.html
```

**Verify backend is running:**
```bash
curl http://localhost:8080/api/v1/health
# Should return: {"status":"UP","uptime":"..."}
```

### Step 4: Configure Frontend

```bash
# Open a new terminal and navigate to frontend
cd ../  # Go to project root

# Install dependencies
npm install

# Create environment file
echo "VITE_API_BASE_URL=http://localhost:8080/api/v1" > .env.local
```

### Step 5: Run Frontend

```bash
# Start Vite development server
npm run dev

# ✅ Frontend running at: http://localhost:5173
```

### Step 6: Login & Test

1. **Open browser:** Navigate to `http://localhost:5173`
2. **Login with default admin credentials:**
   ```
   Username: admin
   Password: password123
   ```
3. **Explore the application:**
   - View employees list
   - Create a leave request
   - Check attendance
   - Generate payslips

### 🎉 Success! You're Now Running Locally

**What's Next?**
- 📖 Read [API-DOCUMENTATION.md](backend/API-DOCUMENTATION.md) to explore API endpoints
- 🧪 Try the Swagger UI at `http://localhost:8080/swagger-ui.html`
- 👥 Create test users with different roles (Manager, HR, Employee)
- 📊 Check monitoring at `http://localhost:8080/actuator/health`

### Troubleshooting Common Issues

**Issue: "Cannot connect to database"**
```bash
# Verify MySQL is running
sudo systemctl status mysql  # Linux
brew services list          # macOS

# Check credentials in application.properties match your MySQL setup
```

**Issue: "Port 8080 already in use"**
```bash
# Find and kill the process using port 8080
# Linux/macOS:
lsof -i :8080
kill -9 <PID>

# Or change the port in application.properties:
server.port=8081
```

**Issue: "Flyway migration failed"**
```bash
# Reset database (WARNING: Deletes all data!)
mysql -u root -p
DROP DATABASE ecovale_hr;
CREATE DATABASE ecovale_hr;
EXIT;

# Restart the backend
mvn spring-boot:run
```

**Issue: "npm install fails"**
```bash
# Clear npm cache and retry
npm cache clean --force
rm -rf node_modules package-lock.json
npm install
```

---

## 🌐 Deploy Your Own (5 Minutes)

Want to deploy this to the cloud? It's easier than you think!

### Backend Deployment → Railway (Free Tier)

**Why Railway?** Free $5 credit/month, auto-deploy from GitHub, MySQL included

```bash
# 1. Install Railway CLI
npm install -g @railway/cli

# 2. Login to Railway
railway login

# 3. Deploy backend
cd backend
railway init
railway up

# 4. Add MySQL database in Railway dashboard
# Railway will auto-configure DATABASE_URL

# 5. Set environment variables in Railway dashboard:
JWT_SECRET=your-256-bit-secret-key-here-minimum-32-characters
CORS_ALLOWED_ORIGINS=https://your-frontend.netlify.app
ADMIN_USERNAME=demo_admin
ADMIN_PASSWORD=Demo@2026!Secure
SPRING_PROFILES_ACTIVE=prod
```

**✅ Your backend is now live!** Note your URL: `https://your-app.railway.app`

### Frontend Deployment → Netlify (Free Tier)

**Why Netlify?** Free hosting, auto-deploy from GitHub, global CDN

```bash
# 1. Install Netlify CLI
npm install -g netlify-cli

# 2. Build your frontend
npm run build

# 3. Login to Netlify
netlify login

# 4. Deploy
netlify deploy --prod --dir=dist

# 5. Set environment variable in Netlify dashboard:
VITE_API_BASE_URL=https://your-backend.railway.app/api/v1
```

**✅ Your frontend is now live!** Note your URL: `https://your-app.netlify.app`

### Final Step: Connect Frontend & Backend

Update your Railway backend environment:
```bash
CORS_ALLOWED_ORIGINS=https://your-app.netlify.app
```

**🎉 Done! Your HR system is now publicly accessible!**

### Complete Deployment Guide

For step-by-step instructions with screenshots and troubleshooting:
- **[DEPLOYMENT-GUIDE.md](DEPLOYMENT-GUIDE.md)** - Complete deployment guide (Railway, Render, Netlify, Vercel)
- **[DEPLOYMENT-SUMMARY.md](DEPLOYMENT-SUMMARY.md)** - Quick deployment checklist
- **[DEMO-CREDENTIALS.md](DEMO-CREDENTIALS.md)** - Test accounts and API examples

---

## 📚 Documentation

### Core Documentation

| Document | Description | Location |
|----------|-------------|----------|
| **Architecture Guide** | System architecture, diagrams, tech stack | [ARCHITECTURE.md](ARCHITECTURE.md) |
| **Deployment Guide** | Deploy to Railway/Render/Netlify/Vercel | [DEPLOYMENT-GUIDE.md](DEPLOYMENT-GUIDE.md) |
| **Deployment Summary** | Quick deployment checklist | [DEPLOYMENT-SUMMARY.md](DEPLOYMENT-SUMMARY.md) |
| **Demo Credentials** | Test accounts and API examples | [DEMO-CREDENTIALS.md](DEMO-CREDENTIALS.md) |
| **API Documentation** | Complete API reference, versioning, examples | [backend/API-DOCUMENTATION.md](backend/API-DOCUMENTATION.md) |
| **API Quick Reference** | Quick start guide for API usage | [backend/API-QUICK-REFERENCE.md](backend/API-QUICK-REFERENCE.md) |
| **API Deprecation Strategy** | Deprecation policy and migration guides | [backend/API-DEPRECATION-STRATEGY.md](backend/API-DEPRECATION-STRATEGY.md) |
| **Leave Management Guide** | Leave module API and workflows | [backend/LEAVE-MANAGEMENT-GUIDE.md](backend/LEAVE-MANAGEMENT-GUIDE.md) |
| **Frontend Migration** | Frontend update guide for API v1 | [FRONTEND-MIGRATION-CHECKLIST.md](FRONTEND-MIGRATION-CHECKLIST.md) |

### Database Documentation

- **Schema Design**: [backend/db-design/](backend/db-design/)
- **Entities**: [backend/db-design/01-entities.md](backend/db-design/01-entities.md)
- **Relationships**: [backend/db-design/03-relationships.md](backend/db-design/03-relationships.md)
- **Migrations**: [backend/src/main/resources/db/migration/](backend/src/main/resources/db/migration/)

### Production Documentation

- **Deployment Guide**: [backend/production/docs/08-deployment-guide.md](backend/production/docs/08-deployment-guide.md)
- **AWS Setup**: [backend/production/README.md](backend/production/README.md)
- **Performance Testing**: [backend/performance-tests/README.md](backend/performance-tests/README.md)

---

## 🛠️ Technology Stack

### Backend (Spring Boot Ecosystem)

| Technology | Version | Purpose |
|------------|---------|---------|
| **Spring Boot** | 3.2.1 | Core application framework |
| **Java** | 17 (LTS) | Primary programming language |
| **Spring Security** | 6.2 | Authentication & authorization |
| **JWT (JJWT)** | 0.12.3 | Token-based authentication |
| **Spring Data JPA** | 6.2 | Database ORM layer |
| **MySQL** | 8.0 | Production database |
| **Flyway** | 9.22 | Database migration & versioning |
| **SpringDoc OpenAPI** | 2.3.0 | API documentation (Swagger UI) |
| **Micrometer + Prometheus** | 1.12 | Metrics & monitoring |
| **Logback** | 1.4 | Structured JSON logging |
| **JUnit 5 + Mockito** | 5.10 | Testing framework |
| **Maven** | 3.9+ | Build & dependency management |

### Frontend (Modern React Stack)

| Technology | Version | Purpose |
|------------|---------|---------|
| **React** | 18 | UI library |
| **TypeScript** | 5.2 | Type-safe JavaScript |
| **Vite** | 5.0 | Lightning-fast build tool |
| **Context API** | Built-in | Lightweight state management |
| **Fetch API** | Built-in | HTTP client |

### Infrastructure & DevOps

| Technology | Purpose |
|------------|---------|
| **Docker** | Containerization |
| **Railway / Render** | Backend hosting (free tier available) |
| **Netlify / Vercel** | Frontend hosting (free tier available) |
| **AWS RDS** | Production database (optional) |
| **CloudFlare** | CDN & DDoS protection |
| **GitHub Actions** | CI/CD pipelines |
| **Prometheus + Grafana** | Monitoring & dashboards |

---

## 🔌 API Documentation

### RESTful API with Versioning

**Modern API Design:** All endpoints follow RESTful principles with versioned paths (`/api/v1/*`), ensuring backward compatibility when introducing new features.

#### Core API Endpoints

```bash
# Authentication & Authorization
POST   /api/v1/auth/login              # Get JWT token
POST   /api/v1/auth/register           # Create new user

# Employee Management (8 RESTful endpoints)
GET    /api/v1/employees               # List all employees (paginated)
POST   /api/v1/employees               # Create new employee
GET    /api/v1/employees/{id}          # Get employee details
PUT    /api/v1/employees/{id}          # Update employee
DELETE /api/v1/employees/{id}          # Soft delete employee
GET    /api/v1/employees/search        # Search with filters
GET    /api/v1/employees/{id}/leaves   # Employee's leave history
GET    /api/v1/employees/{id}/salary   # Salary details

# Leave Management (Two-level approval workflow)
POST   /api/v1/leaves                  # Apply for leave
GET    /api/v1/leaves                  # List leaves (role-based filtering)
GET    /api/v1/leaves/{id}             # Leave details with approval history
PUT    /api/v1/leaves/{id}/manager-approve   # Manager approval (first level)
PUT    /api/v1/leaves/{id}/admin-approve     # Admin approval (second level)
PUT    /api/v1/leaves/{id}/reject      # Reject leave with reason
DELETE /api/v1/leaves/{id}             # Cancel leave request

# Attendance & Time Tracking
POST   /api/v1/attendance              # Clock in/out
GET    /api/v1/attendance              # Attendance records (date range)
GET    /api/v1/attendance/monthly      # Monthly attendance summary
PUT    /api/v1/attendance/{id}         # Update attendance record

# Payroll Processing
POST   /api/v1/payroll/run             # Generate monthly payroll
GET    /api/v1/payroll/payslips        # Employee payslips
GET    /api/v1/payroll/reports         # Financial reports

# Health & Monitoring
GET    /api/v1/health                  # System health check
GET    /api/v1/health/ready            # Kubernetes readiness probe
GET    /api/v1/health/live             # Kubernetes liveness probe
GET    /api/v1/health/info             # App version & uptime
```

### Interactive API Explorer (Swagger UI)

🔗 **Try APIs Live:** [http://localhost:8080/swagger-ui.html](http://localhost:8080/swagger-ui.html)

**Features:**
- ✅ **Try-it-out functionality** - Execute API calls directly from browser
- ✅ **JWT authentication** - Built-in token authorization
- ✅ **Request/response examples** - See sample payloads for every endpoint
- ✅ **Schema documentation** - Complete data model documentation
- ✅ **Error responses** - HTTP status codes and error messages documented

### Quick API Usage Example

**Step 1: Get JWT Token**
```bash
curl -X POST http://localhost:8080/api/v1/auth/login \
  -H "Content-Type: application/json" \
  -d '{
    "username": "demo_admin",
    "password": "Demo@2026!Secure"
  }'
```

**Response:**
```json
{
  "success": true,
  "message": "Login successful",
  "data": {
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
    "type": "Bearer",
    "expiresIn": 86400,
    "roles": ["ROLE_ADMIN", "ROLE_HR"]
  },
  "timestamp": "2026-01-26T10:30:00Z"
}
```

**Step 2: Use Token for Authenticated Requests**
```bash
# Get all employees
curl -X GET http://localhost:8080/api/v1/employees \
  -H "Authorization: Bearer <your-token-here>"

# Apply for leave
curl -X POST http://localhost:8080/api/v1/leaves \
  -H "Authorization: Bearer <your-token-here>" \
  -H "Content-Type: application/json" \
  -d '{
    "leaveTypeId": 1,
    "startDate": "2026-02-01",
    "endDate": "2026-02-03",
    "reason": "Personal work"
  }'
```

### Complete API Reference

📚 **For detailed documentation with request/response schemas, error codes, and testing scenarios:**
- **[API-DOCUMENTATION.md](backend/API-DOCUMENTATION.md)** - Complete API reference (100+ endpoints)
- **[API-QUICK-REFERENCE.md](backend/API-QUICK-REFERENCE.md)** - Quick start guide
- **[DEMO-CREDENTIALS.md](DEMO-CREDENTIALS.md)** - Test accounts with API examples

---

## 💻 Development & Testing

### 🏗️ System Architecture

**Modern Three-Tier Architecture:**
- **Presentation Layer:** React 18 with TypeScript (type-safe UI components)
- **Business Layer:** Spring Boot 3.2 REST API (domain-driven services)
- **Data Layer:** MySQL 8.0 with JPA/Hibernate (entity relationships)

**Design Patterns Implemented:**
- **MVC Pattern** - Controllers separate routing from business logic
- **Repository Pattern** - Data access abstraction with Spring Data JPA
- **DTO Pattern** - Clean separation between entities and API contracts
- **AOP (Aspect-Oriented Programming)** - Centralized audit logging
- **Builder Pattern** - Readable object construction (Employee, Leave entities)
- **Strategy Pattern** - Pluggable leave approval workflows

📐 **For detailed architecture diagrams and design decisions, see [ARCHITECTURE.md](ARCHITECTURE.md)**

---

### 📂 Project Structure

```
ecovale-hr-web-app/
├── backend/                          # Spring Boot 3.2 Backend
│   ├── src/main/java/com/ecovale/hr/
│   │   ├── config/                   # Configuration (Security, CORS, Swagger)
│   │   ├── controller/               # REST API controllers (8 endpoints)
│   │   │   ├── EmployeeController.java
│   │   │   ├── LeaveController.java
│   │   │   ├── AttendanceController.java
│   │   │   ├── PayrollController.java
│   │   │   ├── AuditController.java
│   │   │   └── HealthCheckController.java
│   │   ├── dto/                      # Data Transfer Objects (Request/Response)
│   │   ├── entity/                   # JPA Entities (15 domain models)
│   │   ├── repository/               # Spring Data JPA repositories
│   │   ├── service/                  # Business logic layer
│   │   ├── security/                 # JWT, authentication, authorization
│   │   └── util/                     # Helpers, validators, constants
│   ├── src/main/resources/
│   │   ├── db/migration/             # Flyway migrations (V1__init → V8__audit)
│   │   ├── application.properties    # Main configuration
│   │   └── application-prod.properties  # Production overrides
│   ├── performance-tests/            # k6 load tests (1000+ concurrent users)
│   └── pom.xml                       # Maven dependencies (40+ libraries)
│
├── src/                              # React 18 Frontend
│   ├── components/                   # Reusable UI components
│   │   ├── layout/                   # MainLayout, Navbar, Sidebar
│   │   └── ui/                       # Button, Input, Toast, ErrorBoundary
│   ├── pages/                        # Screen implementations (15 pages)
│   │   ├── LoginPage.tsx
│   │   ├── DashboardPage.tsx
│   │   ├── EmployeesPage.tsx
│   │   ├── NewEmployeePage.tsx
│   │   └── AttendanceRegisterPage.tsx
│   ├── contexts/                     # React Context API (AppContext)
│   ├── services/                     # API service layer (storageService)
│   ├── utils/                        # Helpers, constants, formatters
│   └── types/                        # TypeScript type definitions
│
├── ARCHITECTURE.md                   # 📐 Architecture documentation (17 KB)
├── DEPLOYMENT-GUIDE.md               # 🚀 Cloud deployment guide (24 KB)
├── DEMO-CREDENTIALS.md               # 🔑 Test accounts & scenarios (18 KB)
└── README.md                         # 📖 This file
```

---

### 🧪 Running Tests

**Backend Unit & Integration Tests:**
```bash
cd backend

# Run all tests
mvn test

# Run tests with coverage report
mvn clean test jacoco:report

# View coverage report
# Open: target/site/jacoco/index.html
# Target: >80% code coverage

# Run integration tests only
mvn verify -P integration-tests

# Skip tests during build (not recommended)
mvn package -DskipTests
```

**Performance & Load Testing:**
```bash
cd backend/performance-tests

# Load test: 1000 concurrent users, 5 minutes
k6 run load-test-complete.js

# Stress test: Find breaking point
k6 run stress-test.js

# Spike test: Sudden traffic surge
k6 run spike-test.js

# Expected results:
# - 95th percentile response time: <500ms
# - Error rate: <1%
# - Throughput: >1000 req/sec
```

---

### ✅ Code Quality & Security

**Static Code Analysis:**
```bash
# SonarQube code quality scan
mvn sonar:sonar \
  -Dsonar.projectKey=ecovale-hr \
  -Dsonar.host.url=http://localhost:9000 \
  -Dsonar.login=<your-token>

# Target metrics:
# - Code coverage: >80%
# - Technical debt: <5%
# - Security hotspots: 0
# - Code smells: <50
```

**Security Vulnerability Scanning:**
```bash
# OWASP dependency check
mvn dependency-check:check

# View report: target/dependency-check-report.html
```

**Linting & Formatting:**
```bash
# Frontend linting (if configured)
npm run lint

# Backend formatting (Maven Formatter Plugin)
mvn formatter:format
```

---

### 🗄️ Database Migrations

**Flyway Migration Commands:**
```bash
cd backend

# Check migration status
mvn flyway:info

# Apply pending migrations
mvn flyway:migrate

# Validate checksums
mvn flyway:validate

# Rollback last migration (if supported)
mvn flyway:undo

# ⚠️ Clean database (DESTRUCTIVE - dev only)
mvn flyway:clean
```

**Migration Files:**
- `V1__init_database.sql` - Initial schema (users, roles, permissions)
- `V2__employee_management.sql` - Employee tables
- `V3__leave_management.sql` - Leave tables with approval workflow
- `V4__attendance_tracking.sql` - Attendance tables
- `V5__payroll_system.sql` - Payroll, loans, advances
- `V6__audit_logging.sql` - Audit trail tables
- `V7__additional_features.sql` - Documents, settings
- `V8__audit_indexes.sql` - Performance indexes

---

### 🐳 Local Development with Docker

**Quick Start with Docker Compose:**
```bash
# Start all services (backend + MySQL + monitoring)
docker-compose up -d

# Services running:
✅ Backend API:     http://localhost:8080
✅ MySQL Database:  localhost:3306
✅ Prometheus:      http://localhost:9090
✅ Grafana:         http://localhost:3000

# Check logs
docker-compose logs -f backend

# Stop services
docker-compose down

# Clean volumes (fresh database)
docker-compose down -v
```

**Build Docker Image:**
```bash
cd backend

# Build backend image
docker build -t ecovale-hr:latest .

# Run standalone
docker run -p 8080:8080 \
  -e SPRING_DATASOURCE_URL=jdbc:mysql://host.docker.internal:3306/ecovale_hr \
  -e JWT_SECRET=your-secret-key \
  ecovale-hr:latest
```

---

## 🚀 Production Deployment

### 🐳 Docker Deployment (Recommended)

**Quick Production Setup:**
```bash
# 1. Build backend Docker image
cd backend
docker build -t ecovale-hr:latest .

# 2. Start all production services
docker-compose -f docker-compose.prod.yml up -d

# Services running:
✅ Backend API:     https://your-domain.com
✅ MySQL Database:  Internal network
✅ Prometheus:      Metrics collection
✅ Grafana:         Monitoring dashboards
✅ Nginx:          Reverse proxy + SSL
```

**Docker Compose Production Stack:**
```yaml
version: '3.8'
services:
  backend:
    image: ecovale-hr:latest
    environment:
      - SPRING_PROFILES_ACTIVE=prod
      - DATABASE_URL=${DATABASE_URL}
      - JWT_SECRET=${JWT_SECRET}
    ports:
      - "8080:8080"
  
  mysql:
    image: mysql:8.0
    environment:
      - MYSQL_DATABASE=ecovale_hr
      - MYSQL_ROOT_PASSWORD=${DB_PASSWORD}
    volumes:
      - mysql_data:/var/lib/mysql
  
  prometheus:
    image: prom/prometheus
    ports:
      - "9090:9090"
  
  grafana:
    image: grafana/grafana
    ports:
      - "3000:3000"
```

---

### ☁️ Cloud Deployment (AWS)

**Architecture:** ECS Fargate + RDS MySQL + CloudWatch

**Step 1: Setup RDS MySQL Database**
```bash
# Create production database
aws rds create-db-instance \
  --db-instance-identifier ecovale-hr-prod-db \
  --db-instance-class db.t3.medium \
  --engine mysql \
  --engine-version 8.0 \
  --master-username admin \
  --master-user-password <secure-password-here> \
  --allocated-storage 50 \
  --multi-az \
  --backup-retention-period 7 \
  --publicly-accessible false \
  --vpc-security-group-ids sg-xxxxx \
  --tags Key=Environment,Value=Production Key=Project,Value=EcovaleHR
```

**Step 2: Push Docker Image to ECR**
```bash
# Authenticate Docker to ECR
aws ecr get-login-password --region us-east-1 | \
  docker login --username AWS --password-stdin <account-id>.dkr.ecr.us-east-1.amazonaws.com

# Tag and push image
docker tag ecovale-hr:latest <account-id>.dkr.ecr.us-east-1.amazonaws.com/ecovale-hr:latest
docker push <account-id>.dkr.ecr.us-east-1.amazonaws.com/ecovale-hr:latest
```

**Step 3: Deploy to ECS Fargate**
```bash
# Update ECS service with new image
aws ecs update-service \
  --cluster ecovale-hr-cluster \
  --service ecovale-hr-service \
  --force-new-deployment \
  --desired-count 2

# Check deployment status
aws ecs describe-services \
  --cluster ecovale-hr-cluster \
  --services ecovale-hr-service
```

**Step 4: Configure Secrets (AWS Secrets Manager)**
```bash
# Store database credentials
aws secretsmanager create-secret \
  --name ecovale-hr/db-credentials \
  --secret-string '{
    "username": "admin",
    "password": "<db-password>",
    "host": "ecovale-hr-prod-db.xxxxx.rds.amazonaws.com",
    "port": 3306,
    "database": "ecovale_hr"
  }'

# Store JWT secret (256-bit key)
aws secretsmanager create-secret \
  --name ecovale-hr/jwt-secret \
  --secret-string '{"secret": "<32-character-random-key>"}'

# ECS task will fetch secrets at runtime
```

**Step 5: Setup Application Load Balancer**
```bash
# ALB automatically created by ECS service
# Configure health checks:
# - Path: /api/v1/health/live
# - Interval: 30 seconds
# - Timeout: 5 seconds
# - Healthy threshold: 2
# - Unhealthy threshold: 3
```

---

### 📊 Monitoring & Observability

**CloudWatch Alarms:**
```bash
# High CPU usage alert
aws cloudwatch put-metric-alarm \
  --alarm-name ecovale-hr-high-cpu \
  --metric-name CPUUtilization \
  --namespace AWS/ECS \
  --statistic Average \
  --period 300 \
  --threshold 80 \
  --comparison-operator GreaterThanThreshold \
  --alarm-actions <sns-topic-arn>

# High response time alert
aws cloudwatch put-metric-alarm \
  --alarm-name ecovale-hr-high-latency \
  --metric-name TargetResponseTime \
  --namespace AWS/ApplicationELB \
  --statistic Average \
  --period 60 \
  --threshold 1 \
  --comparison-operator GreaterThanThreshold
```

**Prometheus Metrics Exported:**
- `http_server_requests_seconds` - Request latency by endpoint
- `jvm_memory_used_bytes` - JVM memory usage
- `hikaricp_connections_active` - Database connection pool
- `leave_approval_duration_seconds` - Business metric

**Grafana Dashboards Available:**
- JVM Metrics (heap, GC, threads)
- API Performance (latency, throughput, errors)
- Database Metrics (queries, connections)
- Business Metrics (leaves, attendance, payroll)

---

### 🔐 Production Checklist

Before deploying to production, ensure:

**Security:**
- ✅ Change all default passwords
- ✅ Generate strong JWT secret (256-bit minimum)
- ✅ Configure CORS to allow only your frontend domain
- ✅ Enable HTTPS/SSL certificates
- ✅ Setup rate limiting (10 req/sec per IP)
- ✅ Enable SQL injection protection (JPA parameterized queries)
- ✅ Configure firewall rules (allow only 443, 80, SSH)
- ✅ Rotate database credentials quarterly

**Database:**
- ✅ Enable automated backups (7-day retention minimum)
- ✅ Setup read replicas for scaling
- ✅ Configure slow query logging
- ✅ Apply Flyway migrations before deployment
- ✅ Enable point-in-time recovery

**Monitoring:**
- ✅ Setup CloudWatch logs aggregation
- ✅ Configure error rate alarms (>5% = critical)
- ✅ Setup latency alarms (>1s = warning)
- ✅ Enable distributed tracing (AWS X-Ray)
- ✅ Configure uptime monitoring (Pingdom/UptimeRobot)

**Performance:**
- ✅ Enable database connection pooling (HikariCP configured)
- ✅ Configure caching (Redis recommended for sessions)
- ✅ Setup CDN for frontend assets (CloudFront)
- ✅ Enable gzip compression
- ✅ Run load tests before launch (k6 tests provided)

**📖 Complete Deployment Guide:** See [DEPLOYMENT-GUIDE.md](DEPLOYMENT-GUIDE.md) for Railway, Render, Netlify, Vercel deployment steps with screenshots.

---

## 🤝 Contributing

Contributions are welcome! This is a portfolio/learning project, but improvements are appreciated.

**How to Contribute:**
1. Fork the repository
2. Create a feature branch: `git checkout -b feature/YourFeature`
3. Make your changes with clear commit messages
4. Write/update tests for new functionality
5. Update documentation as needed
6. Push and create a Pull Request

**Coding Standards:**
- Follow existing code style (Java conventions, React best practices)
- Write unit tests (aim for >80% coverage)
- Update relevant documentation
- Add descriptive commit messages

---

## 📞 Support & Contact

### 📚 Documentation Resources
- **[ARCHITECTURE.md](ARCHITECTURE.md)** - System architecture & design patterns
- **[API-DOCUMENTATION.md](backend/API-DOCUMENTATION.md)** - Complete API reference  
- **[DEPLOYMENT-GUIDE.md](DEPLOYMENT-GUIDE.md)** - Cloud deployment guide
- **[DEMO-CREDENTIALS.md](DEMO-CREDENTIALS.md)** - Test accounts

### 💬 Get Help
- **GitHub Issues:** Report bugs or request features
- **Email:** support@ecovale.com
- **Documentation:** Check the docs folder for detailed guides

### 🔗 Useful Links
- **Swagger UI:** `http://localhost:8080/swagger-ui.html`
- **Grafana Dashboard:** `http://localhost:3000`
- **Prometheus Metrics:** `http://localhost:9090`

---

## 📄 License

**Proprietary License** - © 2026 Ecovale

This is a portfolio/demonstration project. Contact the author for licensing inquiries.

---

## 🎉 Acknowledgments

**Built With Modern Technologies:**
- [Spring Boot](https://spring.io/projects/spring-boot) - Backend framework
- [React](https://reactjs.org/) - Frontend library
- [MySQL](https://www.mysql.com/) - Database
- [Docker](https://www.docker.com/) - Containerization
- [Prometheus](https://prometheus.io/) & [Grafana](https://grafana.com/) - Monitoring

**Special Thanks:**
- Spring Boot community for excellent documentation
- React team for the powerful UI library
- Open source contributors who make projects like this possible

---

<div align="center">
  
### 🌟 If you find this project helpful, please star it on GitHub! 🌟

  <p>Made with ❤️ and ☕ by the Ecovale Team</p>
  
  <p>
    <a href="ARCHITECTURE.md">📐 Architecture</a> •
    <a href="backend/API-DOCUMENTATION.md">📚 API Docs</a> •
    <a href="DEPLOYMENT-GUIDE.md">🚀 Deploy Guide</a> •
    <a href="DEMO-CREDENTIALS.md">🔑 Demo Access</a>
  </p>
  
  <p>
    <strong>Ready to deploy?</strong> Follow the <a href="DEPLOYMENT-GUIDE.md">5-minute deployment guide</a>
  </p>
  
</div>

---

**Project Status:** ✅ Production-Ready | 🚀 Actively Maintained | 📖 Well-Documented

**Last Updated:** January 26, 2026 | **Version:** 1.0.0

# Ecovalepvtltd
