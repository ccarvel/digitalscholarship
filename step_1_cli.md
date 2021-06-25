---
layout: default
title: 1. Install Homebrew, Python3 and Pip3 on a Mac
nav_order: 2
---

## 1. INSTALL HOMEBREW, PYTHON, AND PIP ON A MAC
To do this we have to install XCode, which is the Macintosh developer tool package and Homebrew which is a common package manager that handles installation and update of mostly open source software. If you are familiar with other package managers, they will work as well.

* Open your macOS Terminal with Spotlight by entering<br/>
```⌘ + spacebar``` and typing:<br/>
```Terminal```<br/>
to launch the Terminal command line interface.<br/><br/>

* Next, install Xcode Command Line Tools, whic are required to install the Homebrew Package Manager<br/>
{% include codeHeader.html %}
```xcode-select --install
```
<br/>
A prompt should appear asking you to confirm the installation of Xcode (you may need to enter your password)<br/>

* Once Xcode is installed, let's fetch and install the Homebrew Package Manager by typing:<br/>
{% include codeHeader.html %}
```/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)
```<br/>

* Once brew is installed, let's install **pyenv** which will let us up to date Python and Pip packages to run our recognition program; it will also allow us to run different versions of the Python language if we need to::<br/>
{% include codeHeader.html %}
```brew install pyenv```<br/>

* Now let's install the latest Python and Pip software using **pyenv**:<br/>
{% include codeHeader.html %}
```pyenv install 3.8.5```<br/>

* And let's make this version of Python the default:<br/>
{% include codeHeader.html %}
```pyenv global 3.8.5```<br/>

* We now need to add this information to our PATH to ensure we'll be using this version of Python in Terminal:<br/>
Take note of which shell your OS is using by typing:<br/>
{% include codeHeader.html %}
```echo "$SHELL"```<br/>
In most cases you'll receive a response of either:<br/>
```/bin/zsh```<br/>
or<br/>
```/bin/bash```<br/>
This tells us what PATH file to edit to ensure everything runs smoothly.<br/>

* If you saw:<br/>
```/bin/zsh```<br/>
Enter:<br/>
{% include codeHeader.html %}
```echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n  eval "$(pyenv init -)"\nfi' >> ~/.zshrc```<br/>
or<br/>
If you saw:<br/>
```/bin/bash```<br/>
Enter:<br/>
{% include codeHeader.html %}
```echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n  eval "$(pyenv init -)"\nfi' >> ~/.bash_profile```<br/>

* Start a New Shell by typing:<br/>
```⌘N```<br/>

Install Requirements and Handprint
----

Download [requirements.txt](https://raw.githubusercontent.com/ccarvel/ocr-htr-tutorial/gh-pages/requirements.txt)

In macOS Terminal
{% include codeHeader.html %}
```
pip install -r requirements.txt
```
{% include codeHeader.html %}
```
pip install handprint
```

➩[Continue to Step 2a. Set up Microsoft Azure Cloud for text recognition and extraction](step_2a_azure.md)<br/>

{% include footer.html %}
