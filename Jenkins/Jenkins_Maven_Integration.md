# Jenkins - Apache Maven Integration

### Connect to AWS EC2 Instance
- Choose root user
  * Command _"_**sudo su -**_"_

### Install Java
- Execute these commands
  *  amazon-linux-extras install java-openjdk11

### Download Apache Maven
- Visit Apache Maven website
  * Link: _"https://maven.apache.org/"_
- Go to Download page
  * Link: _"https://maven.apache.org/download.cgi"_
- Choose Apache Maven "Binary tar.gz archive" version 
- Copy the link of "Binary tar.gz archive"
- Go back to EC2 Instance terminal.
- Open the "opt" directory
  * Execute these commands _"cd /opt/"_
- Download the Apache Maven
  * wget https://dlcdn.apache.org/maven/maven-3/3.9.0/binaries/apache-maven-3.9.0-bin.tar.gz
- Unrchive the Apache Maven file
  * tar xzvf apache-maven-3.9.0-bin.tar.gz
- Rename the Apache Maven directory
  * mv apache-maven-3.9.0 maven
  * cd /maven/

### Add Apache Maven to the Linux OS Classpath
- Open the "root" directory
  * Execute these commands _"cd ~"_
- Edit ".bash_profile" file
  *  Execute the command "**_vi .bash_profile"_**
- Press the button "Esc"
- Press the button "i"
- Add the JAVA_HOME path
  * Execute the command "**_find / -name java*"_**
  * Find the java 11 path
  * Copy the path
  * Add the path to the JAVA_HOME variable
- Add the MAVEN_HOME path
  * /opt/maven
- Add the M2 path
  * /opt/maven/bin
- Update the PATH variable - PATH=$PATH:$HOME/bin
  * Add this value "$JAVA_HOME:$M2_HOME:$M2"
  * Result: "PATH=$PATH:$HOME/bin:$JAVA_HOME:$M2_HOME:$M2"
- Save the file
  * Press the button "Esc"
  * Press the button "Shift" + ":"
  * Execute "wq"
- Accept ".bash_profile" file changes
  * Execute the command "**_source .bash_profile*"_**
- Check the maven version now
  * Execute the command "**_mvn -v*"_**

### Install Github Jenkins Plugin
- Open a web browser
- Open Jenkins UI using your EC2 instance url and 8080 port.
- Press the button "Manage Jenkins"
- Press the button "Manage Plugins"
- Press the button "Available plugins"
- Find "Maven" plugin
- Press the button "Install without restart"

### Configure Apache Maven
- Press the button "Manage Jenkins"
- Press the button "Global Tool Configuration"
- Configure Maven section
- Configure JDK section
  * Name: "JAVA_11"
  * Path to "java 11 bin"
- Configure Maven section
  * Name: "MAVEN_3.9.0"
  * Path to Maven "/opt/maven"

### Configure Apache Maven Jenkins Plugin
- Press the button "New item"
  * Name: "**First_Maven_Project**"
- Choose "Maven project"
- Press the button "OK"
- Add the description
  * Description: "First Maven Project"
- Choose "Source Code Management"
  * Option: "Git"
- Provide repository url from Github
- Go to "Build Section"
  * Go to "Goals and options"
  * Add goals "clean install"
- Press the button "Apply"
- Press the button "OK"

# Apache Maven job is created!

If you press the button "Build now". 
Git will pull the project from the Github to the EC2 Instance.
Then Apache Maven will build the project with specified goals.
You can check the project using the command "cd /var/lib/jenkins/workspace/"


