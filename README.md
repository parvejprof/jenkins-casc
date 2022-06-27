### To run Jenkins Configurations As Code

## Create Volume 
docker volume create jenkins-vol

## Buid now
docker build -t jenkins:jcasc .

### Change Jenkins Admin user and Password
docker run --name jenkins --rm -p 8080:8080 -v jenkins-vol:/var/jenkins_home/ --env JENKINS_ADMIN_ID=admin --env JENKINS_ADMIN_PASSWORD=password  jenkins:jcasc
