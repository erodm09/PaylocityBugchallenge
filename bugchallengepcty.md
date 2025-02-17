
# Paylocity STE Assessment- Bug Challenge :bug: 🔍 


<details>

<summary>Bug 01- 405 error Occured as wrong  handling</summary>

## Description
Wrong error:  This page isnt working (HTTP 405 error message) is shown on the browser


The error message suggests the wrong handling as if there is a problem with the HTTP request as its responding 405. Instead of having just a simple message such as : Invalid username or password


## Steps To Reproduce

1.Go to the URL: https://wmxrwq14uc.execute-api.us-east-1.amazonaws.com/Prod/Account/Login

2.Enter invalid characters in the `Username` and `Password` fields

3.Click on the `Login` button


## Actual behavior
HTTP ERROR 405 This page is not working is displayed to the user. 

## Expected behavior
A message of Invalid username or password should be shown to the user to avoid confusion or proper error handling towards the UI.


## Priority
High

## Screenshots/Video
<img width="1091" alt="Screenshot 2025-02-16 at 22 51 41" src="https://github.com/user-attachments/assets/a3ad3ce4-cd96-4a97-9df5-c4988b7dd205" />



## Device Details:
Device: MacBook Pro (13-inch, M2, 2022) Chip M2
OS: MacOs
Version: Mac OS Sequoia Version 15.1
Browser : Version 131.0.6778.267 (Official Build) (arm64)
Resolution [2560 × 1600]

Additional context
Add any other context about the problem here

</details> 

<details>

<summary>Bug 02- User credentials not clearing after User fails to loging and goes back</summary>


## Description
After a user inputs an incorrect password(with a valid user) during the login process and then inputs incorrect password or username, and proceeds to login after the error displayed, to rectify it by going back and refreshing the page, the initial error message persists about the missing username or password .

## Steps To Reproduce

1.Navigate to the login page at https://wmxrwq14uc.execute-api.us-east-1.amazonaws.com/Prod/Account/Login 

2.Input an incorrect `password` with a correct `Username` 

3.Click the `login` button.

4. Input an incorrect `password` and incorrect `Username`  or leave it black
5. Click the `login` button.
6. .Observe the displayed error message described in `Bug-01`.
7. Click on the Back button on the Browser

6.Refresh the page using the browser's refresh button or shortcut (e.g., F5 or Ctrl + R).

7.Observe that the initial error message remains unchanged.


## Actual behavior
The message of a missing password or username is still showing. Indicating that there is not a proper session handling in place for the application as past errors are still being shown.

## Expected behavior
Even after refreshing the page, the initial error message indicating an incorrect or missing password continues to be displayed, which could cause user confusion and potentially impact the user experience.

## Priority
Medium

## Screenshots/Video

https://github.com/user-attachments/assets/37a26a6a-dc97-4812-8b74-469ca9cad619



## Device Details:

OS: MacOs
Version: Mac OS Sequoia Version 15.1
Browser : Chrome Version 115.0.5790.170 (Official Build) (arm64)
Resolution [2560 × 1600]

</details>

<details>

<summary>Bug 03- Paylocity Benefits Dashboard link available and shown to user after clicking</summary>


## Description
When a user clicks the “Paylocity Benefits Dashboard” link in the navigation bar, the link remains visible and does not change state, even though the user is already on the Benefits Dashboard page.
## Steps To Reproduce

1. Go to the following website link to Login at https://wmxrwq14uc.execute-api.us-east-1.amazonaws.com/Prod/Account/Login
2.On the upper left corner click on the Paylocity Benefits Dashboard message link.
3. Note that no login credentials are required to access the dashboard.
Observe that the form to add dependents is accessible and can be interacted with.

## Actual behavior
1. The Paylocity Benefits Dashboard is accessible without requiring login credentials.
2.Users can interact with the form to try and add dependents without proper authentication or employee data.

## Expected behavior
1.The Paylocity Benefits Dashboard should require proper login credentials before allowing access.
2.Users should only be able to interact with the form and access data if they are authenticated and authorized users.
3.Unauthorized users should not have access to any functionality of the dashboard.

## Priority
Medium

## Screenshots/Video


https://github.com/user-attachments/assets/38e3d6ec-be9b-4064-9893-f2dd37f3ab18



## Device Details:

OS: MacOs
Version: Mac OS Sequoia Version 15.1
Browser : Chrome Version 115.0.5790.170 (Official Build) (arm64)
Resolution [2560 × 1600]

</details>

<details>

<summary>Bug 04- No Error Message when inputing larger than required characters on First Name</summary>


## Description
When attempting to input larger than required characters in the "First Name" field during the process of adding or editing an employee on the Benefits Dashboard application, no error message is displayed, and the application allows the user to proceed without any indication of the input exceeding the limit.

## Steps To Reproduce

1.Open the Benefits Dashboard application on the following link https://wmxrwq14uc.execute-api.us-east-1.amazonaws.com/Prod/Account/Login

2. Login using valid credentials for Username and Password. 

3.Navigate to the section where you can add an employee by clicking on `Add Employee` button

3.In the "First Name" field, input a string of characters that is longer than the specified limit (e.g., more than 50 characters).

4.Attempt to proceed by clicking the "Save" or "Submit" button

## Actual behavior
No error message is shown, and the application doesnt let the user know that is inputing a wrong field

## Expected behavior
An error message should be displayed on the UI, indicating that the input for the "First Name" field exceeds the allowed character limit.

## Priority
Low

## Screenshots/Video





https://github.com/user-attachments/assets/123e4a47-1763-4574-b917-3cb5e151795a







## Device Details:

OS: MacOs
Version: Mac OS Sequoia Version 15.1
Browser : Chrome Version 115.0.5790.170 (Official Build) (arm64)
Resolution [2560 × 1600]

</details>

<details>

<summary>Bug 05-Duplicate Employee Addition with Same Details is allowed</summary>


## Description

The current version of the application permits the addition of an employee with the exact same First Name, Last Name, and Dependents as an existing entry. This oversight leads to the creation of duplicate employee records within the system, causing potential data inconsistency and confusion.


## Pre-condition

Have an existing user with valid First Name, Last Name and Dependent.


## Steps To Reproduce

1.Go to link for the application to login at https://wmxrwq14uc.execute-api.us-east-1.amazonaws.com/Prod/Account/Login

2.Enter valid details for Username and password and click on the Login button

2.Click on the `Add Employee` button

3.Input the same First Name, Last Name, and Dependents as an already existing employee.

4.Proceed with adding the employee by clicking on the Save button

## Actual behavior
No error message is shown, and the application doesnt let the user know that he/she is adding a Duplicat or existing user

## Expected behavior
An error message should be displayed on the UI, indicating that the entered user already exists to Try agian.

## Priority
High

## Screenshots/Video



https://github.com/user-attachments/assets/c31d386b-0169-46b1-af29-ac30342db645



## Device Details:

OS: MacOs
Version: Mac OS Sequoia Version 15.1
Browser : Chrome Version 115.0.5790.170 (Official Build) (arm64)
Resolution [2560 × 1600]

</details>


<details>

<summary>Bug 06-First Name and Last Name Displayed Incorrectly in Employee Table</summary>


## Description

When a user adds a new employee by filling in the First Name, Last Name, and Dependents fields in the form, the employee is successfully added. However, in the table displaying the list of employees, 
the First Name and Last Name appear swapped (i.e., the First Name is displayed in the Last Name column and vice versa).

## Pre-condition



## Steps To Reproduce

1.Go to link for the application to login at https://wmxrwq14uc.execute-api.us-east-1.amazonaws.com/Prod/Account/Login

2.Enter valid details for Username and password and click on the Login button

2.Click on the `Add Employee` button

3.Input the same First Name, Last Name, and Dependents accordingly

4.Proceed with adding the employee by clicking on the `Add button`


## Actual behavior
See the table on the dashboard that is shown where the First name entered for the new employee is shown as Last Name.

## Expected behavior
The First Name should be displayed under the “First Name” column.
The Last Name should be displayed under the “Last Name” column. 

 # Priority
High

## Screenshots/Video




https://github.com/user-attachments/assets/c3e1581d-3e53-4a58-ae52-d2f1d7282334





## Device Details:

OS: MacOs
Version: Mac OS Sequoia Version 15.1
Browser : Chrome Version 115.0.5790.170 (Official Build) (arm64)
Resolution [2560 × 1600]

</details>

<details>

<summary>Bug 07-API - Error Sending POST Request with Invalid String on dependent field</summary>


## Description

While using Postman to send a POST request to add a New employee, a 405 error is encountered when an invalid string value is provided as the dependent's field. The application should handle and validate input data to prevent the addition of invalid or incorrect values.


## Pre-condition

Have the valid Postman collection imported in Postman


## Steps To Reproduce

1. Launch Postman and access the QA Challenge- Master collection
2. Go to the POST request `Add Employee` for adding a new Employee.
3. On the Depndent field enter an invalid string (e.g., "X") as the dependent's number information.
4. Click on the Send button to send the POST request.

## Actual behavior
The server responds with a 405 Method Not Allowed error instead of handling the invalid input. The API does not return a clear validation error message
 indicating that the Dependents field contains invalid data.
## Expected behavior
When sending a POST request via Postman to add a new employee, if an invalid string value is provided in the Dependents field, 
the application should properly handle the input validation and return a meaningful error response.

Also the following would be expected:

-The API should validate the input before processing the request.
-If an invalid string is provided in the Dependents field, the API should return a 400 Bad Request status code instead of a 405 Method Not Allowed.
- The response body should include a clear error message, such as:   "error": "Invalid input: Dependents field must be a numeric value."

## Priority
Medium

## Screenshots/Video

<img width="1041" alt="Screenshot 2025-02-17 at 15 30 38" src="https://github.com/user-attachments/assets/68b93285-c6c2-4b40-ad85-76f82aa88241" />



## Device Details:
Postman Version: 10.17.3-230823-0523
OS: MacOs 15.1
Version: Mac OS Sequoia Version 15.1
Browser : Chrome Version 115.0.5790.170 (Official Build) (arm64)
Resolution [2560 × 1600]

</details>

<details>

<summary>Bug 08-API - 405 Error with Invalid ID in PUT Request Body for Employee Updated</summary>


## Description

When attempting to update an employee's information using a PUT request, an error is encountered due to an invalid ID being provided in the request body. The application should handle and validate input data to ensure that only valid IDs are accepted for updates


## Pre-condition

Have the valid Postman collection imported in Postman


## Steps To Reproduce

1. Launch Postman and access the QA Challenge- Master collection
2. Go to the PUT request `Update Employee` for editing an Employee.
3. On the Request body include an invalid ID value of a user.( i.e // or other characters)
4. Click on the Send button to send the PUT request.


## Actual behavior
The application accepts the PUT request with an invalid ID value in the request body.The server responds with a 405 error message saying method not allowed.

## Expected behavior
The application should validate the provided ID to ensure that it is a valid and existing employee ID.If an invalid ID is detected in the request body, the application should return a clear error response indicating that the ID is not valid

## Priority
High

## Screenshots/Video


<img width="1129" alt="Screenshot 2025-02-17 at 15 51 15" src="https://github.com/user-attachments/assets/f956f24a-dbeb-4473-a28d-e70f808b853a" />



## Device Details:
Postman Version: 10.17.3-230823-0523
OS: MacOs 15.1
Version:Sequoia Version 15.1
Browser : Chrome Version 115.0.5790.170 (Official Build) (arm64)
Resolution [2560 × 1600]

</details>

<details>

<summary>Bug 08-API -  Incorrect Response for DELETE Request with recently deleted Employee ID</summary>


## Description

When sending a DELETE request to remove an employee from the system, if an employee ID that has already been deleted, the application responds with a "200 OK" status. This behavior is misleading as it suggests successful deletion, even though the employee already does not exist in the first place.

## Pre-condition

Have the valid Postman collection imported in Postman


## Steps To Reproduce

1. Launch Postman and access the QA Challenge- Master collection
2. Go to the DELETE request `Delete Employee` to remove an Employee.
3. On the Request URL include an already deleted employee ID value of a user.
4. Click on the Send button to send the DELETE request.


## Actual behavior
The application accepts the DELETE request with  already deleted employee ID. The server responds with a "200 OK" status, which incorrectly suggests successful deletion.

## Expected behavior
The application should validate the provided employee ID to ensure that it exists in the system. If a non-existing or already deleted ID is detected, the application should return a "404 Not Found" status or an appropriate error response indicating that the employee does not exist.

## Priority
High

## Impact:
This issue has the following negative impacts:

Misleading Response: The "200 OK" status implies successful deletion when the employee does not exist, leading to confusion and incorrect assumptions.
Data Integrity: Users might believe they have successfully deleted a nonexistent employee, affecting data integrity and accuracy.
Ineffective Error Handling: The application fails to provide accurate error responses for such cases, making troubleshooting difficult.

## Screenshots/Video


<img width="1266" alt="Screenshot 2025-02-17 at 16 07 13" src="https://github.com/user-attachments/assets/0ab963af-b715-49cd-9976-f98fd19a4758" />


## Device Details:
Postman Version: 10.17.3-230823-0523
OS: MacOs 10.15.7
Version: Sequoia Version 15.1
Browser : Chrome Version 115.0.5790.170 (Official Build) (arm64)
Resolution [2560 × 1600]

</details>

<summary>Bug 09-API -  Incorrect Response for DELETE Request with Invalid Employee ID</summary>


## Description

When sending a DELETE request to remove an employee from the system, if an employee ID that has already been deleted, the application responds with a "405" error status. 

1. Launch Postman and access the QA Challenge- Master collection
2. Go to the DELETE request `Delete Employee` to remove an Employee.
3. On the Request URL include an invalid employee ID value of a user with wrong characters( i.e //4392990-3230023abcd-34234ddff).
4. Click on the Send button to send the DELETE request.


## Actual behavior
The API returns a 405 Method Not Allowed error which:
	•	The response does not provide a clear indication that the requested employee does not exist.
	•	The error message does not follow standard RESTful API conventions for handling resource deletion errors.
	•	The request method itself (DELETE) is valid, so a 405 status code is misleading in this context

## Expected behavior
The API should return a 404 Not Found status code instead of 405 Method Not Allowed if the Employee ID does not exist.
	•	The response body should provide a meaningful error message, such as:
 error": "Employee ID not found or non existing"
 The API should follow RESTful principles, ensuring correct error handling for resource deletion requests
## Priority
High

## Impact:
This issue has the following negative impacts:

The issue causes misleading error handling, as a 405 Method Not Allowed response suggests a method restriction instead of indicating that the Employee ID does not exist or has already been deleted. 
This leads to confusion for developers, inefficient debugging, and doesnt follow RESTful API usual conventions. 
It can also impact third-party integrations, user experience, and security. The correct approach is to return a 404 Not Found with a clear error message.

## Screenshots/Video

<img width="1419" alt="Screenshot 2025-02-17 at 16 19 52" src="https://github.com/user-attachments/assets/7989ff69-ca92-4a4d-8d86-5c97e0e55845" />




## Device Details:
Postman Version: 10.17.3-230823-0523
OS: MacOs 15.1
Version: Sequoia Version 15.1
Browser : Chrome Version 115.0.5790.170 (Official Build) (arm64)
Resolution [2560 × 1600]

</details>

<details>

<summary>Bug 10-API -  Incorrect Response for GET Request with Non-Existing Employee ID</summary>


## Description

When sending a GET request to remove an employee from the system, if an employee ID that has already been deleted or does not exist is provided in the request URL, the application responds with a "200 OK" status. This behavior is misleading as it suggests successful, even though the employee does not exist in the first place.

## Pre-condition

Have the valid Postman collection imported in Postman


## Steps To Reproduce

1. Launch Postman and access the QA Challenge- Master collection
2. Go to the GET request `Get Employee` to retreive information of an Employee.
3. On the Request URL input an already non existing or recently deleted employee ID value of a user.
4. Click on the Send button to send the GET request.


## Actual behavior
The application accepts the GET request with a non-existing or already deleted employee ID. The server responds with a "200 OK" status, which incorrectly suggests successful retreivement of Employee details.

## Expected behavior
The application should validate the provided employee ID to ensure that it exists in the system. If a non-existing or already deleted ID is detected, the application should return a "404 Not Found" status or an appropriate error response indicating that the employee does not exist.

## Priority
High

## Impact:
This issue has the following negative impacts:

Misleading Response: The "200 OK" status implies successful deletion when the employee does not exist, leading to confusion and incorrect assumptions.
Data Integrity: Users might believe they have successfully deleted a nonexistent employee, affecting data integrity and accuracy.
Ineffective Error Handling: The application fails to provide accurate error responses for such cases, making troubleshooting difficult.

## Screenshots/Video

<img width="1472" alt="Screenshot 2025-02-17 at 16 22 31" src="https://github.com/user-attachments/assets/cfefee02-31c7-496a-8b54-de0d7597e673" />


<img width="1282" alt="Screenshot 2025-02-17 at 16 23 30" src="https://github.com/user-attachments/assets/6e52f7f5-290d-4908-a2fc-2e7ff7c68b69" />

## Device Details:
Postman Version: 10.17.3-230823-0523
OS: MacOs 15.1
Version: Mac OS Sequoia Version 15.1
Browser : Chrome Version 115.0.5790.170 (Official Build) (arm64)
Resolution [2560 × 1600]

</details>


<details>

<summary>Bug 11-API -  500 Internal Server Error with Invalid ID in GET Request Body for GET Employee </summary>


## Description

When attempting to retreive an employee's information using a GET request, a 500 server error is encountered due to an invalid ID being provided in the request URL. The application should handle and validate input data to ensure that only valid IDs are accepted for updates

## Pre-condition

Have the valid Postman collection imported in Postman


## Steps To Reproduce

1. Launch Postman and access the QA Challenge- Master collection
2. Go to the GET request `GET Employee` to retrieve an Employee's information.
3. On the Request body include an invalid ID value of an Employee.( whatever input as ID on the id variable)
4. Click on the Send button to send the GET request.


## Actual behavior
The application accepts the GET request with an invalid ID value in the request URL.The server responds with a 500 internal server error message:
	•	The error indicates an unhandled exception rather than a properly managed validation failure.
	•	No clear message is provided to inform the user that the issue is due to an invalid Employee ID.
	•	The request causes a server-side failure, potentially exposing internal system vulnerabilities.

## Expcted behavior
The API should validate the Employee ID before processing the request.
Additionally:

-If an invalid or non-existent ID is provided, the API should return a 400 Bad Request (if the format is incorrect) or a 404 Not Found (if the ID does not exist).
-A meaningful error message should be returned, such as:
error": "Invalid Employee ID. Please provide a valid identifier."

## Priority
High

## Screenshots/Video

<img width="1409" alt="Screenshot 2025-02-17 at 16 26 08" src="https://github.com/user-attachments/assets/a446b6af-093e-4131-ad0c-0434e79d50a5" />
<img width="1490" alt="Screenshot 2025-02-17 at 16 26 20" src="https://github.com/user-attachments/assets/3c8f4418-a198-44d7-8f6f-db9d40ffc838" />


## Device Details:
Postman Version: 10.17.3-230823-0523
OS: MacOs 15.1
Version: Mac OS Sequoia Version 15.1
Browser : Chrome Version 115.0.5790.170 (Official Build) (arm64)
Resolution [2560 × 1600]

</details>

<details>

<summary>Bug 12-API -  Inconsistent Response for PUT Request with Unchanged User Details</summary>


## Description

When sending a PUT request to edit a user's information, if the request body contains the same details as the existing user, the application responds with a "200 OK" status. This behavior is inconsistent with the expectation that only changes in user details should trigger a successful update response.

## Pre-condition

Have the valid Postman collection imported in Postman


## Steps To Reproduce

1. Launch Postman and access the QA Challenge- Master collection
2. Go to the PUT request `Update Employee` to retrieve an Employee's information.
3. Provide the exact same details as the existing user in the request body.
4. Click on the Send button to send the PUT request.


## Actual behavior
The application accepts the PUT request with unchanged user details in the request body.The server responds with a "200 OK" status, suggesting a successful update even though no changes were made.

## Expected behavior
The application should validate the provided user details against the existing user's information.If the user details in the request body are identical to the existing user, the application should return a "304 Not Modified" status or an appropriate response indicating that no changes were made.

## Priority
Medium

## Screenshots/Video

<img width="1464" alt="Screenshot 2025-02-17 at 16 32 57" src="https://github.com/user-attachments/assets/7ab4a527-0315-402f-9b5f-1cfe381df8a3" />
<img width="1397" alt="Screenshot 2025-02-17 at 16 33 16" src="https://github.com/user-attachments/assets/92a8f95f-21b4-4e18-926b-496ca958e697" />



## Device Details:
Postman Version: 10.17.3-230823-0523
OS: MacOs 15.1
Version: Mac OS Sequoia Version 15.1
Browser : Chrome Version 115.0.5790.170 (Official Build) (arm64)
Resolution [2560 × 1600]

</details>

<details>
  
<summary>Bug 13-API -Duplicate Employee Creation Allowed with Identical Details</summary>


## Description

When adding a new employee using a POST request, the system allows multiple employees to be created with identical First Name, Last Name, and Number of Dependents, 
even if an employee with the same details already exists.
## Pre-condition

Have the valid Postman collection imported in Postman


## Steps To Reproduce

  1.   Launch Postman and open the QA Challenge - Master collection.
	2.	Navigate to the POST request Add Employee.
	3.	Provide details for a new employee (First Name, Last Name, and Dependents).
	4.	Click Send to create the employee.
	5.	Repeat the request using the same exact details.


## Actual behavior
	
• The API returns a “200 OK” response
• A new duplicate employee is created with the same details.
•	The response includes the details of the newly created duplicate employee, confirming the action.

## Expected behavior
The system should check for existing records before creating a new employee.	If an employee with the same First Name, Last Name, and Number of Dependents already exists, the API should return a 409 Conflict response with an appropriate message, such as:
 "error": "An employee with these details already exists. Duplicate entries are not allowed."
## Priority
Medium

## Screenshots/Video
<img width="1276" alt="Screenshot 2025-02-17 at 16 44 06" src="https://github.com/user-attachments/assets/93f96bf1-79ec-441e-8a61-cbf3257ab304" />

<img width="1468" alt="Screenshot 2025-02-17 at 16 38 28" src="https://github.com/user-attachments/assets/166b611f-a13b-4ed0-9898-0a2f706141db" />

<img width="1308" alt="Screenshot 2025-02-17 at 16 38 38" src="https://github.com/user-attachments/assets/813f9c6f-d54a-4040-9113-b0679c9cc8d8" />



## Device Details:
Postman Version: 10.17.3-230823-0523
OS: MacOs 15.1
Version: Mac OS Sequoia Version 15.1
Browser : Chrome Version 115.0.5790.170 (Official Build) (arm64)
Resolution [2560 × 1600]

</details>


<details>
  
<summary>Bug 14-UI -First Name and Last Name Fields Accept Numeric Characters</summary>


## Description

The First Name and Last Name fields in the UI allow users to enter numeric characters (0-9) or even just numbers when adding or editing an employee. This is incorrect behavior, as these fields should only accept alphabetic characters and possibly 
special characters like hyphens or apostrophes. The system should enforce proper validation to prevent invalid name entries
## Pre-condition

Access to the Paylocity Employee Management System.


## Steps To Reproduce

1.Go to link for the application to login at https://wmxrwq14uc.execute-api.us-east-1.amazonaws.com/Prod/Account/Login

2.Enter valid details for Username and password and click on the Login button

2.Click on the `Add Employee` button or edit on an existing employee

3.Input on the First Name field or Last Name field numbers or combination of letters and numbers.

4.Proceed with adding the employee by clicking on the `Add button`


## Actual behavior
  •	The UI accepts numeric characters in the First Name and Last Name fields.
	•	The system successfully saves the employee without validation errors.
	•	The invalid name is displayed in the employee list and details page

## Expected behavior
  •	The First Name and Last Name fields should only accept alphabetic characters.
	•	If a user enters numbers, the system should display a validation error message, such as:
 First Name and Last Name must contain only letters."
## Priority
High

## Screenshots/Video



https://github.com/user-attachments/assets/ba76746d-866a-4ddc-9940-620edcc502ce



## Device Details:
Postman Version: 10.17.3-230823-0523
OS: MacOs 15.1
Version: Mac OS Sequoia Version 15.1
Browser : Chrome Version 115.0.5790.170 (Official Build) (arm64)
Resolution [2560 × 1600]

</details>

<details>
  
<summary>Bug 15-UI -No Validation Error Message for Invalid Dependent Field Input</summary>


## Description

When a user enters invalid input (e.g., letters or special characters) in the Dependent field while adding or editing an employee, the UI correctly prevents the adding or editing with invalid character but does not display any validation error message. 
This creates a poor user experience, as users are unaware of why they cannot proceed .

## Pre-condition

Access to the Paylocity Employee Management System.


## Steps To Reproduce

1.Go to link for the application to login at https://wmxrwq14uc.execute-api.us-east-1.amazonaws.com/Prod/Account/Login

2.Enter valid details for Username and password and click on the Login button

2.Click on the `Add Employee` button or edit icon on an existing employee

3.Go to the Dependent field an enter an invalid character. 
4. Try to Add or Update the employee


## Actual behavior
    
  • The UI prevents submission when invalid input is entered.
	•	No validation error message is displayed, leaving users confused about why they cannot proceed.
	•	Users have no guidance on the expected input format.

## Expected behavior
  The UI should display a clear validation error message when invalid input is detected, such as:
Error: "Invalid input: The Dependent field must contain only numbers."

## Priority
Medium

## Screenshots/Video




https://github.com/user-attachments/assets/e211f3a9-6126-4366-ab95-af3ef9b27981





## Device Details:
Postman Version: 10.17.3-230823-0523
OS: MacOs 15.1
Version: Mac OS Sequoia Version 15.1
Browser : Chrome Version 115.0.5790.170 (Official Build) (arm64)
Resolution [2560 × 1600]

</details>
