TimeWise-Web-App-Testing

Welcome to the TestWise Web Application Testing repository. This repository contains all the information and documentation related to the manual testing of the Story Spoil web application based on the provided Software Requirements Specification (SRS) document.

Overview
The primary objective of this testing effort is to ensure that the TimeWise web application functions as expected according to the provided use cases outlined in the SRS document. This involves creating manual test cases for each use case and identifying and documenting any bugs or issues that are discovered during the testing process.

Software Requirements
Introduction
Purpose
The objective of this document is to provide a description of the TimeWise application (also referred to as The App). It will present an overview of the key functionalities.	

Scope
This document includes high-level descriptions of the basic functionalities of The App, such as user registration, login, profile editing, task creation and management. It does not cover any special user (Administrator) functionalities.


Functional Requirements:

Use Case 1 (Landing Page)
Users should be able to access the TimeWise app from its designated URL via the Internet, which should load the Landing Page. The page should display the "Optimize Your Time Now!" button, which directs to the Login/Register page. Optionally, the usershould be able to view the "10 Time Management Tips to Boost Your Productivity" video by clicking the provided link.

Use Case 2 (User Registration)
	
From the Registration/Login page visitors should be able to navigate to the Registration form and successfully register. This involves filling out fields for First Name, Middle Name, Last Name, Username, Email, Password, and Repeat Password, along with agreeing to the Terms of Service.

Use Case 3 (User Login)
	
From the Registration/Login page visitors should be able to log in using the Login form by entering their Username or Email and Password. The form should also offer a "Remember Me" option and a "Forgot Password" link for password recovery.

Use Case 4 (Home Page and Navigation)
Logged-in users should arrive at the Home Page, featuring a Navbar with a Home Page link and a User Profile Icon. The Sidebar Menu should provide access to the task boards: "To-Do," "In Progress," and "Done. Users should have the ability to navigate across different sections of the app through the Sidebar Menu and should be able to log out of the app using the "Logout" button.

Use Case 5 (Profile Management)
Once logged in, users should be able to view and edit their profile information from the Navbar's Profile Icon dropdown menu. This includes updating their First Name, Middle Name, Last Name, and Avatar Picture (via URL).

Use Case 6 (Task Creation and Management)
Logged-in users should be able to navigate to the "To-do" board and create a new task by clicking the "CREATE TASK" button and entering the required information in the form fields. Upon creation, the task should appear on the appropriate board based on its status.
For any task, users should be able to view detailed information, edit the task's contents, or delete the task. This includes modifying the task's name, description, and start/end dates. Users also should be able to update the status of tasks between the "To-do," "In Progress," and "Done" boards. 

Testing Process

Test Cases

All test cases created for the TimeWise Web Application are documented in the 'Test Cases' directory of this repository. Each test case is designed to validate a specific functionality or use case described in the SRS document. --> [Test-Management-and-Bug-Tracker-Template-Aleksandar-Marinov.xlsx](https://github.com/Aleksmarinov/TimeWise-WebApp/files/14584485/Test-Management-and-Bug-Tracker-Template-Aleksandar-Marinov.xlsx)


API Testing with Postman: TimeWise API: 

This section provides information about the TimeWise Api endpoints and their functionalities. It serves as a guide to understand how to interact with the TimeWise API. 


Contact

For any questions or clarifications regarding the testing process, you can reach out to Aleksandar at aleksandarmarinov97@gmail.com
