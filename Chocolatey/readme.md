## Using Chocolatey to install Terraform and Supporting Apps

I have setup a Chocolatey script that will provide all the tools you need to work with Terraform on Azure - see [here](/Chocolatey/TerraformApps.ps1) or use the Chocolatey install script below:

#Chocolatey setup and installation script for using Terraform
#Set Execution Policy to allow script to run
Set-ExecutionPolicy Bypass -Scope Process -Force 
#Chocolatey install
iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
#Chocolatey apps
choco install vscode -y -no-desktopshortcuts
choco install terraform -y -no-desktopshortcuts
choco install azure-cli -y -no-desktopshortcuts