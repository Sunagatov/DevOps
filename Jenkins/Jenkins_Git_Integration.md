# Jenkins - Git Integration

### Connect to AWS EC2 Instance
- Choose root user
  * Command _"_**sudo su -**_"_
  
### Install Git
- Execute these commands
  *  yum install git

### Install Github Jenkins Plugin
- Open a web browser
- Open Jenkins UI using your EC2 instance url and 8080 port.
- Press the button "Manage Jenkins"
- Press the button "Manage Plugins"
- Press the button "Available plugins"
- Find "Github" plugin
- Press the button "Install without restart"

### Configure Git
- Press the button "Manage Jenkins"
- Press the button "Global Tool Configuration"
- Configure Git section
  * Name: "Git"
  * Path to Git executable
    * Execute these commands "whereis git"
    * Copy this path to the Git section - /usr/bin/git

### Configure Github Jenkins Plugin
- Press the button "New item"
  * Name: "Pull_Code_From_Github"
- Choose "Freestyle project"
- Press the button "OK" 
- Add the description
  * Description: "Pull code from Github"
- Choose "Source Code Management"
  * Option: "Git"
- Provide repository url from Github
- Press the button "Apply"
- Press the button "OK" 

# Jenkins job is created!

If you press the button "Build now". Git will pull the project from the Github to the EC2 Instance.
You can check the project using the command "cd /var/lib/jenkins/workspace/"

