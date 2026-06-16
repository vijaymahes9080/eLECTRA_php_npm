# eLECTRA - Electricity Billing Portal

eLECTRA is a powerful and secure electricity billing portal designed for major power boards. It uses dynamic PDF generation to view and print bills along with a web view. The application is built on top of Laravel 5.5 and offers industry-ready structures for billing, user accounts, and administration.

---

## Features

- **User Authentication**: Secure Login, Registration, and Password Reset for clients.
- **Admin Dashboard**: Dedicated administration panel with full control over user records and billing information.
- **Dynamic PDF Generation**: High-quality PDF bill generation powered by `barryvdh/laravel-dompdf` for easy print and download.
- **Responsive Web Design**: Clean, mobile-friendly interface for managing accounts and viewing invoices.
- **Preconfigured Database Schema**: Ready-to-import database schema included in `a sql file/electra.sql`.

---

## Tech Stack & Requirements

- **PHP**: `>= 7.0.0`
- **Framework**: Laravel 5.5
- **Database**: MySQL
- **Asset Compiler**: Laravel Mix (Webpack) / NPM
- **Dependencies Management**: Composer & NPM

---

## Installation & Setup

Follow these steps to set up eLECTRA on your local system:

### 1. Prerequisites
Make sure you have **PHP (>= 7.0)**, **Composer**, **Node.js/NPM**, and **MySQL** installed on your machine.

### 2. Clone the Repository
```bash
git clone https://github.com/vijaymahes9080/eLECTRA_php_npm.git
cd eLECTRA
```

### 3. Install PHP Dependencies
Run Composer to download and install backend dependencies:
```bash
composer install
```

### 4. Install Front-end Dependencies
Run NPM to install client-side packages:
```bash
npm install
```

### 5. Setup Environment File
Copy the example environment configuration file to create your own `.env` file:
```bash
copy .env.example .env
```
*(On Linux/macOS, use `cp .env.example .env`)*

### 6. Generate Application Key
Generate a secure encryption key for your Laravel installation:
```bash
php artisan key:generate
```

### 7. Database Setup
1. Create a database named `electra` in your MySQL server.
2. Open the `.env` file and configure your database credentials:
   ```env
   DB_CONNECTION=mysql
   DB_HOST=127.0.0.1
   DB_PORT=3306
   DB_DATABASE=electra
   DB_USERNAME=your_database_username
   DB_PASSWORD=your_database_password
   ```
3. Import the initial database backup from `a sql file/electra.sql` into your database using phpMyAdmin, MySQL CLI, or any database tool:
   ```bash
   mysql -u your_database_username -p electra < "a sql file/electra.sql"
   ```

### 8. Run the Server
Launch the local PHP development server:
```bash
php artisan serve
```
Access the application by navigating to `http://127.0.0.1:8000` in your web browser.

---

## License

This project is licensed under the [MIT License](LICENSE).
