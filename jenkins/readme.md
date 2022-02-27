
- Creating a Pipeline to Build and Push Docker Image for a Sample Java Microservice

## Steps to perform
 Step 1 - Launching Jenkins as Docker Container 
      Run- 
      docker compose up 
      Once Jenkins is up , note the admin password.
      Goto http://localhost:8081 
      Enter the password which we saved 
      Then create a new user and password in the page which appears.      
 Step 2 - Initializing Jenkins Plugins and Creating a Github Repo
      Create a github repo to save the Jenkins folder
      Commit and push the folder which comprises of sample java code. 
 Step 3 - Setting up Docker and Maven in Jenkins and First Pipeline Run
      In Jenkins UI- 
         Click on Global Tool Configuration 
         Add Maven and Docker. 
         Give them some name- eg: myMaven and myDocker 
         Now click on Jenkins-> New Item -> Create New job and give it a name- eg : Jenkins-pipeline. Choose pipeline from the list of options. 
         Goto Pipeline and choose- Pipeline script from SCM and then choose Git. 
         Provide the github url which we ceeated above in Step 2. 
         In Script Path- give name as Jenkinsfile (if not present)
         Click Save. 
         Pipeline should run. 

 Step 4 - Configuring Jenkins Pipeline Path with Docker and Maven Tools
          Save your docker hub credentials (https://hub.docker.com/) in the Jenkins UI.  # For assignment pushing to Docker hub
          Click Credentials and then Jenkins , then Global Credentials and then click Add Credentials.
          Keep it global scope. 
          Give it an ID. eg: dockerhub
 Step 5 - Build and Push Docker Image in Jenkins Pipelines by simply clicking Build now. 

