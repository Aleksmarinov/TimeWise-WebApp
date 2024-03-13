[Exam.postman_collection.json](https://github.com/Aleksmarinov/TimeWise-WebApp/files/14584501/Exam.postman_collection.json)TimeWise-Web-App-Testing

Welcome to the TestWise Web Application Testing repository. This repository contains all the information and documentation related to the manual testing of the Story Spoil web application based on the provided Software Requirements Specification (SRS) document.

Overview
The primary objective of this testing effort is to ensure that the TimeWise web application functions as expected according to the provided use cases outlined in the SRS document. This involves creating manual test cases for each use case and identifying and documenting any bugs or issues that are discovered during the testing process.

Software Requirements
1. Introduction
1.1. Purpose
The objective of this document is to provide a description of the TimeWise application (also referred to as The App). It will present an overview of the key functionalities.	

1.2. Scope
This document includes high-level descriptions of the basic functionalities of The App, such as user registration, login, profile editing, task creation and management. It does not cover any special user (Administrator) functionalities.


Functional Requirements 

1.	Use Case 1 (Landing Page)
Users should be able to access the TimeWise app from its designated URL via the Internet, which should load the Landing Page. The page should display the "Optimize Your Time Now!" button, which directs to the Login/Register page. Optionally, the usershould be able to view the "10 Time Management Tips to Boost Your Productivity" video by clicking the provided link.

2.	Use Case 2 (User Registration)
	
From the Registration/Login page visitors should be able to navigate to the Registration form and successfully register. This involves filling out fields for First Name, Middle Name, Last Name, Username, Email, Password, and Repeat Password, along with agreeing to the Terms of Service.
3.	Use Case 3 (User Login)
	
From the Registration/Login page visitors should be able to log in using the Login form by entering their Username or Email and Password. The form should also offer a "Remember Me" option and a "Forgot Password" link for password recovery.

4.	Use Case 4 (Home Page and Navigation)
Logged-in users should arrive at the Home Page, featuring a Navbar with a Home Page link and a User Profile Icon. The Sidebar Menu should provide access to the task boards: "To-Do," "In Progress," and "Done. Users should have the ability to navigate across different sections of the app through the Sidebar Menu and should be able to log out of the app using the "Logout" button.

5. Use Case 5 (Profile Management)
Once logged in, users should be able to view and edit their profile information from the Navbar's Profile Icon dropdown menu. This includes updating their First Name, Middle Name, Last Name, and Avatar Picture (via URL).

6. Use Case 6 (Task Creation and Management)
Logged-in users should be able to navigate to the "To-do" board and create a new task by clicking the "CREATE TASK" button and entering the required information in the form fields. Upon creation, the task should appear on the appropriate board based on its status.
For any task, users should be able to view detailed information, edit the task's contents, or delete the task. This includes modifying the task's name, description, and start/end dates. Users also should be able to update the status of tasks between the "To-do," "In Progress," and "Done" boards. 

Testing Process

Test Cases

All test cases created for the TimeWise Web Application are documented in the 'Test Cases' directory of this repository. Each test case is designed to validate a specific functionality or use case described in the SRS document. --> [Test-Management-and-Bug-Tracker-Template-Aleksandar-Marinov.xlsx](https://github.com/Aleksmarinov/TimeWise-WebApp/files/14584485/Test-Management-and-Bug-Tracker-Template-Aleksandar-Marinov.xlsx)


API Testing with Postman: TimeWise API:

This section provides information about the TimeWise Api endpoints and their functionalities. It serves as a guide to understand how to interact with the TimeWise API. --> 

[Uploading Exa{
	"info": {
		"_postman_id": "55b8bb2b-c2cf-47f9-b41b-a99d576ee47d",
		"name": "Exam Copy",
		"schema": "https://schema.getpostman.com/json/collection/v2.1.0/collection.json",
		"_exporter_id": "29092381"
	},
	"item": [
		{
			"name": "Supported-Methods",
			"request": {
				"method": "GET",
				"header": [],
				"url": {
					"raw": "http://timewise2-env.eba-mkmm3jwy.eu-north-1.elasticbeanstalk.com/api",
					"protocol": "http",
					"host": [
						"timewise2-env",
						"eba-mkmm3jwy",
						"eu-north-1",
						"elasticbeanstalk",
						"com"
					],
					"path": [
						"api"
					]
				}
			},
			"response": []
		},
		{
			"name": "Create User",
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\r\n    \"userName\": \"AleksMarinov146\",\r\n    \"firstName\": \"Aleksandar\",\r\n    \"midName\": \"Mihaylov\",\r\n    \"lastName\": \"Marinov\",\r\n    \"email\": \"aleksmarinov14@6test.com\",\r\n    \"password\": \"123456\",\r\n    \"rePassword\": \"123456\"\r\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "http://timewise2-env.eba-mkmm3jwy.eu-north-1.elasticbeanstalk.com/api/User/Register",
					"protocol": "http",
					"host": [
						"timewise2-env",
						"eba-mkmm3jwy",
						"eu-north-1",
						"elasticbeanstalk",
						"com"
					],
					"path": [
						"api",
						"User",
						"Register"
					]
				}
			},
			"response": []
		},
		{
			"name": "Authorization",
			"request": {
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\r\n    \"email\": \"aleksmarinov14@6test.com\",\r\n    \"password\": \"123456\"\r\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "http://timewise2-env.eba-mkmm3jwy.eu-north-1.elasticbeanstalk.com/api/User/Authorization",
					"protocol": "http",
					"host": [
						"timewise2-env",
						"eba-mkmm3jwy",
						"eu-north-1",
						"elasticbeanstalk",
						"com"
					],
					"path": [
						"api",
						"User",
						"Authorization"
					]
				}
			},
			"response": []
		},
		{
			"name": "Create task",
			"request": {
				"auth": {
					"type": "bearer",
					"bearer": [
						{
							"key": "token",
							"value": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiJKd3RTZXJ2aWNlQWNjZXNzVG9rZW4iLCJqdGkiOiIwYTAwNDY2My03YmQ4LTRmNmEtYWRkZi1mZDI4OTMwNWQ5NGQiLCJpYXQiOiIxMi8xNi8yMDIzIDEwOjU3OjM5IEFNIiwiVXNlcklkIjoiNzAzYzE0MjEtNDJlNy00YjE5LTljNDYtYjM0ZTUwNjM5MGMwIiwiRW1haWwiOiJhbGVrc21hcmlub3YxNEA2dGVzdC5jb20iLCJVc2VyTmFtZSI6IkFsZWtzTWFyaW5vdjE0NiIsImV4cCI6MTcwMjc0NTg1OSwiaXNzIjoiVGltZVdpc2VfQXBwX1NvZnRVbmkiLCJhdWQiOiJUaW1lV2lzZV9XZWJBUElfU29mdFVuaSJ9.Iwzs4MLCVAzA3fCaiDD2-RvCGmxW7kFhnl3mzjdiNng",
							"type": "string"
						}
					]
				},
				"method": "POST",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\r\n    \"taskName\": \"testing-task-2023\",\r\n    \"startDate\": \"16/12/2023 12:58\",\r\n    \"endDate\": \"18/12/2023 12:00\",\r\n    \"description\": \"Task description for my exam at SoftUni-testing\",\r\n    \"status\": \"ToDo\"\r\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "http://timewise2-env.eba-mkmm3jwy.eu-north-1.elasticbeanstalk.com/api/Task/Create",
					"protocol": "http",
					"host": [
						"timewise2-env",
						"eba-mkmm3jwy",
						"eu-north-1",
						"elasticbeanstalk",
						"com"
					],
					"path": [
						"api",
						"Task",
						"Create"
					]
				}
			},
			"response": []
		},
		{
			"name": "Get All Tasks",
			"protocolProfileBehavior": {
				"disableBodyPruning": true
			},
			"request": {
				"auth": {
					"type": "bearer",
					"bearer": [
						{
							"key": "token",
							"value": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiJKd3RTZXJ2aWNlQWNjZXNzVG9rZW4iLCJqdGkiOiIzODNjNDc4OC1hZjRlLTRlOWEtYmY0MS0yMmVlM2UzNzJiN2QiLCJpYXQiOiIxMi8xNi8yMDIzIDExOjAwOjE3IEFNIiwiVXNlcklkIjoiNzAzYzE0MjEtNDJlNy00YjE5LTljNDYtYjM0ZTUwNjM5MGMwIiwiRW1haWwiOiJhbGVrc21hcmlub3YxNEA2dGVzdC5jb20iLCJVc2VyTmFtZSI6IkFsZWtzTWFyaW5vdjE0NiIsImV4cCI6MTcwMjc0NjAxNywiaXNzIjoiVGltZVdpc2VfQXBwX1NvZnRVbmkiLCJhdWQiOiJUaW1lV2lzZV9XZWJBUElfU29mdFVuaSJ9.JqqflAKmv6wdcbj6TL6t5WBRM4kxc6BMsewloS65fKg",
							"type": "string"
						}
					]
				},
				"method": "GET",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "http://timewise2-env.eba-mkmm3jwy.eu-north-1.elasticbeanstalk.com/api/Task/AllTasks?where=&caseSensitive=false&optional=true&values=[\"todo\", \"inprogress\", \"done\"]",
					"protocol": "http",
					"host": [
						"timewise2-env",
						"eba-mkmm3jwy",
						"eu-north-1",
						"elasticbeanstalk",
						"com"
					],
					"path": [
						"api",
						"Task",
						"AllTasks"
					],
					"query": [
						{
							"key": "where",
							"value": ""
						},
						{
							"key": "caseSensitive",
							"value": "false"
						},
						{
							"key": "optional",
							"value": "true"
						},
						{
							"key": "values",
							"value": "[\"todo\", \"inprogress\", \"done\"]"
						},
						{
							"key": "",
							"value": "",
							"disabled": true
						},
						{
							"key": "",
							"value": "",
							"disabled": true
						}
					]
				}
			},
			"response": []
		},
		{
			"name": "Count All Tasks",
			"request": {
				"auth": {
					"type": "bearer",
					"bearer": [
						{
							"key": "token",
							"value": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiJKd3RTZXJ2aWNlQWNjZXNzVG9rZW4iLCJqdGkiOiIzODNjNDc4OC1hZjRlLTRlOWEtYmY0MS0yMmVlM2UzNzJiN2QiLCJpYXQiOiIxMi8xNi8yMDIzIDExOjAwOjE3IEFNIiwiVXNlcklkIjoiNzAzYzE0MjEtNDJlNy00YjE5LTljNDYtYjM0ZTUwNjM5MGMwIiwiRW1haWwiOiJhbGVrc21hcmlub3YxNEA2dGVzdC5jb20iLCJVc2VyTmFtZSI6IkFsZWtzTWFyaW5vdjE0NiIsImV4cCI6MTcwMjc0NjAxNywiaXNzIjoiVGltZVdpc2VfQXBwX1NvZnRVbmkiLCJhdWQiOiJUaW1lV2lzZV9XZWJBUElfU29mdFVuaSJ9.JqqflAKmv6wdcbj6TL6t5WBRM4kxc6BMsewloS65fKg",
							"type": "string"
						}
					]
				},
				"method": "GET",
				"header": [],
				"url": {
					"raw": "http://timewise2-env.eba-mkmm3jwy.eu-north-1.elasticbeanstalk.com/api/Task/Count",
					"protocol": "http",
					"host": [
						"timewise2-env",
						"eba-mkmm3jwy",
						"eu-north-1",
						"elasticbeanstalk",
						"com"
					],
					"path": [
						"api",
						"Task",
						"Count"
					]
				}
			},
			"response": []
		},
		{
			"name": "Edit task",
			"request": {
				"auth": {
					"type": "bearer",
					"bearer": [
						{
							"key": "token",
							"value": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiJKd3RTZXJ2aWNlQWNjZXNzVG9rZW4iLCJqdGkiOiIzODNjNDc4OC1hZjRlLTRlOWEtYmY0MS0yMmVlM2UzNzJiN2QiLCJpYXQiOiIxMi8xNi8yMDIzIDExOjAwOjE3IEFNIiwiVXNlcklkIjoiNzAzYzE0MjEtNDJlNy00YjE5LTljNDYtYjM0ZTUwNjM5MGMwIiwiRW1haWwiOiJhbGVrc21hcmlub3YxNEA2dGVzdC5jb20iLCJVc2VyTmFtZSI6IkFsZWtzTWFyaW5vdjE0NiIsImV4cCI6MTcwMjc0NjAxNywiaXNzIjoiVGltZVdpc2VfQXBwX1NvZnRVbmkiLCJhdWQiOiJUaW1lV2lzZV9XZWJBUElfU29mdFVuaSJ9.JqqflAKmv6wdcbj6TL6t5WBRM4kxc6BMsewloS65fKg",
							"type": "string"
						}
					]
				},
				"method": "PUT",
				"header": [],
				"body": {
					"mode": "raw",
					"raw": "{\r\n    \"taskName\": \"changed task-22\",\r\n    \"startDate\": \"20/01/2023 17:28\",\r\n    \"endDate\": \"27/01/2023 19:28\",\r\n    \"description\": \"This description has been changed from me\",\r\n    \"status\": \"InProgress\"\r\n}",
					"options": {
						"raw": {
							"language": "json"
						}
					}
				},
				"url": {
					"raw": "http://timewise2-env.eba-mkmm3jwy.eu-north-1.elasticbeanstalk.com/api/Task/Edit/67edbec5-4d3b-4b1a-f8f9-08dbfe2447cf",
					"protocol": "http",
					"host": [
						"timewise2-env",
						"eba-mkmm3jwy",
						"eu-north-1",
						"elasticbeanstalk",
						"com"
					],
					"path": [
						"api",
						"Task",
						"Edit",
						"67edbec5-4d3b-4b1a-f8f9-08dbfe2447cf"
					]
				}
			},
			"response": []
		},
		{
			"name": "Delete Task",
			"request": {
				"auth": {
					"type": "bearer",
					"bearer": [
						{
							"key": "token",
							"value": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiJKd3RTZXJ2aWNlQWNjZXNzVG9rZW4iLCJqdGkiOiIzODNjNDc4OC1hZjRlLTRlOWEtYmY0MS0yMmVlM2UzNzJiN2QiLCJpYXQiOiIxMi8xNi8yMDIzIDExOjAwOjE3IEFNIiwiVXNlcklkIjoiNzAzYzE0MjEtNDJlNy00YjE5LTljNDYtYjM0ZTUwNjM5MGMwIiwiRW1haWwiOiJhbGVrc21hcmlub3YxNEA2dGVzdC5jb20iLCJVc2VyTmFtZSI6IkFsZWtzTWFyaW5vdjE0NiIsImV4cCI6MTcwMjc0NjAxNywiaXNzIjoiVGltZVdpc2VfQXBwX1NvZnRVbmkiLCJhdWQiOiJUaW1lV2lzZV9XZWJBUElfU29mdFVuaSJ9.JqqflAKmv6wdcbj6TL6t5WBRM4kxc6BMsewloS65fKg",
							"type": "string"
						}
					]
				},
				"method": "DELETE",
				"header": [],
				"url": {
					"raw": "http://timewise2-env.eba-mkmm3jwy.eu-north-1.elasticbeanstalk.com/api/Task/Delete/67edbec5-4d3b-4b1a-f8f9-08dbfe2447cf",
					"protocol": "http",
					"host": [
						"timewise2-env",
						"eba-mkmm3jwy",
						"eu-north-1",
						"elasticbeanstalk",
						"com"
					],
					"path": [
						"api",
						"Task",
						"Delete",
						"67edbec5-4d3b-4b1a-f8f9-08dbfe2447cf"
					]
				}
			},
			"response": []
		}
	]
}m.postman_collection.json…]()


Contact

For any questions or clarifications regarding the testing process, you can reach out to Aleksandar at aleksandarmarinov97@gmail.com
