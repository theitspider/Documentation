# Automating LAMP Stack Installation

## Description

This guide presents a Bash script for automating the installation and configuration of a LAMP (Linux, Apache, MariaDB, PHP) stack on a Debian-based Linux system.

## Script

```bash
#!/bin/bash

# Check for root privileges
if [ "$(id -u)" -ne 0 ]; then
  echo "This script must be run with root privileges." 1>&2
  exit 1
fi

# Update package repositories
apt update

# Install Apache web server
apt install -y apache2

# Install MariaDB server and configure
debconf-set-selections <<< "mariadb-server-10.5 mysql-server/root_password password [YOUR_PASSWORD_HERE]"
debconf-set-selections <<< "mariadb-server-10.5 mysql-server/root_password_again password [YOUR_PASSWORD_HERE]"
apt install -y mariadb-server

# Secure MariaDB installation
mysql_secure_installation <<EOF
y
[PASSWORD]
[PASSWORD]
y
y
y
y
EOF

# Install PHP and required modules
apt install -y php libapache2-mod-php php-mysql

# Restart Apache and MariaDB services
systemctl restart apache2
systemctl restart mariadb

echo "LAMP stack installation completed successfully."
```

## Explanation

The script begins by verifying root privileges and updating the package repositories to ensure the latest versions of software packages are available. It then proceeds to install the Apache web server (`apache2`) and MariaDB server (`mariadb-server`). During MariaDB installation, the script preconfigures MariaDB with a root password specified within the script. Replace `[YOUR_PASSWORD_HERE]` with a desired password.

After installing MariaDB, the script runs `mysql_secure_installation` to secure the MariaDB installation by removing default accounts and tightening security settings. Next, it installs PHP (`php`) along with the Apache PHP module (`libapache2-mod-php`) and the PHP MySQL extension (`php-mysql`) to enable PHP support for connecting to MariaDB databases.

Finally, the script restarts both Apache and MariaDB services to apply the configuration changes made during installation.

## Usage

After saving the script to a file, for example, `install_lamp.sh`, set the execution permissions using `chmod +x install_lamp.sh`. Then execute the script with root privileges using `sudo ./install_lamp.sh`.

## Notes

- Replace `[PASSWORD]` with a secure password for the MariaDB root user.
- This script is specifically designed for Debian-based Linux distributions and may require modifications for other distributions.
- Always review scripts from untrusted sources before executing them on a system.

## Conclusion

Utilizing this script facilitates the efficient setup of a LAMP stack on Debian-based Linux systems, enabling the hosting of dynamic websites and web applications. Through automation, the installation and configuration process becomes streamlined, saving time and effort for system administrators and developers alike. This script serves as a valuable tool for deploying a robust web hosting environment without manual intervention.
