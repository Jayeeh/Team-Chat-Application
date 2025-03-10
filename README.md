## Team Chat Application (Laravel)

### Prerequisites
- Used **Stable PHP 8.4.4** in [PHP Official Site](https://www.php.net/downloads)
- Used **PEAR package manager** in [PEAR Official Site](https://pear.php.net/manual/en/installation.getting.php)
- Used **Composer v2.8.6** in [Composer Official Site](https://getcomposer.org/download/)
- Used **7-Zip 24.09** in [7-Zip Official Site](https://www.7-zip.org/download.html)
- Used **Node.js v22.14.0 LTS** in [Node.js Official Site](https://nodejs.org/en/download/)
- Used **PostgreSQL 17.4** in [PostgreSQL Official Site](https://www.postgresql.org/download/windows/)
- Used **Laravel 12.0**

### Installation
1. Install PHP 8.4.4 in [PHP Official Site](https://www.php.net/downloads)
   - Download the **VS17 x64 Thread Safe (2025-Feb-11 16:30:00)** ZIP file.
   - Extract the ZIP file to the desired location. (e.g: `C:\php-8.4.4`)
   - Add the PHP folder (``C:\php``) to the system environment variable PATH.
   - To verify it's installation, open command prompt and type `php -v`. (If it's not showing up, try opening another command prompt or restart your computer.)
2. Edit your `php.ini` file.
   - Open the `php.ini` file and uncomment the following lines:
   ```ini
   extension=fileinfo
   extension=pdo_pgsql
   ```
3. Install PEAR
   - Download the **go-pear.phar** file and paste it to your PHP installation folder. (e.g: `C:\php`)
   - Using comma prompt, change directory to the **go-pear.phar**'s file location (e.g: `C:\php`) then run `php go-pear.phar`
4. Install Composer v2.8.6 in [Composer Official Site](https://getcomposer.org/download/)
   - Download the **Composer Setup.exe** file.
   - Run the Composer Setup.exe file.
   - To verify it's installation, open command prompt and type `composer -V`. (If it's not showing up, try opening another command prompt or restart your computer.)
5. Install 7-Zip 24.09 in [7-Zip Official Site](https://www.7-zip.org/download.html)
   - Download the **7z2409-x64.exe** installer.
   - Run the installation file.
   - Add the 7-Zip folder (`C:\Program Files\7-Zip`) to the system environment variable PATH.
   - To verify it's installation, open command prompt and type `7z`. (If it's not showing up, try opening another command prompt or restart your computer.)
6. Install Node.js
7. Install PostgreSQL and configure your local database.
8. Install Laravel
   ```
   composer global require laravel/installer
   ```
9. Don't forget to create a `.env` file to configure the PostgreSQL database. *(Use .env.example as a template)*
   - Uncomment the following lines and change it to your local PostgreSQL database:
      ```ini
      DB_CONNECTION=pgsql
      DB_HOST=127.0.0.1
      DB_PORT=5432
      DB_DATABASE=laravel
      DB_USERNAME=postgres
      DB_PASSWORD=postgres
      ```
10. Finally, build the Laravel project.
    ```
    npm install
    npm run build
    php artisan serve
    ```