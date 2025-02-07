# MAST5112-POE-2025

# Online Food Menu App

This is a simple web application for showcasing Christoffel's online food menu. It allows customers to explore menu items, view details, and contact the business directly. This README will guide you through setting up and running the app on your local machine.

 Prerequisites

Before running the app, make sure you have the following installed:

- PHP 7.0+: For running the server-side scripts.
- MySQL: To store the menu data.
- Web Server (e.g., Apache or Nginx with PHP support).

How to Run the App

 Step 1: Clone the Repository

Clone the app's repository to your local machine by running:

```bash
git clone https://github.com/yourusername/food-menu-app.git
```

 Step 2: Set Up the Database

1. Create a MySQL Database:
   - Log into MySQL:
     ```bash
     mysql -u root -p
     ```
   - Create a database (e.g., `food_menu`):
     ```sql
     CREATE DATABASE food_menu;
     ```
   
2. Import the `tbl_menu` Table:
   - Inside the `food-menu-app` folder, you will find a SQL file containing the necessary database structure. Import it into your MySQL database:
     ```bash
     mysql -u root -p food_menu < path/to/tbl_menu.sql
     ```

Step 3: Configure Database Connection

1. Edit the `conn/conn.php` file to set your database credentials:
   ```php
   <?php
   $conn = new PDO('mysql:host=localhost;dbname=food_menu', 'username', 'password');
   ?>
   ```
   Replace `'username'` and `'password'` with your MySQL username and password.

Step 4: Upload to Your Web Server

- If you're running a local server (like XAMPP or MAMP), place the files in the server's root directory (e.g., `htdocs` for XAMPP).
- If you're using Apache or Nginx on a remote server, upload the files to your server's web directory.

 Step 5: Run the App

1. Open a web browser and go to:
   ```text
   http://localhost/food-menu-app/
   ```
   Or, if hosted remotely, access it via the domain.

2. Navigate through the Home, Food Menu, and Contact Us sections. You will be able to view and interact with the food menu, and submit contact forms.

 Notes

- The Admin Area is accessible through the "Admin Area" link in the navbar. Ensure proper security measures are in place if you plan to allow admin access.
  
 License

This project is licensed under the MIT License.

```

This version is focused on getting the app up and running quickly with clear instructions on setting up dependencies, configuring the database, and launching the app.
