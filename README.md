# Task Management System

A modern and efficient web-based task management system built with PHP and MySQL. This application helps teams and individuals organize their work by providing a robust platform for task creation, assignment, tracking, and management.

![Task Management System](https://img.shields.io/badge/Task-Management-blue)
![PHP](https://img.shields.io/badge/PHP-7.4+-purple)
![MySQL](https://img.shields.io/badge/MySQL-5.7+-orange)
![License](https://img.shields.io/badge/License-MIT-green)

## 🌟 Features

### User Management
- Role-based access control (Admin, Manager, User)
- Secure authentication system
- User profile management
- Password reset functionality
- Team member management

### Task Management
- Create, edit, and delete tasks
- Assign tasks to team members
- Set task priorities (High, Medium, Low)
- Track task status (Pending, In Progress, Completed)
- Due date management
- Task filtering and search

### Dashboard
- Overview of task statistics
- Recent activity tracking
- Team member status
- Project progress visualization
- Quick access to important functions

### Additional Features
- Responsive design for all devices
- Real-time notifications
- Clean and intuitive user interface
- Secure data handling
- Export functionality

## 🛠️ Tech Stack

- **Backend:**
  - PHP 7.4+
  - MySQL 5.7+
  - MVC Architecture

- **Frontend:**
  - HTML5
  - CSS3
  - JavaScript (ES6+)
  - Font Awesome Icons

- **Development Tools:**
  - Git for version control
  - VS Code recommended

## 📋 Prerequisites

Before you begin, ensure you have the following installed:
- PHP 7.4 or higher
- MySQL 5.7 or higher
- Web server (Apache/Nginx)
- Composer (for dependency management)

## 🚀 Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/task-manager.git
   ```

2. Navigate to the project directory:
   ```bash
   cd task-manager
   ```

3. Import the database:
   - Create a new MySQL database named `task_manager`
   - Import the `task_manager.sql` file from the project root

4. Configure the database connection:
   - Open `config/database.php`
   - Update the database credentials:
     ```php
     define('DB_SERVER', 'localhost');
     define('DB_USERNAME', 'your_username');
     define('DB_PASSWORD', 'your_password');
     define('DB_NAME', 'task_manager');
     ```

5. Start your local server:
   ```bash
   php -S localhost:8000
   ```

6. Access the application:
   - Open your browser and navigate to `http://localhost:8000`

## 📁 Project Structure

```
task-manager/
├── assets/
│   ├── css/
│   ├── js/
│   └── images/
├── config/
├── controllers/
├── models/
├── views/
│   ├── auth/
│   ├── dashboard/
│   ├── tasks/
│   └── user/
├── public/
└── README.md
```

## 🏗️ Architecture & Design Patterns

### MVC Architecture
The project follows the Model-View-Controller (MVC) pattern:
- **Models**: Handle data logic and database operations
- **Views**: Manage the presentation layer and user interface
- **Controllers**: Process user requests and coordinate between models and views

### SOLID Principles Implementation
1. **Single Responsibility Principle (SRP)**
   - Each class has a single responsibility
   - Separate controllers for different functionalities (TaskController, UserController, AdminController)
   - Models handle only data-related operations

2. **Open/Closed Principle (OCP)**
   - User interface implementation allows extension without modification
   - Task status system is extensible for new statuses
   - Factory pattern for user creation

3. **Liskov Substitution Principle (LSP)**
   - User hierarchy allows substitution of derived classes
   - Admin and RegularUser classes can be used interchangeably where User is expected

4. **Interface Segregation Principle (ISP)**
   - UserInterface defines only necessary methods
   - Separate interfaces for different functionalities
   - Clean separation of concerns in model interfaces

5. **Dependency Inversion Principle (DIP)**
   - High-level modules depend on abstractions
   - Database connection is injected rather than created directly
   - Controllers depend on interfaces rather than concrete implementations

### Design Patterns Used
1. **Factory Pattern**
   - UserFactory for creating different types of users
   - Abstract factory pattern for user creation
   - Allows easy addition of new user types

2. **Observer Pattern**
   - Task status changes notify relevant components
   - Event-driven architecture for task updates
   - Notification system for task assignments

3. **Strategy Pattern**
   - Different authentication strategies
   - Multiple task filtering strategies
   - Configurable task priority handling

4. **Repository Pattern**
   - Data access abstraction
   - Centralized database operations
   - Consistent data handling across the application

5. **Singleton Pattern**
   - Database connection management
   - Configuration handling
   - Session management

### Code Organization
- Clear separation of concerns
- Modular component structure
- Reusable code components
- Consistent coding standards
- Easy to maintain and extend

## 🔒 Security Features

- Password hashing using PHP's password_hash()
- SQL injection prevention
- XSS protection
- CSRF protection
- Input validation and sanitization


⭐ Star this repository if you find it helpful! 