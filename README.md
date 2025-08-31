# 📚 University Library Management System

A modern web application for managing university library resources with user authentication, book management, and admin dashboard.

## 🚀 Features

- **User Authentication** - Sign up/Sign in with university ID verification
- **Book Catalog** - Browse and search through available books
- **Book Borrowing** - Request and manage book borrowals
- **Admin Dashboard** - Manage books, users, and library operations
- **File Upload** - Upload university ID cards and book covers
- **Rate Limiting** - Prevent abuse with Redis-based rate limiting
- **Email Notifications** - Automated email system for library updates

## 🛠️ Tech Stack

- **Frontend:** Next.js 15, React 19, TypeScript, Tailwind CSS
- **Backend:** Next.js API routes, NextAuth
- **Database:** PostgreSQL (Neon), Drizzle ORM
- **File Storage:** ImageKit
- **Cache:** Upstash Redis
- **Email:** Resend
- **Workflow:** Upstash QStash

## 🏃‍♂️ Quick Start

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd library
   ```

2. **Install dependencies**
   ```bash
   npm install --legacy-peer-deps
   ```

3. **Setup environment variables**
   ```bash
   cp .env.example .env.local
   # Add your credentials (see Environment Variables section)
   ```

4. **Setup database**
   ```bash
   npm run db:migrate
   npm run seed
   ```

5. **Start development server**
   ```bash
   npm run dev
   ```

6. **Visit the application**
   - Main App: http://localhost:3000
   - Admin Panel: http://localhost:3000/admin

## 🔑 Environment Variables

Create a `.env.local` file with:

```bash
# API Endpoints
NEXT_PUBLIC_API_ENDPOINT=http://localhost:3000/api
NEXT_PUBLIC_PROD_API_ENDPOINT=https://your-domain.com/api

# Authentication
AUTH_SECRET=your-secret-key

# Database (Neon PostgreSQL)
DATABASE_URL=postgresql://user:pass@host/db

# ImageKit (File Storage)
NEXT_PUBLIC_IMAGEKIT_PUBLIC_KEY=your-public-key
NEXT_PUBLIC_IMAGEKIT_URL_ENDPOINT=https://ik.imagekit.io/your-id
IMAGEKIT_PRIVATE_KEY=your-private-key

# Upstash Redis
UPSTASH_REDIS_URL=your-redis-url
UPSTASH_REDIS_TOKEN=your-redis-token

# Upstash QStash (Workflows)
QSTASH_URL=https://qstash.upstash.io
QSTASH_TOKEN=your-qstash-token

# Resend (Email)
RESEND_TOKEN=your-resend-token
```

## 📱 Usage

### For Students:
1. **Sign Up** - Create account with university ID upload
2. **Browse Books** - Search and explore the library catalog
3. **Borrow Books** - Request books for borrowing
4. **Manage Profile** - View borrowing history and profile

### For Admins:
1. **Access Admin Panel** - `/admin`
2. **Manage Books** - Add, edit, delete books
3. **User Management** - View and manage user accounts
4. **Library Operations** - Handle borrowing requests

## 🎯 Key Pages

- `/` - Home page with featured books
- `/sign-up` - Student registration
- `/sign-in` - User login
- `/books/[id]` - Individual book details
- `/my-profile` - User profile and history
- `/admin` - Admin dashboard
- `/admin/books` - Book management
- `/admin/books/new` - Add new books

## 🔧 Development Commands

```bash
npm run dev          # Start development server
npm run build        # Build for production
npm run start        # Start production server
npm run lint         # Run ESLint
npm run db:generate  # Generate database migrations
npm run db:migrate   # Run database migrations
npm run db:studio    # Open Drizzle Studio
npm run seed         # Seed database with sample data
```

## 📦 Project Structure

```
├── app/                 # Next.js app directory
├── components/          # Reusable UI components
├── database/           # Database schema and utilities
├── lib/                # Utility functions and configurations
├── public/             # Static assets
├── styles/             # Global styles
└── migrations/         # Database migrations
```

---

**Built with ❤️ using Next.js and modern web technologies**
