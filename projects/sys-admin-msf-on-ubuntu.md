---
layout: default
---

[🏠 home](../)

<h1 style="text-align: center;">System Administration: Installing Metasploit on Ubuntu</h1>

# OS Version
```
DISTRIB_RELEASE=24.04
DISTRIB_DESCRIPTION="Ubuntu 24.04.1 LTS"
```

# Install Metasploit Framework
```
# Install curl and postgresql
sudo apt install curl postgresql postgresql-contrib

# Install metasploit
curl https://raw.githubusercontent.com/rapid7/metasploit-omnibus/master/config/templates/metasploit-framework-wrappers/msfupdate.erb > msfinstall

# Give read, write, and execute permissions
chmod 755 msfinstall

# Execute installation
sudo ./msfinstall

# Create msf database
msfdb init

# Launch msfconsole
msfconsole

# Verify database connectivity 
db_status

# Updating Metasploit Framework
msfupdate

# Check version
msfconsole  --version
```

# Uninstall Metasploit Framework
```
sudo apt remove metasploit-framwork
```
