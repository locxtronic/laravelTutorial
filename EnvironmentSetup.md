## Setting Up The Environtment ##
 1. Laravel 5.5 required PHP 7 to run, therefore if you have older version PHP, please install the new PHP 7. **If you have working project in your htdocs directory, make sure you install the new Xampp in different directory** to make sure your current project not affected. Download and install Xampp, [Xampp with PHP 7 Download Here](https://www.apachefriends.org/xampp-files/7.1.9/xampp-win32-7.1.9-0-VC14-installer.exe)
 2. Download Composer and install it, choose default configuration during installation. [Composer download here](https://getcomposer.org/Composer-Setup.exe)
 3. Open command prompt (CMD) and type in `Composer`. You should see it print out Composer banner. This step is only to check and make sure Composer installed working correctly.
![Composer run in cmd](https://github.com/locxtronic/laravelTutorial/raw/master/img/2017-10-17.png)
 4. Run composer to install Laravel package by running this command, `composer global require "laravel/installer"` This will take a while depending on internet speed.
 5. To **create laravel new project**, change the command prompt directory to htdocs directory e.g `cd c:\xampp\htdocs\`and then run command `laravel new tutorProject`.
 6. **PLEASE BE PATIENT WHILE IT DOWNLOADING THE WHOLE INTERNET FOR YOU :-p**
![create laravel project](https://github.com/locxtronic/laravelTutorial/raw/master/img/2017-10-17%20%281%29.png)
 7. When the process is completed, please run **Apache** and **MySQL** in **Xampp** control panel.
 8. Now open up your browser and direct it to `localhost/tutorProject/public`. You should see Laravel is working like charm. ![enter image description here](https://github.com/locxtronic/laravelTutorial/raw/master/img/2017-10-17%20%283%29.png)
 9. Yes we are done now. Class dismiss. Pack your bag and go home.