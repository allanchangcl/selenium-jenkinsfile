# Selenium tests Workflow with Jenkins Codepipeline
To fully automate, you will need to setup Jenkins plugins for git integration.
So when you push to git, it will trigger Jenkins to run the tests.

This example only explains setup for part of the process.
Jenkins will fetch from repository and run the tests using pipelines.

## Requirements
Running Jenkins server
Have ChromeDriver in /usr/local/bin/chromedriver
Allow repository access

## Jenkins Setup
Create a new job
Enter item name
Select Pipeline
 - pipeline script form scm
 - scm => git
 - enter repository url
