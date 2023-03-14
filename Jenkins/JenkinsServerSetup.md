# Jenkins Server

### Launch AWS EC2 instance:
- Open AWS UI dashboard.
- Find AWS EC2 Service.
- Press the button "Launch AWS EC2 instance"
- Choose Amazon Machine Image (AMI)
  * Name: "Amazon Linux 2 Kernel 64-bit (x86)"
- Choose an instance type
  * Name: "r2.micro"
- Add storage
    * Name: "General purpose SSD (gp2) 8 GiB"
- Add tags
    * Key: "Name"
    * Value: "Jenkins_Server"
- Configure Security Group
    * Create a new security group
      * Name: "DevOps_Project_Security_Group"
      * Description: "DevOps_Project_Security_Group"
    * Add a new custom TCP rule
      * Port Range: "8080"
      * Protocol: "TCP"
      * Source: "0.0.0.0/0"
      * Source: "::/0"
      * Source Type: "Custom"
- Create a new key pair:
  * Type: "RSA"
  * Name: "DevOps_Project_RSA_Key"
  * Key file format: "pem"
  

