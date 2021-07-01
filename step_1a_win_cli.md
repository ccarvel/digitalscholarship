---
layout: default
title: 1a. Install Chocolatey, Python3 and Pip3 on Windows
nav_order: 3
---
Install Chocolatey
------------------

[Chocolatey](https://chocolatey.org/install) is the Windows package manager.

Open PowerShell in Administrative mode (Windows key ⊞ >> type "Windows Powershell" >> right click >> "Run as Administrator").
Once PowerShell is running, run the following command. It may be easiest to copy and paste to avoid typos.
```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```

Install Pyenv-Win
----

[Pyenv-Win](https://github.com/pyenv-win/pyenv-win) is a Python installation manager, which allows one to install multiple versions of python on their computer. 

*still in Powershell*
```
choco install pyenv-win 
```
You may be prompted to approve the installation with the following text (or similar):<br>
```Do you want to run the script?([Y]es/[A]ll - yes to all/[N]o/[P]rint):```<br>
Here you can enter ```A``` and press Enter<br>

Install sudo
------------

Also install sudo, which allows you to run command-line applications (like choco) with administration rights without opening an administrator PowerShell window:

```
choco install sudo
```
Again, you will be asked to confirm this is what you want by entering ```A``` and pressing Enter.

Install Python via Pyenv
------------------------

New CMD or POWERSHELL
```
pyenv install 3.8.5
```
```
pyenv global 3.8.5
```
```
pyenv local 3.8.5
```
Set PATH
----

New CMD or POWERSHELL

```
sudo setx /m PATH "%HOMEPATH%\.pyenv\pyenv-win\versions\3.8.5;%PATH%"
```
```
sudo setx /m PATH "%HOMEPATH%\.pyenv\pyenv-win\versions\3.8.5\Scripts;%PATH%"
```
```
sudo setx /m PATH "%HOMEPATH%\appdata\roaming\python\python38\site-packages;%PATH%"
```
```
sudo setx /m PATH "%HOMEPATH%\AppData\Roaming\Python\Python38\Scripts;%PATH%"
```

Create an Alias for Python (optional)
--------------------

The rest of this tutorial uses the command ```python3``` when executing python commands; on **macOS** you can *usually* use the commands ```python``` or ```python3``` interchangeably, but not always. 
Windows will sometimes send you to the Microsoft Store to download a different version of Python if you enter ```python3```.
To follow the rest of the tutorial verbatim, tell Windows to treat the command ```python3``` as an alias for ```python``` by entering the following command in PowerShell:
```
Set-Alias python3 python
```
Or, you can remind yourself that subsequent references to ```python3``` in this tutorial should be run as ```python``` in Windows. 

You can now close your administrative shell by typing ```exit``` and pressing Enter.

Install Requirements and Handprint
----

Download [requirements.txt](https://raw.githubusercontent.com/ccarvel/ocr-htr-tutorial/gh-pages/requirements.txt)

New CMD or POWERSHELL
```
pip install handprint
```

➩[Continue to Step 2a. Set up Microsoft Azure Cloud for text recognition and extraction](step_2a_azure.md)<br/>

{% include footer.html %}
