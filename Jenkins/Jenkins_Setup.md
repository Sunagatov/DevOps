# Jenkins Setup

- Choose root user
  * Command _"_**sudo su -**_"_

- Visit Jenkins website
  * Link: _"https://www.jenkins.io/"_
  
- Go to Download page
  * Link: _"https://www.jenkins.io/download/"_
  
- Choose Jenkins version for particular OS
  * OS Name: _**"Red Hat/Fedora/Alma/Rocky/CentOS"**_
  * Link: _"https://pkg.jenkins.io/redhat-stable/"_
  
- Execute these commands
  *  sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
  *  sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key" 
  *  amazon-linux-extras install java-openjdk11
  *  yum install jenkins
  
- Open a web browser
- Open Jenkins UI using your EC2 instance url and 8080 port.
- Insert a password
  * Retrieve password using command: _**"cat /var/lib/jenkins/secrets/initialAdminPassword"**_


