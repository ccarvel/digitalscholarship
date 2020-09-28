# RECOGNIZING AND EXTRACTING HANDWRITTEN TEXT USING PYTHON AND HANDPRINT
This tutorial will help you use Microsoft's Azure and/or Google's Cloud Platform (GCP) to recognize and extract handwritten text from image or PDF files.
This tutorial requires the command line and is macOS-centric. 
Linux-based systems will likely mirror the steps here--some of the commands or steps will be similar though not identical. 
Windows 10 can also execute these workflows but offers 3 routes to running Python--by using either of two Windows-based Python environments, or, by installing a Linux subsystem for Windows. For Windows 10 users, we suggest the use of a [Linux subsystem installation](https://realpython.com/installing-python/).

The goals for this tutorial are:
* 0.  Set up the **Homebrew package manager** to add **Python 3** and **PIP 3** to your command line using **pyenv**;
* 1a. Set up **Microsoft Azure Cloud** for text recognition and extraction;
* 1b. Set up **Google Cloud Platform** for text recognition and extraction;
* 2.  Set up your shell **(PATH)** for connecting to Azure and/or GCP for text recognition and extraction;
* 3.  Installing and running a Python module **(handprint)** that interacts with Azure and/or GCP and does the work of using computer vision to analyze images or PDFs containing unrecognized written material to return editable text files. 

## 0. INSTALL HOMEBREW, PYTHON, AND PIP
* Open your macOS Terminal with Spotlight by entering<br/>
```⌘ + spacebar``` and typing:<br/>
```Terminal```<br/>
to launch the Terminal command line interface.<br/>
Take note of which shell your OS is using by typing:<br/>
```echo "$SHELL"```<br/>
In most cases you'll receive a response of either:<br/>
```/bin/zsh```<br/>
or<br/>
```/bin/bash```<br/>
This tells us what PATH file to edit to ensure everything runs smoothly.

* Next, install Xcode Command Line Tools, whic are required ot install the Homebrew Package Manager<br/>
```xcode-select --install```<br/>
A prompt should appear asking you to confirm the installation of Xcode (you may need to enter your password)<br/>

* Once Xcode is installed, let's fetch and install the Homebrew Package Manager by typing:<br/>
```/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)```<br/>





## 1a.

## 1b.

## 2. 

## 3. 
