# User Management System (Java Servlet + JSP + MySQL)

## 📌 Project Overview
This project is a **User Management Web Application** developed using Java web technologies.  
It allows users to perform **CRUD operations (Create, Read, Update, Delete)** on user records stored in a MySQL database.

The application follows the **MVC (Model-View-Controller) architecture**, which separates business logic, presentation, and data handling for better maintainability.

---

## 🚀 Features
- Add new users
- View list of users
- Edit existing user information
- Delete users
- Database connectivity using JDBC
- Simple and responsive UI using Bootstrap

---

## 🛠 Technologies Used

| Technology | Description |
|------------|-------------|
| Java | Backend programming language |
| Servlets | Handles HTTP requests and responses |
| JSP | Used for dynamic web pages |
| JDBC | Connects Java application to MySQL |
| MySQL | Database for storing user data |
| Apache Tomcat | Web server for running the application |
| Bootstrap | Frontend styling |

---

## 📂 Project Structure


UserManagement
│
├── src
│ └── com.xadmin.usermanagement
│ ├── dao
│ │ └── UserDAO.java
│ │
│ ├── model
│ │ └── User.java
│ │
│ └── web
│ └── UserServlet.java
│
├── WebContent
│ ├── user-list.jsp
│ ├── user-form.jsp
│ ├── Error.jsp
│ │
│ └── WEB-INF
│ ├── web.xml
│ └── lib
│ ├── mysql-connector.jar
│ └── jstl.jar


---

## 🧱 Architecture (MVC)

This project follows the **Model-View-Controller architecture**.

### Model
Handles application data.


User.java


Represents the user entity with attributes like:

- id
- name
- email
- country

---

### View
Responsible for displaying data to users.


user-list.jsp
user-form.jsp


Functions:
- Display user data
- Provide forms to add/update users

---

### Controller


UserServlet.java


Functions:
- Receives HTTP requests
- Calls DAO methods
- Redirects to JSP pages

---

### Data Access Layer


UserDAO.java


Handles database operations:

- Insert user
- Select user
- Update user
- Delete user

---

## 🔄 Application Flow


Browser
↓
UserServlet (Controller)
↓
UserDAO (Database Logic)
↓
MySQL Database
↓
JSP Pages (View)


---

## 🗄 Database Setup

Create the database in MySQL.

```sql
CREATE DATABASE userdb;

USE userdb;

CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    email VARCHAR(100),
    country VARCHAR(100)
);
⚙️ How to Run the Project
1️⃣ Clone the repository
git clone https://github.com/yourusername/UserManagement
2️⃣ Import project into Eclipse

Open Eclipse IDE

File → Import → Existing Projects into Workspace
3️⃣ Configure MySQL

Update database credentials in:

UserDAO.java

Example:

private String jdbcURL = "jdbc:mysql://localhost:3306/userdb";
private String jdbcUsername = "root";
private String jdbcPassword = "yourpassword";
4️⃣ Add required libraries

Add the following JAR files:

mysql-connector-java
jstl.jar
servlet-api.jar
5️⃣ Run the project

Start Apache Tomcat server.

Open the application:

http://localhost:8080/UserManagement/
📸 Screenshots

Add screenshots here:

User List Page
Add User Form
Database Table
📚 What I Learned

Building web applications using Java Servlets and JSP

Understanding MVC architecture

Database connectivity using JDBC

Implementing CRUD operations

Deploying applications on Apache Tomcat

Structuring Java web projects

🔗 GitHub Repository
https://github.com/yourusername/UserManagement
👨‍💻 Author

