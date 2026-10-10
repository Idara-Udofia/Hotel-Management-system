# 🏨 Hotel Management System

A web-based **Hotel Management System** developed using HTML, CSS, Bootstrap, JavaScript, PHP, and MySQL. The system is designed to simplify hotel operations by providing an organized platform for managing rooms, guest records, reservations, check-in/check-out activities, payments, and other essential hotel services.

Database Name : - hotel.sql
user name : - Admin
password  : - admin123

## 📖 About the Project

The Hotel Management System is a dynamic web application developed to automate hotel management processes and reduce the challenges associated with manual record keeping.

The application provides a centralized system for authorized hotel personnel to manage guest information, room availability, reservations, billing, and payment records. Its responsive interface enables users to access the system through modern web browsers on desktop computers, tablets, and mobile devices.

The project uses PHP for server-side processing and MySQL for database management, while HTML, CSS, Bootstrap, and JavaScript provide the user interface and interactive functionality.

## 🎯 Objectives

The major objectives of this project are to:

- Automate hotel room reservation and management.
- Maintain accurate guest records.
- Monitor room availability and occupancy.
- Simplify guest check-in and check-out.
- Manage hotel bills and payment records.
- Reduce paperwork and minimize record-keeping errors.
- Improve the efficiency of daily hotel operations.
- Provide a user-friendly and responsive interface.

## ✨ Features

### 1. Admin Dashboard
- View hotel operational summaries.
- Monitor rooms, guests, and reservations.
- Review payment and booking information.
- Access available management modules.

### 2. Room Management
- Add, update, and delete room records.
- Manage room categories and prices.
- View room availability and occupancy status.
- Track rooms under maintenance.

### 3. Reservation Management
- Create and manage guest reservations.
- Record check-in and check-out dates.
- Check room availability.
- Track confirmed, pending, and cancelled bookings.
- Prevent overlapping reservations when properly implemented.

### 4. Guest Management
- Register new guests.
- Store and update guest information.
- View guest booking history.
- Maintain guest contact details.

### 5. Check-In and Check-Out
- Record guest arrivals and departures.
- Update room occupancy status.
- Calculate applicable accommodation charges.
- Maintain check-in and check-out records.

### 6. Billing and Payment Management
- Generate guest bills.
- Calculate accommodation costs.
- Record payments and outstanding balances.
- Track payment status and transaction history.

### 7. User Authentication
- Provide a login system for authorized users.
- Protect restricted pages from unauthorized access.
- Support administrator and staff access where configured.

### 8. Responsive Interface
- Bootstrap-based responsive layouts.
- Interactive forms and navigation.
- Organized tables and management pages.
- Compatibility with modern web browsers.

*Note: The features above describe the intended system functionality. Retain only features implemented in your actual application.*

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| HTML5 | Structures web pages and application content |
| CSS3 | Styles the interface and page layouts |
| Bootstrap | Provides responsive layouts and UI components |
| JavaScript | Adds client-side interactivity and validation |
| PHP | Handles server-side logic and application processing |
| MySQL | Stores and manages application data |
| Apache | Serves the application locally or on a web server |
| Git and GitHub | Version control and source code hosting |

## 💻 System Requirements

Before installing the project, ensure you have:

- Windows, Linux, or macOS.
- PHP 8.0 or later, compatible with the codebase.
- MySQL 8.0 or a compatible MySQL/MariaDB version.
- Apache web server.
- XAMPP, WAMP, or an equivalent local development environment.
- A modern web browser.
- Visual Studio Code or another code editor.
- Git (optional, for cloning and version control).

## ⚙️ Installation and Setup

Follow these steps to install and run the application locally.

### Step 1: Install the Development Environment

Download and install [XAMPP](https://www.apachefriends.org/).

XAMPP provides Apache, PHP, and MariaDB/MySQL-compatible database services for local development.

Start the **Apache** and **MySQL** services from the XAMPP Control Panel.

### Step 2: Clone the Repository

Open your terminal and run:

```bash
git clone https://github.com/YOUR-USERNAME/hotel-management-system.git
```

Navigate to the project directory:

```bash
cd hotel-management-system
```

Replace `YOUR-USERNAME` and the repository name with your actual GitHub details.

Alternatively, download the repository as a ZIP file and extract it.

### Step 3: Move the Project into the Web Directory

For XAMPP on Windows, place the project folder inside:

```text
C:\xampp\htdocs\hotel-management-system
```

### Step 4: Create the Database

Open phpMyAdmin in your browser:

```text
http://localhost/phpmyadmin
```

Create a new database named:

```sql
CREATE DATABASE hotel_management;
```

If your repository includes a database export file, such as `hotel_management.sql`, import it into the newly created database using phpMyAdmin's **Import** feature.

### Step 5: Configure the Database Connection

Locate the PHP database configuration file in your project. It may be named `config.php`, `db.php`, or `database.php`.

Configure the connection with your local database credentials. For example, using MySQLi:

```php
<?php
$host = "localhost";
$username = "root";
$password = "";
$database = "hotel.sql";

$conn = new mysqli(
    $host,
    $username,
    $password,
    $database
);

if ($conn->connect_error) {
    error_log("Database connection failed: " . $conn->connect_error);
    exit("Unable to connect to the database.");
}

$conn->set_charset("utf8mb4");
?>
```

Adjust the settings to match your environment. The example uses the common default XAMPP configuration; do not use an empty database password in production.

If your project already has a database connection file, update that file instead of creating a duplicate connection.

### Step 6: Launch the Application

Open your browser and visit:

```text
http://localhost/hotel-management-system/
```

If the project uses a specific entry page, such as `index.php` or `login.php`, open the appropriate page.

### Step 7: Log In

If authentication is implemented, sign in using an account configured in the database or through the application's supported account-creation process.

Do not assume default login credentials unless they are explicitly documented in your project.

## 🗄️ Database Structure

The application may use the following database tables, depending on the implementation:

| Table | Description |
|---|---|
| `users` | Stores administrator and staff account information |
| `guests` | Stores guest details |
| `rooms` | Stores room numbers, categories, prices, and status |
| `reservations` | Stores booking details and reservation dates |
| `payments` | Stores payment transactions |
| `invoices` | Stores guest billing records |
| `services` | Stores additional hotel services |

These are suggested table names. The actual database schema should match the SQL file or database structure supplied with your project.

## 📂 Project Structure

A typical PHP-based implementation may use the following folder structure:

```text
hotel-management-system/
│
├── index.php
├── login.php
├── dashboard.php
├── logout.php
│
├── config/
│   └── database.php
│
├── admin/
│   ├── dashboard.php
│   ├── rooms.php
│   ├── guests.php
│   ├── reservations.php
│   ├── payments.php
│   └── reports.php
│
├── includes/
│   ├── header.php
│   ├── navbar.php
│   ├── sidebar.php
│   └── footer.php
│
├── assets/
│   ├── css/
│   │   └── style.css
│   ├── js/
│   │   └── script.js
│   └── images/
│
├── database/
│   └── hotel_management.sql
│
├── README.md
└── .gitignore
```

**Important:** This is an example structure. Modify it to reflect the actual files and folders in your repository.

## 🧩 System Modules

The system can be organized into these main modules:

1. **Authentication Module:** Manages user login and access control.
2. **Room Management Module:** Manages room details, prices, and availability.
3. **Guest Management Module:** Maintains guest registration and records.
4. **Reservation Module:** Handles bookings and reservation schedules.
5. **Check-In/Check-Out Module:** Records guest arrivals and departures.
6. **Billing Module:** Calculates charges and maintains invoices.
7. **Payment Module:** Records payments and outstanding balances.
8. **Reporting Module:** Presents operational and financial summaries.

## 🔐 Security

Security is important when managing guest and payment information. Recommended practices include:

- Use PHP password hashing with `password_hash()` and verify passwords with `password_verify()`.
- Use prepared statements for database queries.
- Validate and sanitize user input appropriately.
- Protect authenticated pages with server-side session checks.
- Apply role-based permissions where necessary.
- Implement CSRF protection for sensitive forms.
- Keep database credentials outside publicly accessible files where possible.
- Avoid committing passwords, private configuration files, or real guest information to GitHub.
- Use HTTPS when deploying the system online.

## 🔮 Future Improvements

Potential improvements include:

- Online room booking for guests.
- Integration with Paystack or Flutterwave.
- Email booking confirmations and reminders.
- Restaurant and room-service management.
- Housekeeping and maintenance tracking.
- Printable invoices and downloadable reports.
- Advanced occupancy and revenue analytics.
- Multiple hotel branch management.
- Integration with external booking platforms.

## 🤝 Contributing

Contributions and suggestions are welcome.

To contribute:

1. Fork the repository.
2. Create a feature branch.
3. Implement your changes.
4. Test the functionality.
5. Commit your changes with a descriptive message.
6. Push the branch to your fork.
7. Submit a Pull Request.

## 🐛 Reporting Issues

If you discover a bug or have a feature suggestion, open an issue in the GitHub repository. Include a clear description of the problem and the steps needed to reproduce it. Do not include passwords, private guest information, or other sensitive data.

## 👨‍💻 Author

**Comr. Idara Udofia**

- GitHub: Idara-udofia(https://github.com/Idara-Udofia)
- Project: Hotel Management System(https://github.com/idara-udofia/hotel-management-system)


---

### ⭐ Support

If you find this project useful, consider giving the repository a star on GitHub.

**Built with HTML, CSS, Bootstrap, JavaScript, PHP, and MySQL.**
