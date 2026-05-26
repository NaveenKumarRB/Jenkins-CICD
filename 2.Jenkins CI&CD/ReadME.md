Install Jenkins

Install Java
    sudo apt install openjdk-17-jdk -y
Install Jenkins

curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | sudo tee \
  /usr/share/keyrings/jenkins-keyring.asc > /dev/null

echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null

sudo apt update
sudo apt install jenkins -y

Start Jenkins : - 
sudo systemctl enable jenkins
sudo systemctl start jenkins

Access Jenkins - http://<EC2-IP>:8080

Get Initial Password - sudo cat /var/lib/jenkins/secrets/initialAdminPassword


Install Jenkins Plugins

Git Plugin
Pipeline Plugin
NodeJS Plugin
SSH Agent Plugin

Configure Jenkins Tools
Go to: Manage Jenkins → Global Tool Configuration
Configure:

Git
NodeJS
Python

Flask Jenkins Pipeline
Create Pipeline Job

Name: flask-ci-cd
