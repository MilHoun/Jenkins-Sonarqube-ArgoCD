# Jenkins-Sonarqube-ArgoCD
Building a Java application in Jenkins using Docker as an agent, running static code analysis with Sonarqube, and deploying on Kubernetes using ArgoCD.

Run the commands below to install Java and Jenkins on an Ubuntu Amazon EC2 instance.

sudo apt update
sudo apt install openjdk-17-jre

Verify Java is Installed

java -version

Now, you can proceed with installing Jenkins

curl -fsSL https://pkg.jenkins.io/debian/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null
echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins

In our Jenkins Pipeline, we've used a declarative Jenkinsfile, which is easy to write and facilitates collaboration.
