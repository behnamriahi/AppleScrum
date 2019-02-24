**Applescrum** is a free, open source, flexible project management web application written using CakePHP.

#### Requirements
    * Apache with `mod_rewrite`
    	* Enable curl in php.ini
    	* Change the 'post_max_size' and `upload_max_filesize` to 200Mb in php.ini
    * PHP 5.3 or higher
    * MySQL 4.1 or higher
		* If STRICT mode is On, turn it Off.

#### Installation
    * Extract the archive. Upload the extracted folder(applescrum-master) to your working directory.
    * Provide proper write permission to "app/Config", "app/tmp" and "app/webroot" folders and their sub-folders.
	Ex. chmod -R 0777 app/Config, chmod -R 0777 app/tmp, chmod -R 0777 app/webroot
	You can change the write permission of "app/Config" folder after installation procedure is completed.
    * Create a new MySQL database named "applescrum"(`utf8_unicode_ci` collation).
    * Get the database.sql file from the root directory and import that to your database.
    * Locate your `app` directory, do the changes on following files:
	  * `app/Config/database.php` - We have already updated the database name as "Applescrum" which you can change at any point. In order to change it, just create a database using any name and update that name as database in DATABASE_CONFIG section. And also you can set a password for your Mysql login which you will have to update in the same page as password. [Required]
	  * `app/Config/constants.php` - Provide your valid SMTP_UNAME and SMTP_PWORD. For SMTP email sending you can use(Only one at a time) either Gmail or Sendgrid or Mandrill. By default we are assuming that you are using Gmail, so Gmail SMTP configuration section is uncommented. If you are using Sendgrid or Mandrill just comment out the Gmail section and uncomment the Sendgrid or Mandrill configuration section as per your requirement. [Required]
	  * `app/Config/constants.php` - Update the FROM_EMAIL_NOTIFY and SUPPORT_EMAIL [Required]
    * Run the application as http://your-site.com/ from your browser and start using Applescrum
    
