# CivicSync - Community Issue Reporting System

CivicSync is a web-based platform that allows community members to report and track local issues, fostering better communication between citizens and local authorities.

## Prerequisites

- XAMPP (Apache, MySQL, PHP)
- Web browser
- Internet connection

## Installation Steps

1. **Download and Install XAMPP**
   - Download XAMPP from [https://www.apachefriends.org/](https://www.apachefriends.org/)
   - Install XAMPP with Apache and MySQL components
   - Start Apache and MySQL services from XAMPP Control Panel

2. **Database Setup**
   - Open phpMyAdmin (http://localhost/phpmyadmin)
   - Create a new database named `civicsync`
   - Import the database schema from `database/civicsync.sql`
   - Run `fix_tables.php` to ensure all required tables are created:
     ```bash
     php fix_tables.php
     ```

3. **Application Setup**
   - Clone or download this repository
   - Place the files in your XAMPP htdocs directory (typically `C:\xampp\htdocs\civicsync`)
   - Configure database connection in `config/database.php`:
     ```php
     $host = "localhost";
     $username = "root";
     $password = "";
     $dbname = "civicsync";
     ```

4. **File Permissions**
   - Ensure the `uploads` directory has write permissions
   - Set appropriate permissions for image uploads

## Usage Guide

### User Registration
1. Navigate to `register.php`
2. Fill in the registration form with:
   - Username
   - Email address
   - Password
3. Click "Register" to create your account

### User Login
1. Go to `login.php`
2. Enter your credentials
3. Click "Login" to access your account

### Reporting Issues
1. Log in to your account
2. Click "Report Issue" in the navigation menu
3. Fill in the issue details:
   - Title
   - Description
   - Category
   - Location
   - Upload image (optional)
4. Click "Submit" to report the issue

### Viewing Issues
1. Browse issues on the home page
2. Click on an issue to view details
3. Add comments or vote on issues
4. Track issue status updates

### Admin Features
1. Access admin dashboard at `admin/index.php`
2. Manage user accounts
3. Update issue statuses
4. View system statistics

## File Structure

```
civicsync/
├── admin/              # Admin interface files
├── config/             # Configuration files
├── includes/           # Shared PHP functions
├── uploads/            # User uploaded files
├── assets/             # CSS, JS, and images
├── index.php           # Main application page
├── login.php           # User login
├── register.php        # User registration
├── report_issue.php    # Issue reporting form
└── view_issue.php      # Issue details page
```

## Security Features

- Password hashing
- SQL injection prevention
- XSS protection
- Session management
- Input validation
- File upload restrictions

## Troubleshooting

1. **Database Connection Issues**
   - Verify XAMPP services are running
   - Check database credentials in `config/database.php`
   - Ensure database exists and is accessible

2. **File Upload Issues**
   - Check `uploads` directory permissions
   - Verify PHP upload settings in php.ini
   - Check file size limits

3. **Session Issues**
   - Clear browser cookies
   - Check PHP session configuration
   - Verify session storage permissions

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Support

For support, please contact the development team or create an issue in the repository. 
