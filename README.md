This script automates the installation process for a master and slave Ubuntu vagrant machine, allowing for a seamless setup of a LAMP stack. The following components are required for successful execution: 
- Vagrant 
- Virtual Box 

Slave & Master Machine Specifications:
- Memory: 1024 MB
- CPUs: 2 

Slave Machine Configuration:
The slave1 machine will contain the following specifications: 
- Name: slave1
- Image: ubuntu/focal64
- Network Settings:
    - Private Network 
    - IP Address: "192.168.20.11"

The script will then proceed to update and upgrade the machine before installing the necessary components, including sshpass for password authentication during login, enabling password authentication, restarting the sshd service, and installing avahi-daemon libnss-mdns.

Master Machine Configuration:
The master machine will have the following specifications:
- Host Name: master
- Image: ubuntu/focal64
- Network Settings:
    - Private Network 
    - IP Address: "192.168.20.10"

Master Configuration:

To ensure optimal performance, please follow the steps below to update and upgrade your machine.

Installation:
- Install sshpass, which allows you to enter a password while logging in.
- Enable the password authenticator for logging in with a password.
- Restart the sshd service.
- Install avahi-daemon libnss-mdns for improved network compatibility.


Script Configuration for Master:
- Create a new user with sudo access named "altschool".
- Generate an SSH key for the "altschool" user.
- Copy the "altschool" user's SSH key to the slave machine. Please note that only the user "altschool" will be able to SSH into the slave machine using a password.
- Copy a file named "/mnt" from the "altschool" user to the slave machine.


LAMP Stack (Master & Slave Installation):
The LAMP (Linux, Apache, MySQL, PHP) stack is essential for website development and hosting. Please follow these steps for installation:

1. Install Apache2 Web Server
2. Install PHP and its requirements
3. Install MySQL database management system
4. Enable necessary modules for optimal performance 
5. Restart Apache Web Server 

Finally, the installation script will configure a LAMP stack on both the master and slave servers. Once completed, Apache will be restarted to ensure proper functionality. In addition, both the MySQL server and client will also be installed on both servers as part of the installation process.
