# simple-java-maven-app

This repository is for the
[Build a Java app with Maven](https://jenkins.io/doc/tutorials/build-a-java-app-with-maven/)
tutorial in the [Jenkins User Documentation](https://jenkins.io/doc/).

The repository contains a simple Java application which outputs the string
"Hello world!" and is accompanied by a couple of unit tests to check that the
main application works as expected. The results of these tests are saved to a
JUnit XML report.

The `jenkins` directory contains an example of the `Jenkinsfile` (i.e. Pipeline)
you'll be creating yourself during the tutorial and the `jenkins/scripts` subdirectory
contains a shell script with commands that are executed when Jenkins processes
the "Deliver" stage of your Pipeline.


How To Run::
1. Create a VM(preferably AWS) install java, jenkins and docker
sudo apt update
sudo apt install openjdk-17-jre

Jenkins:
curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins

2. Open port 8080(or check the required port in which jenkins is running using: ps -ef | grep jenkins)

3. Log into jenkins:
Go to browser type:: http://ipaddress(public EC2):port(Jenkins, in our case 8080)
Eg : http://18.233.147.245:8080

4. Install the Docker Pipeline and Maven plugin in Jenkins.

5. Run and if you run into any issue google it up.
