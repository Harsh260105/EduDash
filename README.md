# 🏫 EduDash - School Management System

A comprehensive full-stack school management application built with Next.js, PostgreSQL, Prisma ORM, and Docker.

## 🚀 Features

### Role-Based Dashboards

- **Admin** - Complete CRUD operations for teachers, students, parents, classes, subjects, and more
- **Teacher** - Access to personal lessons, exams, assignments with protected routes
- **Student** - View class schedules, exam results, and personal assignments
- **Parent** - Monitor child's schedule, grades, and attendance

### Core Functionality

- 🔐 **Authentication & Authorization** - Role-based access control with middleware protection
- 📊 **Dashboard Analytics** - Interactive charts and data visualization
- 📅 **Calendar Integration** - Schedule management and event tracking
- 🔍 **Search & Pagination** - Efficient data browsing
- 📱 **Responsive Design** - Mobile-friendly interface

## 🛠️ Tech Stack

### Frontend
- **Next.js** - React framework with server-side rendering
- **React Hook Form** - Form handling and validation
- **Tailwind CSS** - Utility-first CSS framework
- **Chart.js** - Data visualization

### Backend
- **PostgreSQL** - Primary database
- **Prisma ORM** - Database toolkit and query builder
- **Next.js API Routes** - Server-side API endpoints

### DevOps
- **Docker** - Containerization
- **Hostinger VPS** - Deployment platform

## 📋 Prerequisites

- Node.js 18+ 
- Docker & Docker Compose
- PostgreSQL (or use Docker container)

## 🚀 Quick Start

### 1. Clone Repository
```bash
git clone <repository-url>
cd EduDash
```

### 2. Environment Setup
```bash
cp .env.example .env.local
```

Configure your environment variables:
```env
DATABASE_URL="postgresql://username:password@localhost:5432/edudash"
NEXTAUTH_SECRET="your-secret-key"
NEXTAUTH_URL="http://localhost:3000"
```

### 3. Database Setup with Docker
```bash
# Start PostgreSQL container
docker-compose up -d postgres

# Generate Prisma client
npx prisma generate

# Run migrations
npx prisma migrate dev

# Seed database (optional)
npx prisma db seed
```

### 4. Install Dependencies & Run
```bash
npm install
npm run dev
```

Visit `http://localhost:3000` to access the application.

## 🗄️ Database Schema

### Core Entities
- **Users** - Admin, Teacher, Student, Parent roles
- **Academic** - Class, Subject, Lesson, Assignment, Exam
- **Results** - Grades, Attendance, Performance tracking
- **Communication** - Events, Announcements

### Key Relationships
- Parents → Children (Students)
- Teachers → Subjects → Classes
- Students → Classes → Lessons → Assignments/Exams

## 🔧 Development

### Prisma Commands
```bash
# View database in Prisma Studio
npx prisma studio

# Reset database
npx prisma migrate reset

# Deploy migrations
npx prisma migrate deploy
```

### Project Structure
```
├── app/
│   ├── (dashboard)/          # Protected dashboard routes
│   ├── api/                  # API endpoints
│   └── auth/                 # Authentication pages
├── components/               # Reusable UI components
├── lib/                      # Utilities and configurations
├── prisma/                   # Database schema and migrations
└── public/                   # Static assets
```

## 🚀 Deployment

### Docker Deployment
```bash
# Build and run with Docker Compose
docker-compose up --build

# Production deployment
docker-compose -f docker-compose.prod.yml up -d
```

### Hostinger VPS Setup
1. Configure VPS with Docker
2. Set environment variables
3. Deploy using Docker containers
4. Configure reverse proxy (Nginx)

## 🔐 Authentication Flow

1. **Login** - Role-based authentication
2. **Middleware** - Route protection and redirection
3. **Authorization** - Feature access based on user role
4. **Session Management** - Secure session handling

## 📊 Key Components

### Reusable Components
- **Calendar** - Event and schedule management
- **Charts** - Performance analytics
- **Tables** - Data display with pagination
- **Forms** - CRUD operations with validation

### Server Actions
- Data mutations separated from components
- Server-side validation and processing
- Optimistic updates for better UX

## 🧪 Best Practices Implemented

- **Prisma Singleton Pattern** - Development-safe client creation
- **Nested Relationships** - Efficient data fetching
- **Server Components** - Optimal data loading
- **Middleware Protection** - Secure route access
- **Form Validation** - Client and server-side validation

## 📝 API Endpoints

```
GET    /api/admin/users       # Get all users
POST   /api/admin/users       # Create user
PUT    /api/admin/users/:id   # Update user
DELETE /api/admin/users/:id   # Delete user

GET    /api/teacher/lessons   # Get teacher lessons
GET    /api/student/schedule  # Get student schedule
GET    /api/parent/children   # Get children data
```

## 🤝 Contributing

1. Fork the repository
2. Create feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Built following modern Next.js best practices
- Database design optimized for educational institutions
- UI/UX designed for multi-role accessibility

---

**Live Demo**:   
**Documentation**:  
**Support**:
