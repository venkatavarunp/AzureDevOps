# PowerShell
- Made by Microsoft
- Cross-Platform Automation and Configuration
- Command Line shell and Scripting language
- Extensible through modules
`cmdlets` is a word for the commands that we run in PowerShell

## Installing PowerShell on Linux

```
# Update the list of packages
sudo apt-get update

# Install pre-requisite packages.
sudo apt-get install -y wget apt-transport-https software-properties-common

# Download the Microsoft repository GPG keys
wget -q "https://packages.microsoft.com/config/ubuntu/$(lsb_release -rs)/packages-microsoft-prod.deb"

# Register the Microsoft repository GPG keys
sudo dpkg -i packages-microsoft-prod.deb

# Delete the the Microsoft repository GPG keys file
rm packages-microsoft-prod.deb

# Update the list of packages after we added packages.microsoft.com
sudo apt-get update

# Install PowerShell
sudo apt-get install -y powershell

# Start PowerShell
pwsh
```
```
curl https://packages.microsoft.com/config/rhel/7/prod.repo | sudo tee /etc/yum.repos.d/microsoft.repo

sudo yum install -y powershell
```
## Accessing PowerShell
we can launch it by 
```
pwsh
```
we can get the running processes by `get-processes` command
```
get-processes
```
we can change the default command line in linux by 
```
cat /etc/shells

chsh -s /usr/bin/pwsh 
```

