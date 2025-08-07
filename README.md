AI-Ticket-Assistant 
Welcome to the AI-Powered Ticket Management System! 
AI-Powered Ticket Management System
A smart ticket management system that uses AI to automatically categorize, prioritize, and assign support tickets to the most appropriate moderators.

🚀 Features
AI-Powered Ticket Processing

Automatic ticket categorization
Smart priority assignment
Skill-based moderator matching
AI-generated helpful notes for moderators
Smart Moderator Assignment

Automatic matching of tickets to moderators based on skills
Fallback to admin assignment if no matching moderator found
Skill-based routing system
User Management

Role-based access control (User, Moderator, Admin)
Skill management for moderators
User authentication with JWT
Background Processing

Event-driven architecture using Inngest
Automated email notifications
Asynchronous ticket processing
🛠️ Tech Stack
Backend: Node.js with Express
Database: MongoDB
Authentication: JWT
Background Jobs: Inngest
AI Integration: Google Gemini API
Email: Nodemailer with Mailtrap
Development: Nodemon for hot reloading
📋 Prerequisites
Node.js (v14 or higher)
MongoDB
Google Gemini API key
Mailtrap account (for email testing)
⚙️ Installation
Clone the repository

🚀 Running the Application
Start the main server

npm run dev
Start the Inngest dev server

npm run inngest-dev
📝 API Endpoints
Authentication
POST /api/auth/signup - Register a new user
POST /api/auth/login - Login and get JWT token
Tickets
POST /api/tickets - Create a new ticket
GET /api/tickets - Get all tickets for logged-in user
GET /api/tickets/:id - Get ticket details
Admin
GET /api/auth/users - Get all users (Admin only)
POST /api/auth/update-user - Update user role & skills (Admin only)
🔄 Ticket Processing Flow
Ticket Creation

User submits a ticket with title and description
System creates initial ticket record
AI Processing

Inngest triggers on-ticket-created event
AI analyzes ticket content
Generates:
Required skills
Priority level
Helpful notes
Ticket type
Moderator Assignment

System searches for moderators with matching skills
Uses regex-based skill matching
Falls back to admin if no match found
Updates ticket with assignment
Notification

Sends email to assigned moderator
Includes ticket details and AI-generated notes



