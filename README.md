# Student Records API

This is a simple REST API built with Express.js and MySQL.  
It lets you manage students and courses with full CRUD (Create, Read, Update, Delete).  

---

## Setup

npm install

CREATE DATABASE student_records;

USE student_records;

CREATE TABLE students (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(100) NOT NULL,
  email VARCHAR(100) NOT NULL UNIQUE,
  age INT NOT NULL
);

CREATE TABLE courses (
  id INT AUTO_INCREMENT PRIMARY KEY,
  code VARCHAR(20) NOT NULL UNIQUE,
  title VARCHAR(255) NOT NULL,
  units INT NOT NULL
);

Make a .env file in the project root:

DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_mysql_password
DB_NAME=student_records
PORT=3000

server runs at http://localhost:3000

POSTMAN NOTES: 
Endpoints
Health

GET /api/health → check if server and DB are running

//Students

POST /api/students → add a student
GET /api/students → get all students
GET /api/students/:id → get a student by id
PUT /api/students/:id → update a student
DELETE /api/students/:id → delete a student

//Courses

POST /api/courses → add a course
GET /api/courses → get all courses
GET /api/courses/:id → get a course by id
PUT /api/courses/:id → update a course
DELETE /api/courses/:id → delete a course
