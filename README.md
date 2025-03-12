# ReciepeWebsite
🍽️ Cooking Chronicles - Recipe Website
📌 Overview
Cooking Chronicles is a PHP & MySQL-powered recipe website designed for culinary enthusiasts. Users can:
✅ Sign Up & Log In to access personalized features
✅ Browse & Search Recipes with step-by-step instructions
✅ Discover Cooking Tips to improve culinary skills
✅ View an About Us Page to learn about the creators
✅ Contact the Team for queries & support

This platform aims to provide a seamless and interactive experience for users passionate about cooking.

🛠️ Technologies Used
Frontend
HTML, CSS → Structuring & styling web pages
JavaScript → Interactive search functionality
Google Fonts → Enhanced typography (Roboto & Merriweather)
Backend
PHP → Handles authentication & dynamic content
MySQL → Stores user data, recipes, and cooking tips
phpMyAdmin → Manages the database
Development Tools
XAMPP → Local web server (Apache, MySQL, PHP)
VS Code / PHPStorm → Code editor
GitHub → Version control & collaboration
📂 Project Structure
graphql
Copy
Edit
Cooking-Chronicles/
│── index.html        # Main homepage  
│── about.html        # About Us page  
│── cookingtips.html  # Cooking Tips page  
│── contact.html      # Contact Us page  
│── styles.css        # Main CSS file  
│── script.js         # Main JavaScript file  
│── recipes/          # Folder with different recipe pages  
│── assets/           # Images, styles, and scripts  
│── backend/          # PHP backend files  
│── login.php         # User authentication  
│── signup.php        # User registration  
│── config.php        # Database connection  
│── database.sql      # MySQL database schema  
│── README.md         # This file  
🚀 Features
✔️ User Authentication → Signup & Login (PHP & MySQL)
✔️ Recipe Listings → Browse and view detailed cooking instructions
✔️ Search Functionality → Find recipes easily with JavaScript-powered search
✔️ Cooking Tips Module → Useful kitchen hacks and culinary advice
✔️ About Us Page → Information about the creators of Cooking Chronicles
✔️ Responsive Design → Optimized for mobile, tablet, and desktop

🔍 Key Code Examples
📜 User Login System (login.php)
php
Copy
Edit
<?php
require 'config.php';

if ($_SERVER["REQUEST_METHOD"] == "POST") {
    $username = $_POST['username'];
    $password = $_POST['password'];

    $sql = "SELECT * FROM users WHERE username = '$username' AND password = '$password'";
    $result = $conn->query($sql);

    if ($result->num_rows > 0) {
        header('Location: index.html'); 
        exit;
    } else {
        echo "Invalid username or password.";
    }
}
$conn->close();
?>
📜 Search Functionality (script.js)
js
Copy
Edit
function searchRecipe() { 
    const query = document.querySelector('.search-bar input').value.toLowerCase();
    if (query === 'cookies') { window.location.href = 'recipes/cookies.html'; }  
    else if (query === 'soup') { window.location.href = 'recipes/soup.html'; }  
    else if (query === 'pasta') { window.location.href = 'recipes/pasta.html'; }  
    else { alert('Recipe not available'); }
}
🛠️ How to Set Up & Run Locally
1️⃣ Download & Install XAMPP → Download Here
2️⃣ Move the Project to htdocs

sh
Copy
Edit
C:\xampp\htdocs\CookingChronicles
3️⃣ Start XAMPP Services

Open XAMPP Control Panel
Start Apache & MySQL
4️⃣ Import the Database
Open phpMyAdmin (http://localhost/phpmyadmin/)
Create a new database: cooking_chronicles
Import database.sql
5️⃣ Run the Project
Open http://localhost/CookingChronicles/index.html in a browser.
