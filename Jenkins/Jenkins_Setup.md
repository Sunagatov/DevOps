# Jenkins Setup

### Connect to AWS EC2 Instance
- Choose root user
  * Command _"_**sudo su -**_"_
  
### Install Java
- Execute these commands
  *  amazon-linux-extras install java-openjdk11

### Download Jenkins
- Visit Jenkins website
  * Link: _"https://www.jenkins.io/"_
  
- Go to Download page
  * Link: _"https://www.jenkins.io/download/"_
  
- Choose Jenkins version for particular OS
  * OS Name: _**"Red Hat/Fedora/Alma/Rocky/CentOS"**_
  * Link: _"https://pkg.jenkins.io/redhat-stable/"_

### Install Jenkins
- Execute these commands
  *  sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo
  *  sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key" 
  *  yum install jenkins

### Open Jenkins 
- Open a web browser
- Open Jenkins UI using your EC2 instance url and 8080 port.
- Insert a password
  * Retrieve password using command: _**"cat /var/lib/jenkins/secrets/initialAdminPassword"**_


