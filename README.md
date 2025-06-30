
# SecureWeb– PHP User Authentication System

A simple and secure user authentication system built with PHP and MySQL. This project includes user registration, login, profile management, password reset, and session handling functionalities.

## 📁 Project Structure

```
htdocs/
│
├── index.php               # Homepage
├── register.php            # User registration form
├── login.php               # Login page
├── logout.php              # Logout and session destroy
├── profile.php             # Authenticated user profile
├── reset_password.php      # Request password reset
├── new_password.php        # Set new password
├── verify_code.php         # Email/code verification
├── verify_login.php        # Login logic
├── data_management.php     # (Optional) Manage user data
├── delete_data.php         # (Optional) Delete user account or data
│
├── css/                    # Custom stylesheets
├── includes/               # PHP includes (database, auth helpers)
├── session_debug.txt       # Debugging session variables (temporary)
│
├── if0_38236144_secure_app.sql  # MySQL database structure
└── composer.json           # Composer dependencies (if used)
```

## ⚙️ Features

- ✅ User registration with validation
- ✅ Email/code verification system (optional)
- ✅ Secure login with sessions
- ✅ Password reset (via verification code)
- ✅ Profile page (update/view info)
- ✅ Logout & session destruction
- ✅ Protection against SQL Injection
- ✅ Password hashing using `password_hash()`

## 🏁 Getting Started

### 📌 Requirements

- PHP 7.4+
- MySQL or MariaDB
- Apache/Nginx (or use XAMPP/Laragon)
- Composer (optional)

### 🔧 Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/secureapp.git
   ```

2. **Import the database:**
   - Create a MySQL database (e.g. `secure_app`)
   - Import the `if0_38236144_secure_app.sql` file into it

3. **Configure database connection:**
   - Open `includes/db.php` (or similar)
   - Update:
     ```php
     $host = "localhost";
     $user = "root";
     $pass = "";
     $dbname = "secure_app";
     ```

4. **Run locally:**
   - Start Apache and MySQL
   - Visit `https://secureapp.free.nf/register.php` in your browser

## 🔐 Security Notes

- Passwords are hashed using PHP’s `password_hash()` function
- SQL statements use `mysqli_real_escape_string()` or `prepared statements`
- Session hijacking is mitigated by checking user session values

## 💡 To-Do (Improvements)

- Add email sending for password reset
- Use prepared statements (PDO or MySQLi)
- Integrate CSRF protection
- Add front-end validation with JavaScript

## 🧑‍💻 Author

- **Hamza Al-Haidari*https://github.com/Hamzzaal/Hamzzaal)
- LinkedIn: [Hamza Al-Haidari](https://linkedin.com/in/hamzah-alhaidari-bb2228219/)

## 📄 License

This project is open-source and free to use under the MIT License.
