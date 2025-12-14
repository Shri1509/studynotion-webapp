# 📚 StudyNotion – EdTech Platform

**A Comprehensive Online Learning & Course Management System**

![JavaScript](https://img.shields.io/badge/javascript-ES6+-yellow)
![React](https://img.shields.io/badge/react-18-blue)
![Node.js](https://img.shields.io/badge/node.js-18+-green)
![MongoDB](https://img.shields.io/badge/mongodb-latest-green)
![License](https://img.shields.io/badge/license-MIT-blue)

[Live Demo](https://studynotion-webapp-frontend.vercel.app) · [Report Bug](https://github.com/Shri1509/studynotion-webapp/issues) · [Request Feature](https://github.com/Shri1509/studynotion-webapp/issues)

---

## 📘 High-Level Overview

StudyNotion is a full-stack EdTech platform designed to connect instructors and students through a seamless online learning experience. The platform enables users to create, manage, and enroll in courses with features like live classes, video content, and student progress tracking.

**Key Features:**

- **Multi-role system:** Students, Instructors, and Admins
- **Course management:** Create, update, delete, and organize courses
- **Live classes:** Host and attend live learning sessions
- **JWT Authentication:** Secure user authentication and authorization
- **Email notifications:** OTP-based account verification and course updates via Nodemailer
- **Responsive UI:** Built with React for seamless experience across devices
- **RESTful API:** Node.js backend with comprehensive API endpoints

---

## 🧱 System Architecture

```
[Frontend - React/Vite]
├── User Authentication
├── Dashboard (Student/Instructor)
├── Course Catalog & Enrollment
├── Course Builder
├── Live Classes Interface
└── Profile Management
        │
        ▼
[API Gateway]
        │
        ▼
[Backend - Node.js/Express]
├── Authentication Routes
├── User Management
├── Course Management
├── Enrollment Management
├── Email Services (Nodemailer)
└── JWT Token Handling
        │
        ▼
[Database - MongoDB]
├── Users Collection
├── Courses Collection
├── Enrollments Collection
├── Live Classes Collection
└── Course Content
```

---

## 🧰 Technology Stack

| Layer | Technology |
|-------|-----------|
| **Frontend** | React 18, Vite, Tailwind CSS |
| **Backend** | Node.js, Express.js |
| **Database** | MongoDB |
| **Authentication** | JWT (JSON Web Tokens) |
| **Email Service** | Nodemailer |
| **Deployment** | Vercel (Frontend), Cloud Services (Backend) |
| **Styling** | Tailwind CSS, CSS Modules |

---

## 📁 Project Folder Structure

```
studynotion-webapp/
├── src/                           # Frontend source code
│   ├── components/                # React components
│   │   ├── Auth/                  # Authentication components
│   │   ├── Dashboard/             # Dashboard pages
│   │   ├── Courses/               # Course-related components
│   │   ├── LiveClasses/           # Live class interface
│   │   └── Common/                # Reusable components
│   ├── pages/                     # Page components
│   │   ├── Login.jsx
│   │   ├── Signup.jsx
│   │   ├── Dashboard.jsx
│   │   ├── CourseDetails.jsx
│   │   └── ...
│   ├── services/                  # API service calls
│   │   ├── api.js                 # Axios configuration
│   │   ├── authService.js
│   │   ├── courseService.js
│   │   └── liveClassService.js
│   ├── context/                   # React Context for state management
│   │   ├── AuthContext.js
│   │   ├── CourseContext.js
│   │   └── ...
│   ├── styles/                    # Global styles
│   │   ├── index.css
│   │   └── tailwind.css
│   ├── App.jsx
│   └── main.jsx
│
├── server/                        # Backend source code
│   ├── routes/                    # Express routes
│   │   ├── auth.js                # Authentication routes
│   │   ├── courses.js             # Course management routes
│   │   ├── enrollments.js         # Enrollment routes
│   │   ├── users.js               # User management routes
│   │   └── admin.js               # Admin routes
│   ├── controllers/               # Route handlers
│   │   ├── authController.js
│   │   ├── courseController.js
│   │   ├── enrollmentController.js
│   │   └── userController.js
│   ├── models/                    # MongoDB schemas
│   │   ├── User.js
│   │   ├── Course.js
│   │   ├── Enrollment.js
│   │   └── LiveClass.js
│   ├── middleware/                # Express middleware
│   │   ├── authMiddleware.js      # JWT verification
│   │   ├── roleMiddleware.js      # Role-based access control
│   │   └── errorHandler.js
│   ├── services/                  # Business logic
│   │   ├── emailService.js        # Nodemailer configuration
│   │   ├── courseService.js
│   │   └── enrollmentService.js
│   ├── config/                    # Configuration files
│   │   ├── database.js
│   │   ├── jwt.js
│   │   └── email.js
│   ├── utils/                     # Utility functions
│   │   ├── validators.js
│   │   ├── helpers.js
│   │   └── errorHandler.js
│   ├── server.js                  # Entry point
│   └── requirements.txt           # Node dependencies
│
├── public/                        # Static assets
│   ├── favicon.ico
│   ├── images/
│   └── ...
│
├── .env.example                   # Environment variables template
├── .gitignore
├── package.json                   # Frontend dependencies
├── tailwind.config.js             # Tailwind CSS configuration
├── vite.config.js                 # Vite configuration
└── README.md
```

---

## 🔐 User Roles & Permissions

### 1. **Student**
- Browse and enroll in courses
- Access course content and materials
- Attend live classes
- Track learning progress
- Submit assignments
- View course certificates

### 2. **Instructor**
- Create and manage courses
- Upload course materials and videos
- Host live classes
- Track student progress
- Add course descriptions and learning outcomes
- Manage enrollments

### 3. **Admin**
- Approve courses and instructors
- Manage user accounts
- View platform analytics
- Handle system-wide configurations
- Monitor course content compliance

---

## 🚀 Getting Started

### Prerequisites

- **Node.js** (v18 or higher)
- **npm** or **yarn**
- **MongoDB** (local or Atlas cluster)
- **Git**

### Installation

#### 1. Clone the Repository

```bash
git clone https://github.com/Shri1509/studynotion-webapp.git
cd studynotion-webapp
```

#### 2. Setup Backend

```bash
# Install backend dependencies
cd server
npm install

# Create .env file in server directory
cp .env.example .env

# Configure environment variables
# DATABASE_URL=your_mongodb_connection_string
# JWT_SECRET=your_jwt_secret_key
# SMTP_EMAIL=your_email@gmail.com
# SMTP_PASSWORD=your_app_password
# NODE_ENV=development

# Start backend server
npm run dev
# Server runs on http://localhost:5000
```

#### 3. Setup Frontend

```bash
# Install frontend dependencies
npm install

# Create .env file in root directory
cp .env.example .env

# Configure environment variables
# VITE_API_URL=http://localhost:5000/api

# Start development server
npm run dev
# Frontend runs on http://localhost:5173
```

---

## 📚 Core Features

### Authentication & Authorization

- **User Registration & Login:** Email-based signup with OTP verification
- **JWT Tokens:** Secure token-based authentication
- **Password Reset:** Secure password recovery via email
- **Role-Based Access Control (RBAC):** Different permissions for each user type

**Key Endpoints:**

```javascript
POST   /api/auth/signup          // Register new user
POST   /api/auth/login           // Login user
POST   /api/auth/verify-otp      // Verify OTP
POST   /api/auth/forgot-password // Request password reset
POST   /api/auth/reset-password  // Reset password
```

### Course Management

- **Create Courses:** Instructors can create and structure courses
- **Upload Content:** Support for video, documents, and rich text
- **Course Sections:** Organize content into modules and lessons
- **Publish/Unpublish:** Control course visibility

**Key Endpoints:**

```javascript
GET    /api/courses              // Get all courses
GET    /api/courses/:id          // Get course details
POST   /api/courses              // Create new course (Instructor)
PUT    /api/courses/:id          // Update course (Instructor)
DELETE /api/courses/:id          // Delete course (Instructor)
GET    /api/courses/search?q=    // Search courses
```

### Student Enrollment

- **Browse Courses:** Explore course catalog with filters
- **Enroll:** Join courses to gain access
- **Track Progress:** Monitor completion and learning progress
- **Certificate:** Earn certificates upon course completion

**Key Endpoints:**

```javascript
POST   /api/enrollments          // Enroll in course
GET    /api/enrollments/my-courses // Get enrolled courses
GET    /api/enrollments/:courseId/progress // Track progress
DELETE /api/enrollments/:id      // Unenroll from course
```

### Live Classes

- **Schedule Classes:** Instructors schedule live sessions
- **Real-time Interaction:** Join live sessions with video/audio
- **Recording:** Classes can be recorded for later viewing
- **Q&A:** Students can ask questions during classes

**Key Endpoints:**

```javascript
POST   /api/live-classes         // Schedule live class
GET    /api/live-classes         // Get upcoming classes
POST   /api/live-classes/:id/join // Join live session
GET    /api/live-classes/:id/recordings // Get recordings
```

### Email Notifications

Nodemailer integration for:
- **Account verification:** OTP for email confirmation
- **Course updates:** Notify students of new course content
- **Assignment alerts:** Remind students of deadlines
- **Enrollment confirmations:** Welcome emails

**Email Templates:**

```javascript
// OTP Verification Email
// Course Enrollment Confirmation
// Assignment Deadline Reminder
// Course Update Notification
// Password Reset Link
```

---

## 🛠️ API Documentation

### Authentication Endpoints

#### Register User
```http
POST /api/auth/signup
Content-Type: application/json

{
  "firstName": "John",
  "lastName": "Doe",
  "email": "john@example.com",
  "password": "securePassword123",
  "accountType": "student"
}
```

**Response:**
```json
{
  "success": true,
  "message": "User registered successfully. Check your email for OTP.",
  "user": {
    "id": "user_id",
    "email": "john@example.com",
    "accountType": "student"
  }
}
```

#### Login User
```http
POST /api/auth/login
Content-Type: application/json

{
  "email": "john@example.com",
  "password": "securePassword123"
}
```

**Response:**
```json
{
  "success": true,
  "message": "Login successful",
  "token": "jwt_token",
  "user": {
    "id": "user_id",
    "email": "john@example.com",
    "accountType": "student"
  }
}
```

### Course Endpoints

#### Get All Courses
```http
GET /api/courses?category=web-development&search=React
Authorization: Bearer jwt_token
```

**Response:**
```json
{
  "success": true,
  "data": [
    {
      "id": "course_id",
      "title": "React Mastery",
      "description": "Learn React from basics to advanced",
      "instructor": "instructor_name",
      "price": 4999,
      "rating": 4.8,
      "enrollments": 1250,
      "category": "web-development",
      "thumbnail": "image_url"
    }
  ],
  "totalCount": 45
}
```

#### Create Course (Instructor)
```http
POST /api/courses
Authorization: Bearer jwt_token
Content-Type: application/json

{
  "title": "Advanced Node.js",
  "description": "Master backend development",
  "category": "backend",
  "price": 3999,
  "thumbnail": "image_url",
  "courseContent": [
    {
      "sectionName": "Basics",
      "subsection": [
        {
          "title": "Introduction",
          "videoUrl": "video_url"
        }
      ]
    }
  ]
}
```

---

## 📊 Database Schema

### User Model

```javascript
{
  _id: ObjectId,
  firstName: String,
  lastName: String,
  email: String (unique),
  password: String (hashed),
  accountType: String (student/instructor/admin),
  profilePicture: String (URL),
  phoneNumber: String,
  verified: Boolean,
  otp: String,
  otpExpiry: Date,
  courses: [ObjectId], // For instructors
  enrolledCourses: [ObjectId], // For students
  createdAt: Date,
  updatedAt: Date
}
```

### Course Model

```javascript
{
  _id: ObjectId,
  title: String,
  description: String,
  instructor: ObjectId (User reference),
  category: String,
  price: Number,
  rating: Number,
  ratingCount: Number,
  thumbnail: String (URL),
  courseContent: [
    {
      sectionName: String,
      subsection: [
        {
          title: String,
          videoUrl: String,
          duration: Number,
          resources: [String]
        }
      ]
    }
  ],
  enrollments: Number,
  status: String (draft/published),
  createdAt: Date,
  updatedAt: Date
}
```

### Enrollment Model

```javascript
{
  _id: ObjectId,
  student: ObjectId (User reference),
  course: ObjectId (Course reference),
  enrollmentDate: Date,
  progress: Number (0-100),
  completedSections: [ObjectId],
  lastAccessedAt: Date,
  certificateEarned: Boolean,
  certificateDate: Date
}
```

---

## 🧪 Testing & Validation

### Input Validation

- Email format validation
- Password strength requirements
- Course data validation
- Enrollment status checks

### Error Handling

- Comprehensive error messages
- HTTP status code implementation
- Database error handling
- Authentication failure responses

---

## 🔐 Security Features

- **JWT Authentication:** Secure token-based auth with expiration
- **Password Hashing:** bcrypt for secure password storage
- **OTP Verification:** Two-factor verification for sensitive operations
- **CORS Configuration:** Restricted cross-origin requests
- **Rate Limiting:** Prevent brute force attacks
- **Input Sanitization:** XSS and injection attack prevention
- **HTTPS:** Secure data transmission in production

---

## 📈 Performance Optimization

- **Database Indexing:** Indexed frequently queried fields
- **Caching:** Implement caching for course data
- **Pagination:** Large dataset pagination for courses
- **Lazy Loading:** Frontend lazy load components
- **Image Optimization:** Compressed thumbnails and course images
- **CDN:** Static assets served via CDN

---

## 🚀 Deployment

### Frontend Deployment (Vercel)

```bash
# Deploy frontend
npm run build
vercel deploy --prod
```

**Environment Variables (Vercel):**
```
VITE_API_URL=https://api.studynotion.com
```

### Backend Deployment (Cloud Services)

**Heroku / Railway / Render:**

```bash
# Install dependencies
npm install

# Set environment variables
# DATABASE_URL
# JWT_SECRET
# SMTP_EMAIL
# SMTP_PASSWORD
# FRONTEND_URL

# Start server
npm start
```

---

## 🐛 Troubleshooting

### Common Issues

**Issue:** Backend connection fails
```
Solution: Check DATABASE_URL in .env and ensure MongoDB is running
```

**Issue:** Emails not sending
```
Solution: Verify SMTP credentials and enable "Less Secure App Access" for Gmail
```

**Issue:** CORS errors
```
Solution: Check FRONTEND_URL in backend .env matches frontend URL
```

---

## 📚 Additional Resources

- [Express.js Documentation](https://expressjs.com/)
- [React Documentation](https://react.dev/)
- [MongoDB Documentation](https://docs.mongodb.com/)
- [JWT Guide](https://jwt.io/)
- [Nodemailer Documentation](https://nodemailer.com/)

---

## 🤝 Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit changes (`git commit -m 'Add amazing feature'`)
4. Push to branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

---

## 👨‍💻 Author

**Shri1509** - [GitHub Profile](https://github.com/Shri1509)

---

## 📞 Support

For support, email your query or open an issue on [GitHub Issues](https://github.com/Shri1509/studynotion-webapp/issues).

---

## 🙏 Acknowledgments

- Inspired by modern EdTech platforms
- Thanks to the open-source community
- React, Node.js, and MongoDB communities

---

**Made with ❤️ by Shri1509**
