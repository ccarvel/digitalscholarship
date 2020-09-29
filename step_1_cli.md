## 1. INSTALL HOMEBREW, PYTHON, AND PIP
Open your macOS Terminal with Spotlight by entering<br/>
```⌘ + spacebar``` and typing:<br/>
```Terminal```<br/>
to launch the Terminal command line interface.<br/><br/>

* Next, install Xcode Command Line Tools, whic are required ot install the Homebrew Package Manager<br/>
```xcode-select --install```<br/>
A prompt should appear asking you to confirm the installation of Xcode (you may need to enter your password)<br/>

* Once Xcode is installed, let's fetch and install the Homebrew Package Manager by typing:<br/>
```/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)```<br/>

* Once brew is installed, let's install **pyenv** which will let us up to date Python and Pip packages to run our recognition program; it will also allow us to run different versions of the Python language if we need to::<br/>
```brew install pyenv```<br/>

* Now let's install the latest Python and Pip software using **pyenv**:<br/>
```pyenv install 3.8.5```<br/>

* And let's make this version of Python the default:<br/>
```pyenv global 3.8.5```<br/>

* We now need to add this information to our PATH to ensure we'll be using this version of Python in Terminal:<br/>
Take note of which shell your OS is using by typing:<br/>
```echo "$SHELL"```<br/>
In most cases you'll receive a response of either:<br/>
```/bin/zsh```<br/>
or<br/>
```/bin/bash```<br/>
This tells us what PATH file to edit to ensure everything runs smoothly.<br/>

* If you saw:<br/>
```/bin/zsh```<br/>
Enter:<br/>
```echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n  eval "$(pyenv init -)"\nfi' >> ~/.zshrc```<br/>
or<br/>
If you saw:<br/>
```/bin/bash```<br/>
Enter:<br/>
```echo -e 'if command -v pyenv 1>/dev/null 2>&1; then\n  eval "$(pyenv init -)"\nfi' >> ~/.bash_profile```<br/>

* Start a New Shell by typing:<br/>
```⌘N```<br/>

➩[Continue to Step 2a. Set up Microsoft Azure Cloud for text recognition and extraction](step_2a_azure.md)<br/>

{% include footer.html %}
