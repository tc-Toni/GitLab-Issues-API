# GitLab Issues API
'Postman project' is created as an automated test of the GitLab Issue API. The project, as depicted in the screenshot below, exist out of 1 main folder:

* GitLab Issues API

And 2 sub-folders (collections) containing the requests:

* CRUD operations
* Edge cases

All the requests in these collections make use of the end points that are available on the GitLab Issues API page.

For more info go to https://docs.gitlab.com/ee/api/issues.html

<img src="Images/Screenshot%20Postman.PNG" >

## GitLab Group and Project
* To be able to make request on issues in GitLab the issues must be part of a project. Therefore the following is created in GitLab:
  - Group: Big Bank
  - Project: Banking App

It is a public GitLab project. To view the issues on the project board first search on the group 'Big Bank' and then select the project 'Banking App'. Here you can select 'Issues' followed by 'Board'.

## Important notes

* Authorization is done via the OAuth 2.0 acces token. This token is added to the authorization tab in the 'GitLab Issues API' folder. All underlying folders and requests inherit the authorization from this parent.

* All request make use of parameters. These parameters are defined as environment variables, so that they are only available within the GitLab environment.

* All folders and requests are provided with a description with more info about the executed tests.

* Every request contains 1 or more tests which are shown in the 'Test' tab of the request. All test are provided with comments to clarify what is executed with each line of code.

## Expected test results
The collection exists out of 33 tests of which:
* 32 pass
* 1 fail
  - Failed test case: Set invalid due date for issue. 
  - Test case will fail due to a BUG. An invalid input (due_date=2019-35-35) is requested. 
    - Expected response: 400 Bad Request.
    - Actual response: 200 OK. 
    - When we check the value of due_date in the response it is 'null'

<img src="Images/Collection%20runner.PNG" >

## Getting started
* Download the folder 'Project Postman' to your local environment. The folder exists out of 2 .json files:
  - GitLab Issues API.postman_collection_final.json
  - GitLab.postman_environment_final.json

You can download this repository by clicking on the green 'Clone or download' button on top of this page and choose the option 'Download ZIP'. A file named GitLab-Issues-API-master.zip will be downloaded. Unpack the zip file to a desired location. Now the project folder is available to be imported in Postman (see 'Configuration of the Postman app' for how to do this).

For the execution of the tests no additional plugins or libraries are needed.

## Prerequisites
The following is needed to run the tests via Postman App:
* Postman App

Note. There is also a chrome extensions for Postman available. This extensions hasn't been used for this project. Therefore we advice to use the App.

The following is needed to run the tests via the command line:
* Node.js
* Newman

## Postman App
### Installing the Postman App
* Download the Postman App from https://www.getpostman.com/downloads/

### Configuration of the Postman App
* Open the application
* Sign in with your account. In case you don't have an account yet, click on 'Create account'
* Click on the 'Import' button in the header of the app.
* Open the tab 'Import Folder'
* Click on 'Choose folder' and select the 'Postman project' folder from your local environment. With this action both .json files (the collection and the environment) will be imported.

### Running all tests via 'Runner'
* Click on the 'Runner' button in the header of the app. The 'Collection Runner' will now be opened in a new window.
* Under 'All collections' select the collection 'GitLab Issues API' (1).
* Select 'GitLab' as 'Environment' (2)
* Click on 'Run GitLab Issues ...' (3). Now all test will be executed and the results are shown in a report.

<img src="Images/Collection%20Runner%20Settings.PNG" >

### Running tests manually
You can also run a test manually bij openening the request in the collection and click on 'Send'. 
* Make sure to select the envoronment 'GitLab' on the top right of the screen.
* Execute the test in the order as they are shown in the folder to make sure all tests will pass (for example, we need to create an issue first before we can delete it).

## Command Line
### Installing Node.js and Newman
* Follow the instructions in this tutorial to install node.js and Newman: https://www.youtube.com/watch?v=f2yMmOGZU7M

## License
This project is licensed under the MIT License.
