# Connect to EC2 via SSH

- Download a SSH Client.
  * Name: "MobaXterm"
- Open MobaXterm SSH Client.
- Configure MobaXterm SSH Client.
  * Press the button "Session". There you can see "Session settings"
  * Press the button "SSH"
  * Configure "Basic SSH settings"
    * Update "Remote host" - "Public IPv4 address"
    * Specify "username" - "ec2-user"
    * Port: "22"
  * Press "Advanced SSH settings"
  * Configure "Advanced SSH settings"
    * Press the button "Use private key"
    * Find the pem key.
    * Choose the key.
    * Protocol: "SFTP"
    * Compression: "Yes"
    * X-11-Forwarding: "Yes"

  

