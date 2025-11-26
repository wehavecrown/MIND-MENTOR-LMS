# 📚 MindMentor: A Learning Management System

**MindMentor** is a web-based Learning Management System (LMS) designed to facilitate a streamlined educational experience for instructors and students. Built on the **PHP CodeIgniter framework**, the platform enables instructors to easily create and manage courses, upload content, and oversee student enrollment, while providing students with a centralized hub for accessing course materials.

-----

## ✨ Features

  * **Role-Based Access Control (RBAC):** Distinct interfaces and privileges for **Administrator**, **Instructor**, and **Student** roles.
  * **Course Management:** Instructors can create, edit, and publish courses.
  * **Content Delivery:** Instructors can upload and organize various lesson materials (e.g., PDF, documents, media links).
  * **Student Enrollment:** Students can browse available courses and enroll, and Instructors can manage their class roster.
  * **Centralized Dashboards:** Dedicated dashboards for each user role to manage relevant tasks and view enrolled courses.
  * **Security:** Implements CodeIgniter's built-in security features, including secure password hashing and input sanitization, to protect data in the MySQL database.
  * **Responsive Design:** Utilizes **Bootstrap 5** for a mobile-friendly and intuitive user interface.

-----

## 💻 Technologies Used

| Category | Technology | Version / Stack |
| :--- | :--- | :--- |
| **Backend Framework** | PHP CodeIgniter | 3.x |
| **Server Environment** | PHP | 7.4+ |
| **Database** | MySQL | 5.6+ |
| **Frontend** | HTML5, CSS3, JavaScript | Bootstrap 5 |
| **Local Environment** | XAMPP | Latest Stable |

-----

## ⚙️ Local Setup (Using XAMPP)

To run MindMentor locally, you will need a running web server environment with PHP and MySQL support. We recommend using **XAMPP**.

### Prerequisites

1.  **XAMPP:** Download and install the latest stable version of [XAMPP](https://www.apachefriends.org/index.html).
2.  **Web Browser:** Any modern web browser (Chrome, Firefox, Edge).

### Installation Steps

#### 1\. Database Setup (MySQL/phpMyAdmin)

1.  Start the **Apache** and **MySQL** services from the XAMPP Control Panel.
2.  Open your web browser and navigate to `http://localhost/phpmyadmin`.
3.  Click **New** on the left sidebar to create a new database.
4.  Name the database (e.g., `mindmentor_lms`).
5.  Import your database structure:
      * Click on the newly created database.
      * Go to the **Import** tab.
      * Select the SQL file provided with the project (e.g., `mindmentor_db.sql`) and click **Go**.

#### 2\. Project File Configuration

1.  Navigate to your XAMPP installation directory (usually `C:\xampp`).

2.  Place the entire MindMentor project folder inside the **`htdocs`** directory (e.g., `C:\xampp\htdocs\mindmentor`).

3.  **Configure Database Connection:**

      * Open the CodeIgniter configuration file, typically found at `application/config/database.php`.
      * Update the following lines to match your database settings:

    <!-- end list -->

    ```php
    $db['default'] = array(
        // ...
        'hostname' => 'localhost',
        'username' => 'root', // XAMPP default
        'password' => '',     // XAMPP default (leave blank)
        'database' => 'mindmentor_lms', // Name you created in Step 1.4
        // ...
    );
    ```

#### 3\. Base URL Configuration

1.  Open the main configuration file: `application/config/config.php`.

2.  Update the `$config['base_url']` setting to match your local project path:

    ```php
    $config['base_url'] = 'http://localhost/mindmentor/';
    ```

#### 4\. Access the Application

1.  Ensure Apache and MySQL services are still running in XAMPP.
2.  Open your web browser and navigate to: `http://localhost/mindmentor/`

-----

## 🚀 Usage Guide

### Instructor Workflow

1.  **Login:** Log in with your Instructor credentials.
2.  **Course Creation:** Navigate to the **Course Module** to create a new course by providing a title and description.
3.  **Content Upload:** Use the Course Management interface to upload lesson materials (Lessons Controller) that students can view.
4.  **Student Management:** View the enrollment roster for your courses, and manually enroll/unenroll students as needed.

### Student Workflow

1.  **Login:** Log in with your Student credentials.
2.  **Browse & Enroll:** Visit the **Available Courses** page to view the catalog. Click the **Enroll** button on the desired course.
3.  **View Content:** Access your **Dashboard** to see enrolled courses, and click to view the uploaded lesson materials.
