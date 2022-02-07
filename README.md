# Touchless Interactive Information Kiosk for Leyte Normal University

Detailed installation instruction for the system. The touchless feature was made possible by [MediaPipe Hands Model](https://google.github.io/mediapipe/solutions/hands)

## Software Requirements
1. [Xampp/Wampp](https://www.apachefriends.org/download.html)
 - PHP 8.0^
2. [Composer](https://getcomposer.org/Composer-Setup.exe)
3. [Node](https://nodejs.org/en/download/) 

## Minimum Hardware Requirements (Based on testing for different hardwares)
1. Intel Core i5 11th Gen and above
2. Atleast 8GB RAM
3. NVIDIA Video Card Geoforce GTX 1060 (Optional but recommended for better performance)

## How to run this system
1. Navigate to capstone-fe (Management System) folder then open a terminal / command prompt and run the following command
```bash

 #Install dependencies
 > npm install
 
 #To run
 > npm run serve
 
 #To access check the url given after running the npm run serve command
 
 ```

2. Create a database on localhost/phpmyadmin called 'touchless-info-kiosk'
 2.1 Navigate to capstone-be (Laravel - Backend) folder then open a terminal / command prompt and run the following command and open in the browser 
```bash

 #Install dependencies
 > npm install
 > composer install 
 
 #If an error occurs for the composer install run the following command
 > composer install --ignore-platform-reqs
 
 #Migrate and Seed the Database
 > php artisan migrate --seed
 
 #Run the JWT Token (Tymon JWT was used for this system)
 > php artisan jwt:secret
 
 #To run
 > php artisan serve
 
 #To access check the url given after running the npm run serve command and open in the browser
 
```

## Checkout the .env file for the configuration of the Laravel Project (capstone-be)
    - DATABASE
	  - DB_CONNECTION up to DB_PASSWORD
	- EMAIL SERVICE - An error may occur for the approval/creation of account if this was not set properly
	  - MAIL_MAILER up to MAIL_FROM_NAME