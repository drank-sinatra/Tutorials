# Log into Linux Servers Without Entering Password
	1. Create a SSH public and private key pair using the command `ssh-keygen`
	2. Press **Enter**
	3. Press **Enter**
	4. Press **Enter**
	5. Execute the command `ssh-copy-id <user>@<server>` where **<user>** is the username for the server to logged into and **<server>** is the IP address or Bonjour name for the server to be logged into (e.g., `ssh-copy-id pi@raspberrypi.local` ) 
	6. Enter the correct password for the user specified above
	7. Log into the server with the command `ssh <user>@<server>` , and it should complete without prompting for a password