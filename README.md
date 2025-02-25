# SonarQube---Jenkins-Integration

Prerequisites
Jenkins installed and running.

SonarQube server installed and running.

SonarScanner installed on the Jenkins server or agent.

A project repository (e.g., GitHub, GitLab, Bitbucket) to analyze.

Steps to Integrate SonarQube with Jenkins
1. Install Required Plugins in Jenkins
Go to Jenkins Dashboard → Manage Jenkins → Manage Plugins.

Install the following plugins:

SonarQube Scanner for Jenkins

Pipeline Utility Steps (optional, for advanced pipeline scripts).

2. Configure SonarQube Server in Jenkins
Go to Jenkins Dashboard → Manage Jenkins → Configure System.

Scroll down to the SonarQube servers section.

Click Add SonarQube and provide the following details:

Name: A name for your SonarQube server (e.g., SonarQube).

Server URL: The URL of your SonarQube server (e.g., http://localhost:9000).

Server authentication token:

Go to your SonarQube server → User → My Account → Security.

Generate a token and paste it here.

Click Save.

3. Configure SonarScanner in Jenkins
Go to Jenkins Dashboard → Manage Jenkins → Global Tool Configuration.

Scroll down to the SonarQube Scanner section.

Click Add SonarQube Scanner and provide:

Name: A name for the scanner (e.g., SonarScanner).

Install automatically: Check this box to let Jenkins install the scanner automatically.

Click Save.

4. Add SonarQube Analysis to Your Jenkins Job
You can integrate SonarQube analysis into your Jenkins job using either a Freestyle Project or a Pipeline.

Option 1: Freestyle Project
Go to your Jenkins job → Configure.

Under the Build section, add a build step:

Select Execute SonarQube Scanner.
