---
layout: default
title: 1. Install Homebrew, Python3 and Pip3 on a Mac
nav_order: 2
---

## 1. INSTALL HOMEBREW, PYTHON, AND PIP ON A MAC
To do this we have to install XCode, which is the Macintosh developer tool package and Homebrew which is a common package manager that handles installation and update of mostly open source software. If you are familiar with other package managers, they will work as well.

* Open your macOS Terminal with Spotlight by entering<br/>
```⌘ + spacebar``` and typing:<br/>
```Terminal```
to launch the Terminal command line interface.<br/>

* Next, install Xcode Command Line Tools, whic are required to install the Homebrew Package Manager<br/>
<input id=code001 value="xcode-select --install"> 
<button class="btn" data-clipboard-target="#code001">
  <img src="assets/clippy.svg" alt="Copy to clipboard">
  </button>

A prompt should appear asking you to confirm the installation of Xcode (you may need to enter your password)<br/>

* Once Xcode is installed, let's fetch and install the Homebrew Package Manager by typing:<br/>
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)
```
* Once brew is installed, let's install **pyenv** which will let us manage python and its PyPip (pip) packages to run our recognition program; it will also allow us to run different versions of the Python language if we need to::<br/>
```
brew install pyenv
```
* Now let's install the latest Python and Pip software using **pyenv**:<br/>
```
pyenv install 3.8.5
```

* And let's make this version of Python the default:<br/>
```
pyenv global 3.8.5
```
```
pyenv local 3.8.5
```

* We now need to add this information to our PATH to ensure we'll be using this version of Python in Terminal:<br/>
Take note of which shell your OS is using by typing:<br/>
```
echo "$SHELL"
```
In most cases you'll receive a response of either:<br/>
```
/bin/zsh
```
or<br/>
```
/bin/bash
```
This tells us what PATH file to edit to ensure everything runs smoothly.<br/>

* If you saw:<br/>
```
/bin/zsh
```
Enter:
<br/>
```
echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n  eval "$(pyenv init -)"\nfi' >> ~/.zshrc
```
or
<br/>
If you saw:
<br/>
```
/bin/bash
```
Enter:<br/>
```
echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n  eval "$(pyenv init -)"\nfi' >> ~/.bash_profile
```

* Start a New Shell by typing:<br/>
```
⌘N
```

Install Requirements and Handprint
----

Download [requirements.txt](https://raw.githubusercontent.com/ccarvel/ocr-htr-tutorial/gh-pages/requirements.txt)

In macOS Terminal
```
pip3 install -r requirements.txt
```
```
pip3 install handprint
```

=======
➩[Continue to Step 2a. Set up Microsoft Azure Cloud for text recognition and extraction](step_2a_azure.md)<br/>

{% include footer.html %}
