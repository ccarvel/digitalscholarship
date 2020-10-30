Install Chocolatey
------------------

[Chocolatey](https://chocolatey.org/install) is the Windows package manager.

Open PowerShell in Administrative mode (Windows key ⊞ >> type "Windows Powershell" >> right click >> "Run as Administrator").
Once PowerShell is running, run the following command. It may be easiest to copy and paste to avoid typos.
```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```
Install Anaconda 
-----------------

[Anaconda](https://www.anaconda.com/open-source) is a collection of data science tools that provides everything you need to use Handprint. You can install the Python 3 version of Anaconda with this command:

```
choco install anaconda3
```
You may be prompted to approve the installation with the following text (or similar):<br>
```Do you want to run the script?([Y]es/[A]ll - yes to all/[N]o/[P]rint):```<br>
Here you can enter ```A``` and press Enter<br>
As noted during installation, be patient. The Anaconda3 installation can take a while to install (up to 30 minutes).

Install sudo
------------

Also install sudo, which allows you to run command-line applications (like choco) with administration rights without opening an administrator PowerShell window:

```
choco install sudo
```

Close your administrative shell window:
```
exit
```

Use Anaconda
------------

To use Anaconda's tools in PowerShell, open a new "Anaconda Powershell Prompt". You should then be able to follow the rest of this tutorial.
