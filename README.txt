LoginRegisterApp - Setup Instructions
====================================

Login/registration system using Java Swing, NetBeans IDE 26, XAMPP MySQL. Returns to MainMenu after login. Run Main.java.

1. Install XAMPP:
   - Download: https://www.apachefriends.org/.
   - Install defaults (e.g., C:\xampp).
   - Start MySQL.

2. Set Up MySQL Database:
   - http://localhost/phpmyadmin.
   - Create "user_db".
   - Run create_database.sql:
     ``````````````````````````````````````````
     CREATE TABLE users (
         id INT AUTO_INCREMENT PRIMARY KEY,
         nickname VARCHAR(50) NOT NULL,
         username VARCHAR(50) NOT NULL UNIQUE,
         password VARCHAR(50) NOT NULL
     );
     ``````````````````````````````````````````

3. Add MySQL Connector:
   - Use lib/mysql-connector-java-8.0.33.jar.
   - NetBeans: Libraries > Add JAR/Folder.
   - Download: https://dev.mysql.com/downloads/connector/j/ (8.0.33).

4. Verify MySQL Credentials:
   - DatabaseConnection.java: user "root", password "".
   - Update if different.

5. Font and Design:
   - Font: Public Pixel (https://www.dafont.com/public-pixel.font).
   - Fallback: Arial (Design tab > Properties > font).
   - Background: Copy background.png to src/loginregisterapp/images/, set via code in constructor (see LoginForm.java).
   - Buttons: Background RGB(30, 144, 255), foreground White, Public Pixel.

6. Run Application:
   - NetBeans 26, JDK 17.
   - Run Main.java.
   - Register (Nickname, Username, Password), login to MainMenu.

7. Main Menu Integration:
   - Replace MainMenu.java with your MainMenu (extends JFrame).
   - LoginForm/RegisterForm require MainMenu.

8. Troubleshooting:
   - MySQL error? Check port 3306.
   - Database error? Verify user_db/users.
   - Background error? Ensure background.png in src/loginregisterapp/images/.
   - Font missing? Install Public Pixel or Arial.
   - Contact [your name].

Requirements:
- Java JDK 17
- Apache NetBeans IDE 26
- XAMPP MySQL
- mysql-connector-java-8.0.33.jar
- Public Pixel font
- src/loginregisterapp/images/background.png