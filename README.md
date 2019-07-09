# GitLab Issues API
This project is created as an automated test of the GitLab Issue API's. The project exist out of 1 main folder:

* GitLab Issues API

And to sub-folders (collections) containing the requests:

* CRUD operations
* Edge cases

All the requests in these collections make use of the end points that are available on the GitLab Issues API page.

For more info go to https://docs.gitlab.com/ee/api/issues.html

## Important notes

* Authorization is done via an OAUTH2 acces token. This token is added to the authorization tab in the 'GitLab Issues API' folder. All underlying folders and requests inherit the authorization from this parent.

* All request make use of parameters. Parameters are defined as environment variables, so that they are only available within the GitLab environment.

* All folders and requests are accompanied with a description with more info about the executed tests.

* Every request contains 1 or more tests which are shown in the 'Test' tab of the request. All test are accompanied with comments to clarify what is executed with each line of code.

## Getting started
The project was created in Postman and exported as a .json file. Download the project to your local environment. 
For the execution of the tests no additional plugins or libraries are needed.

## Prerequisites
The following is needed to run the tests via Postman App:
* Postman App

Note. There is also a chrome extensions for Postman available. This extensions hasn't been used for this project. Therefore we advice to use the App.

The following is needed to run the tests via the command line:
* Node.js
* Newman

## Installing Postman App
* Download the Postman App from https://www.getpostman.com/downloads/

## Installing Node.js and Newman
* Follow the instructions in this tutorial to install node.js and Newman: https://www.youtube.com/watch?v=f2yMmOGZU7M

## Running tests via the Postman App
* Open the application
* Sign in with your account. In case you don't have an account yet, click on 'Create account'
* Click on the 'Import' button in the header of the app.
* Open the tab 'Import Folder'
* Click on 'Choose folder' and select the project folder from your local environment.

### Running all tests via 'Runner'
* Click on the 'Runner' button in the header of the app. The 'Collection Runner' will now be opened in a new window.
* Under 'All collections' select the collection 'GitLab Issues API'.
* Select 'GitLab' as 'Environment'
* Click on 'Run GitLab Issues ...'. Now all test will be executed and the results are shown in a report.

### Running tests manually
You can also run a test manually bij openening the request in the collection and click on 'Send'. Make sure to execute the test in the order as they are shown in the folder to make sure all tests will pass (for example, we need to create an issue first before we can delete it).

### Running tests via command line

todo

