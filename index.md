# RECOGNIZING AND EXTRACTING HANDWRITTEN TEXT USING PYTHON AND HANDPRINT
This tutorial will help you use Microsoft's Azure and/or Google's Cloud Platform (GCP) to recognize and extract handwritten text from image or PDF files.
This tutorial requires the command line and is macOS-centric. 
Linux-based systems will likely mirror the steps here--some of the commands or steps will be similar though not identical. 
Windows 10 can also execute these workflows but offers 3 routes to running Python--by using either of two Windows-based Python environments, or, by installing a Linux subsystem for Windows. For Windows 10 users, we suggest the use of a [Linux subsystem installation](https://realpython.com/installing-python/).

**The overview of goals for this tutorial are:**
* 0.  Set up the **Homebrew package manager** to add **Python 3** and **PIP 3** to your command line using **pyenv**;
* 1a. Set up **Microsoft Azure Cloud** for text recognition and extraction;
* 1b. Set up **Google Cloud Platform** for text recognition and extraction;
* 2.  Set up your shell **(PATH)** for connecting to Azure and/or GCP for text recognition and extraction;
* 3.  Installing and running a Python module **(handprint)** that interacts with Azure and/or GCP and does the work of using computer vision to analyze images or PDFs containing unrecognized written material to return editable text files. 

## 0. INSTALL HOMEBREW, PYTHON, AND PIP
* Open your macOS Terminal with Spotlight by entering<br/>
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

## 1a. Set up **Microsoft Azure Cloud** for text recognition and extraction
To sign up for Azure and obtain a key, visit [https://portal.azure.com](https://portal.azure.com) and create a new account.  (Note: you will need to turn off browser security plugins such as Ad&nbsp;Block and uMatrix if you have them, or else the site will not work.)  If you use your Caltech Access login, the Azure portal will redirect you to the regular Caltech Access login page and then (after you log in) back to the Microsoft Azure Dashboard [https://portal.azure.com](https://portal.azure.com), from where you can create credentials.  Otherwise, if you create a new account, after going through the various screens, you will also end up on the Dashboard page.

Before you create any service accounts, the Microsoft Azure Dashboard looks somewhat like this:

<p align="center">
<img alt="Azure Dashboard" src="https://github.com/ccarvel/handprint/raw/master/.graphics/azure-no-resources.png">
</p>

To create a service account, first click on the blue **Create Resources** button.  This will lead to a page where you select resources that looks somewhat like this:

<p align="center">
<img alt="Create Azure resource" src="https://github.com/ccarvel/handprint/raw/master/.graphics/azure-create-resource.png">
</p>

Click **AI + Machine Learning**; this will bring up a list of "Featured" options in the right-hand column (the things with the blue squares in the screen capture above), and there look for **Computer Vision**.  Click on that one.  The next page will look somewhat like this:

<p align="center">
<img alt="Azure Dashboard" src="https://github.com/ccarvel/handprint/raw/master/.graphics/azure-start-free-account.png">
</p>

Click **Start Free**, then click through to fill out account information and identification.  It will require a phone number and a credit card, but you won't be charged anything.

After all that's done, you will once again be put back to the Portal Dashboard.  Click on **Create Resources** again, select **AI + Machine Learning** followed by **Computer Vision** again, and this time the following form will appear:

<p align="center">
<img src="https://github.com/ccarvel/handprint/raw/master/.graphics/azure-create-computer-vision.png">
</p>

Fill in the blanks in this form. Give the service a name (for your own organizational purposes), keep the "Free Trial", and for the location, make sure to select `West US`.  For the pricing tier, select the F0 free option.  For the "Resource group", click on the "Create new" link below the blank and create a new resource name &ndash; it can be anything that makes sense, such as "Handprint" or "OCR test" or whatever.

Finally, after the form is done, you should be able to click on the resource name in your Azure Dashboard.  This should lead to a page that looks somewhat like this:

<p align="center">
<img src="https://github.com/ccarvel/handprint/raw/master/.graphics/azure-get-keys.png">
</p>

Double-check that the API endpoint begins with `https://westus.api.cognitive.microsoft.com` in Section 2 and then click on the **Keys** link in Section 1. The key will be a string such as `"18de248475134eb49ae4a4e94b93461c"`. The next page will provide two keys.  You can copy either one and use it in the `microsoft.json` file described in the [instructions for installing Handprint](https://github.com/ccarvel/handprint).

## 1b.

## 2. 

## 3. 
