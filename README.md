# To-Do List Management System

## Overview

The To-Do List Management System is a desktop application developed using Java Swing and MySQL that helps users efficiently manage their daily tasks. The application provides an intuitive graphical user interface (GUI) for creating, updating, deleting, and tracking tasks while storing all task data in a MySQL database.

## Features

* Add new tasks
* Edit existing tasks
* Delete tasks
* Mark tasks as completed
* View all tasks in a tabular format
* Persistent storage using MySQL database
* User-friendly Java Swing interface

## Tech Stack

* Java
* Java Swing
* JDBC
* MySQL

## Project Structure

JAVA/
├── src/
│ ├── DatabaseHelper.java
│ └── ToDoListApp.java
├── lib/
│ └── mysql-connector-j-9.2.0.jar
└── out/

### Components

#### DatabaseHelper.java

Handles all database operations:

* Database connection
* Table creation
* Insert task
* Retrieve tasks
* Update task
* Delete task
* Mark task as completed

#### ToDoListApp.java

Manages the graphical user interface:

* Task input field
* Task display table
* Add, Edit, Delete, and Complete buttons
* Event handling and task management

## Database Setup

### Create Database

```sql
CREATE DATABASE todo_app;
```

### Table Structure

```sql
CREATE TABLE tasks (
    id INT PRIMARY KEY AUTO_INCREMENT,
    description VARCHAR(255) NOT NULL,
    status VARCHAR(20) DEFAULT 'Pending',
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

## Installation

1. Install Java JDK 8 or above.
2. Install MySQL Server.
3. Create the database and table.
4. Update database credentials in `DatabaseHelper.java`.

```java
private static final String URL = "jdbc:mysql://localhost:3306/todo_app";
private static final String USER = "root";
private static final String PASSWORD = "your_password";
```

5. Add MySQL JDBC Connector to the project.
6. Compile and run the application.

## How to Use

1. Launch the application.
2. Enter a task in the text field.
3. Click **Add Task** to save it.
4. Select a task and:

   * Click **Edit Task** to modify it.
   * Click **Delete Task** to remove it.
   * Click **Mark as Completed** to update its status.
5. View all tasks in the task table.

## Learning Outcomes

* Java GUI development using Swing
* Database integration using JDBC
* CRUD operations with MySQL
* Event-driven programming
* Desktop application development

## Future Enhancements

* Task priority levels
* Due date reminders
* Search and filter functionality
* User authentication
* Export tasks to CSV/PDF
* Dark mode support
