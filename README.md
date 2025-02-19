PaylocityTask- QA Bug Challenge 🐛 🔍
Welcome to the Bug Challenge Solutions repository! Here you'll find the reports to the software bugs that were identified in the STE Bug Challenge for the Paylocity Benefits Dashboard along with the solution for the API part of the STE Automation challenge. Each bug has been analyzed, found and documented here.

How to navigate through the Repo 🧭
On the file named bugchallengepcty.md  you will see tne different dropdown Bugs and categorized by numbers(e.g Bug 01,etc).You will find the list of 16 bugs found, analyzed and documented.

On the file QA Challenge- Master.postman_collection.json you will find the Postman Collection used to run the API tests with all the mentioned requets that are detailed in the Bugs found along with the assertions made.
As well you will find the file for the environment that was made : Benefits-Paylocity.postman_environment.json. 

Run the Postman Collection: To test any potential bug fixes or to run the collection to re-verify the bugs, and running the API requests with the assertions, you can use the provided Postman Collection and environment. The collection includes API requests with assertions made.

-Step 1: Download and install Postman.

-Step 2: Open Postman and import the Bug-Challenge-Collection.json file located in the postman-collection directory of this repository.
-Step 3: After importing the collection then proceed to import the Benefits-Paylocity.postman_environment.json. file in the environments section in postman. This is done by
going on the left panel ->Environments ->Import>Selecting the file

-Step 3: Once imported, you will see a collection of API requests named "QA Challenge- Master." and an environment created named Benefits-Paylocity. On a collection level make sure to select the envinronment so all the requests are run using this environment.

-Step 4: Going to the requests: Each request corresponds to a specific scenarios. Click on a request to open it.

-Step 5: Review the request details and ensure that any variables (such as base URLs), specific as well to the Basic Token, and that these are correctly set.

-Step 6: Send the request and observe the response to verify that the bug fix is effective or that the bug is still present as reported.

Additionally you can opt to Run the entire collection so all the tests are run at once.

Other options: Clone the Repository: Begin by cloning this repository to your local machine using the following command:

git clone < https://github.com/erodm09/PaylocityBugchallenge.git>

Explore the Bugs
Navigate through the repository to find detailed bug reports found for various scenarios. Each bug report includes a description of the bug, steps to reproduce, expected behavior, actual behavior, impact, priority, and screenshots.

Contact 📧
For questions or discussions related to the bug solutions or this repository, feel free to contact Edgar Rodriguez at erodm9@gmail.com
