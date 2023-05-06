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
## Command Syntax
each of cmdlets has a set of standards they adhere to. This allows us to have a much more uniform and consistent experience across all of cmdlets that we use.

cmdlets follow a set struture `verb-noun` structure. One of the example for this is get-process or get-ADuser (where get is noun)

to get list of commands
```
get-command
```
to get help with cmdlets we can use `get-help`
```
get-help get-process
```
to get the full details we can use 
```
get-help -full 

get-help -detailed
```
to get cmdlets of a verb we use
```
get-command -verb get
```
to get cmdlets with a specific noun we use
```
# gets the cmdlets ending with time noun 
get-command -noun "*time"

# gets the cmdlets starting with time noun
get-command -noun "time*
```

to get modules in the machine
```
get-module -ListAvailable
```
to get cmdlets for a specific module 
```
get-command -Module PSReadLine
```
## Running Commands 
we can pipe using powershell as well and we can pass objects while piping with commands 
```
Get-Process | select-object ProcessName
```
to sort the objects 
```
Get-Process | select-object ProcessName | Sort-Object ProcessName
```

## Variables 
to get objects with specific values we can use variables. we can declare variable using `$` in powershell and `_` variable is referencing to the object passed through pipe 
```
get-process | where{$_.ProcessName -eq "systemd"}
```
to assign an object to a variable we can use 
```
$var = get-process | where{$_.ProcessName -eq "systemd"}
```
we can setup the properties to variables as
```
$myvar = "Hello World"

Set-Variable -name $myvar -Description "welcome"

# select * shows all properties
Get-Variable $myvar | select *
```
## if , Loops
example for if else 
```
if ($var.CPU -gt 1){Write-Host "The CPU is running high"}
else {Write-host "CPU is running cool"}
```
example for while loop
```
$var=1  
while($var -lr 5)  
{
    $message="---Pass"+$var+"---"
    get-process | select ProcessName , CPU | sortobject -property CPU | select -last 5
    $var++ 
}
```
## modules 
they are sets of commands that are packaged together

to find a module we use
```
find-module aZ
```
to install module we use
```
install-module aZ
```
to import a module we use
```
import-module az
```
to get cmdlets for a specific resources we can use 
```
get-command -module az.sql
```
## Scheduling script execution
we can do this using 
- `Cron` in Linux 
- `Task Scheduler` in Windows
- Third Party tools on Linux and Windows

lets create a cron in powershell
```
vim psscript.ps1
```
in the editor we can use 
```
#! /usr/bin/pwsh

get-uptime > /home/cloud_user/uptime.txt
```
we need to give excute permissions to cron 
```
chmod +x psscript.ps1
```
to edit cron we use 
```
crontab -e
```
we insert the cron values in the editor 
```
* * * * * pwsh -file "/home/user/psscript.ps1"
```
we can check the excution of the cron using  
```
cat ./uptime.txt 
```
**Create and powershell script to record the server name and its top 5 cpu-utilizing processes to a file**
```
vim psscript.ps1
```
```
hostname > processes.txt

get-process | sort-object -property cpu | select -last 5 | out-file -append processes.txt
```
```
./psscript.ps1
```
```
cat ./processes.txt
```
