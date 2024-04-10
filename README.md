#!/bin/bash

# Update package index
sudo apt update

# Install Apache
sudo apt install -y apache2

# Start Apache service
sudo systemctl start apache2

# Enable Apache service to start on boot
sudo systemctl enable apache2

# Check Apache status
sudo systemctl status apache2

# Print Apache version
apache_version=$(apache2 -v | grep version)
echo "Apache installed successfully. Version: $apache_version"
