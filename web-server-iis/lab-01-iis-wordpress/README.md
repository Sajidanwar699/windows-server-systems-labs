# Lab 1: IIS and WordPress Web Server

> **Environment:** Windows Server 2012 R2. The domain `Bkteam.com` and all addresses are lab-only examples.

In this lab we describe, step by step, how to install Internet Information Services (IIS) 8.5 on Windows Server 2012 R2. IIS is the Web server role in Windows Server 2012 R2. The Windows Server 2012 R2 operating system has all the IIS features needed to support the hosting of Web content in production environments. In additionally we will cover setting up WordPress on Windows Server 2012 R2 with IIS, PHP, PHP Manager, PhpMyAdmin and MySQL.

WordPress is a free, open-source website creation platform. On a more technical level, WordPress is a content management system (CMS) written in PHP that uses a MySQL database. In non-geek speak, WordPress is the easiest and most powerful blogging and website builder in existence today. WordPress is an excellent website platform for a variety of websites. From blogging to e-commerce to business and portfolio websites, WordPress is a versatile CMS. Designed with usability and flexibility in mind, WordPress is a great solution for both large and small websites.

To install WordPress on IIS 8.5 by using the Windows Server 2012 R2 follow these steps:

1. Install IIS
2. Download and install WordPress
3. Install the Web Platform Installer
4. Install the Visual C++ Redistributable
5. files Step 5: Installing PHP and PHP Manager using the Web Platform Installer Step 6: Installing MySQL in Windows Server Step 7: Installing PhpMyAdmin in Windows Server 2012 R2 Step 8: Configure wp-config.php Step 9: Using phpMyAdmin Create Database

## 1. IIS (Internet Information Services) Server

**Step 1.** Click Server Manager.

![1. IIS (Internet Information Services) Server – step 1](images/01-step-1.png)

**Step 2.** In Server Manager Dashboard, Click Add roles and features.

![1. IIS (Internet Information Services) Server – step 2](images/02-step-2.png)

**Step 3.** In Before you begin page, click Next.

![1. IIS (Internet Information Services) Server – step 3](images/03-step-3.png)

**Step 4.** In Select installation type, select Role-based or feature-based installation, click Next.

![1. IIS (Internet Information Services) Server – step 4](images/04-step-4.png)

**Step 5.** In Select destination server from Server Pool select Win-Server 2012, click Next.

![1. IIS (Internet Information Services) Server – step 5](images/05-step-5.png)

**Step 6.** In select server roles, check the box Web Server and click Next.

![1. IIS (Internet Information Services) Server – step 6](images/06-step-6.png)

**Step 7.** In Add required features for Web Server (IIS), click Add Features.

![1. IIS (Internet Information Services) Server – step 7](images/07-step-7.png)

**Step 8.** In select features, click Next.

![1. IIS (Internet Information Services) Server – step 8](images/08-step-8.png)

**Step 9.** Click Next.

![1. IIS (Internet Information Services) Server – step 9](images/09-step-9.png)

**Step 10.** Check the box HTTP Redirection, under Common HTTP Features.

![1. IIS (Internet Information Services) Server – step 10](images/10-step-10.png)

**Step 11.** Check the box FTP Service, under FTP Server.

![1. IIS (Internet Information Services) Server – step 11](images/11-step-11.png)

**Step 12.** Check Restart the destination server automatically if required and click Install.

![1. IIS (Internet Information Services) Server – step 12](images/12-step-12.png)

**Step 13.** Click on close. Installation completed.

![1. IIS (Internet Information Services) Server – step 13](images/13-step-13.png)

## 2. Download and Installation WordPress

**Step 1.** First, download the latest stable release of WordPress from WordPress officially site https://wordpress.org/download. For this article, WordPress version 5.7.2 was used.

![2. Download and Installation WordPress – step 1](images/14-step-1.png)

**Step 2.** Uncompressed the downloaded WordPress files and copy the files to C:\Inetpub\wwwroot\wordpress or another directory of your choosing. There is no need to modify permissions on the WordPress Web directory, because the default permissions suffice.

![2. Download and Installation WordPress – step 2](images/15-step-2.png)

## 3. Install the Web Platform Installer

Microsoft Web Platform Installer is a freeware to simplify the workflow of installing common open-source web applications and web platform technologies. It simplifies download, install and keep up-to-date with the latest components of the Microsoft Web Platform. Download and install the package. You can download the Web Platform Installer from here.

![3. Install the Web Platform Installer – figure 16](images/16-figure.png)

After the WPI is installed, open WPI from Apps and install web-packages you want.

![3. Install the Web Platform Installer – figure 17](images/17-figure.png)

## 4. Install Visual C++ Redistributable

The Visual C++ Redistributable is required when installing a default installation of PHP. It will install DLL files that are required by numerous PHP extensions. Without it you will receive HTTP 500 errors and PHP will throw the error “The Fast CGI process exited unexpectedly”.

You can download the Visual C++ Redistributable from here.

## 5. Install PHP and PHP Manager using the Web Platform Installer

Once you’ve installed all the prerequisites you can go ahead and install PHP using the Web Platform Installer.

**Step 1.** Click Start and type “Server Manager” and then hit enter. This should launch the Server Manager application.

![Installer – step 1](images/18-step-1.png)

**Step 2.** Select Tools → Internet Information Services (IIS) Manager.

![Installer – step 2](images/19-step-2.png)

**Step 3.** Select your server’s name from the navigation tree.

![Installer – step 3](images/20-step-3.png)

**Step 4.** Double click Web Platform Installer under Management.

![Installer – step 4](images/21-step-4.png)

**Step 5.** Enter “PHP” in the search field and select the version of PHP you’d like to install. I recommend the latest version of PHP 8 (Currently Latest).

![Installer – step 5](images/22-step-5.png)

**Step 6.** After successfully installing PHP then install PHP Manager for PHP Enter “PHP Manager” in the search field of WPI and select PHP Manager for IIS click Add and then Select Install and accept the terms and conditions. PHP and PHP Manager for IIS should now download and install successfully.

![Installer – step 6](images/23-step-6.png)

Congratulations. You now have a working IIS Server running PHP meeting all requirements of a default PHP installation. Enjoy!

![Installer – step 6](images/24-step-6.png)

## 6. Installing MySQL in Windows Server

**Step 1.** In the Web Platform Installer window, search for MySQL in the search box.

**Step 2.** Select the most current version of MySQL Windows click Add, and then click Install to start the installation.

**Step 3.** Provide a password for the root account of the MySQL server.

**Step 4.** Set MySQL root password

**Step 5.** Review the licensing agreement and click I Accept.

**Step 6.** After the installation is completed, click Finish

## 7. Installing PhpMyAdmin in Windows Server

PhpMyAdmin supports a wide range of operations with MySQL. The most frequently used operations are supported by the user interface (managing databases, tables, fields, relations, indexes, users, permissions, etc.), while you still have the ability to directly execute any SQL statement. PhpMyAdmin is a web-based open-source tool written in PHP designed to help manage MySQL database through the Web browser. Because of this PhpMyAdmin facilitates the management and maintenance of the MySQL database. PhpMyAdmin provides an easy way to use graphic interface to write and execute queries, manage users and databases, to export and import data.

For easier management of MySQL Database, we are going to installed phpMyAdmin

**Step 1.** Download PhpMyAdmin from here https://www.phpmyadmin.net/downloads/

![7. Installing PhpMyAdmin in Windows Server – step 1](images/25-step-1.png)

**Step 2.** After downloading the zip file Extract the files from the archive to phpMyAdmin folder (C:\inetpub\wwwroot\phpMyAdmin).

![7. Installing PhpMyAdmin in Windows Server – step 2](images/26-step-2.png)

**Step 3.** To access phpMyAdmin you should give full rights (C:\inetpub\wwwroot\phpmyadmin).

![7. Installing PhpMyAdmin in Windows Server – step 3](images/27-step-3.png)

**Step 4.** After Installation of phpMyAdmin, open a browser and check browser for http://localhost/phpmyadmin/ and you will see a window like this:

![7. Installing PhpMyAdmin in Windows Server – step 4](images/28-step-4.png)

## 8. Configure wp-config.php

The wp-config-sample.php file contains the database information and tells the WordPress application which database to pull information from. This step must be completed to ensure the correct database information is associated with the WordPress installation.

The wp-config-sample.php file can be found in folder where WordPress is installed. To modify the file:

Go to folder where WordPress is installed From the folder, open wp-config-sample.php in a text editor Right click on the file, select Rename and change the name of the file to wp-config.php. Right-click on the wp-config.php file and select Code Edit. When the file opens, look for the following information:

```php
define('DB_NAME', 'database_name_here');
/** MySQL database username */
define('DB_USER', 'username_here');
/** MySQL database password */
define('DB_PASSWORD', 'password_here');
```

Replace database_name_here with the name of the database you created (above in step). Replace username_here with the username of the database you created. Replace password_here with the password of the database that you created. When done editing, click the Save Changes button, then close the file.

## 9. Using phpMyAdmin Create Database

If your web server has phpMyAdmin installed, you may follow these instructions to create your WordPress username and database. If you work on your own computer, on most Linux distributions you can install PhpMyAdmin automatically.

**Step 1.** Choose a name for your WordPress database: ‘WordPress’ Enter the chosen database name in the Create database field and choose the best collation for your language and encoding. In most cases it’s better to choose in the “utf8_” series and, if you don’t find your language, to choose “utf8mb4_general_ci”

![9. Using phpMyAdmin Create Database – step 1](images/29-step-1.png)

**Step 2.** Click the PhpMyAdmin icon in the upper left to return to the main page, then click the Users tab. If a user relating to WordPress does not already exist in the list of users, create one:

![9. Using phpMyAdmin Create Database – step 2](images/30-step-2.png)

**Step 3.** Click Add user.

**Step 4.** Choose a username for WordPress (‘wordpress‘ is good) and enter it in the User name field. (Be sure Use text field: is selected from the dropdown.)

**Step 5.** Choose a secure password (ideally containing a combination of upper- and lower- case letters, numbers, and symbols), and enter it in the Password field. (Be sure Use text field: is selected from the dropdown.) Re-enter the password in the Re-type field.

**Step 6.** Write down the username and password you chose.

![9. Using phpMyAdmin Create Database – step 6](images/31-step-6.png)

**Step 7.** Leave all options under Global privileges at their defaults.

**Step 8.** Click Go.

**Step 9.** Return to the Users screen and click the Edit privileges icon on the user you’ve just created for WordPress.

**Step 10.** In the Database-specific privileges section, select the database you’ve just created for WordPress under the Add privileges to the following database dropdown, and click Go.

**Step 11.** The page will refresh with privileges for that database. Click Check All to select all privileges, and click Go.

**Step 12.** On the resulting page, make note of the host name listed after Server: at the top of the page. (This will usually be localhost.)

![9. Using phpMyAdmin Create Database – step 12](images/32-step-12.png)

---
[Web Server (IIS)](../README.md)
