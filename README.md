# eshop - Educational E-commerce Web Application

## Overview
Welcome to **eshop**, an educational e-commerce platform developed using HTML, CSS, PHP, and JavaScript. This repository contains a comprehensive solution intended for educational purposes. Feel free to use this application by copying and pasting the code.

## Main Features
- **Intuitive Interface:** User-friendly design ensuring easy navigation and a pleasant browsing experience.
- **Extensive Product Showcase:** Comprehensive catalog displaying various products with detailed descriptions and high-resolution images.
- **Efficient Shopping Cart:** Convenient cart system enabling users to manage selected items before making a purchase.
- **Secure Payment Processing:** Reliable payment gateway integration ensuring the security of transactions.
- **Responsive Design:** Compatibility across devices, guaranteeing accessibility on desktops, tablets, and mobile phones.
- **Backend Functionality:** Powerful PHP backend for efficient management of orders, inventory, and user accounts.

## Technologies Utilized
- HTML
- CSS
- PHP
- JavaScript

## Usage Instructions

1. Clone this repository to your local machine.
2. Replace the database connection details in the `connection.php` file with your own database credentials:
    ```php
    Database::$connection = new mysqli("localhost", "root", "[your_db_password]", "eshop", "[port_number]");
    ```

3. Modify the `forgotPasswordProcess.php` file with your SMTP configuration and email details:
    Replace the existing code in `forgotPasswordProcess.php` with the following, using your own email settings:
    ```php
    $mail = new PHPMailer;
    $mail->IsSMTP();
    $mail->Host = 'smtp.gmail.com';
    $mail->SMTPAuth = true;
    $mail->Username = '[Your Email]';
    $mail->Password = '[Your App Key]';
    $mail->SMTPSecure = 'ssl';
    $mail->Port = 465;
    $mail->setFrom('[Your Email]');
    $mail->addReplyTo('[Your Email]');
    $mail->addAddress($email);
    $mail->isHTML(true);
    $mail->Subject = 'eShop Forgot password Verification Code';
    $bodyContent = '<h1 style="color:green;">Your Verification Code is '.$code.'</h1>';
    $mail->Body    = $bodyContent;
    ```

4. Ensure to replace `[Your Email]` and `[Your App Key]` with your actual email and application key respectively in the `forgotPasswordProcess.php` file.
5. Save the changes to the `forgotPasswordProcess.php` file after updating the SMTP configuration and email details.
6. Continue with any other necessary configuration or setup steps as mentioned in the repository documentation for smooth operation.

## Contributions Welcome
Feel free to contribute by suggesting enhancements, reporting issues, or submitting pull requests to further improve eshop.
