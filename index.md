# RECOGNIZING AND EXTRACTING HANDWRITTEN TEXT USING PYTHON AND HANDPRINT
This tutorial will help you use Microsoft's Azure and/or Google's Cloud Platform (GCP) to recognize and extract handwritten text from image or PDF files.
This tutorial requires the command line and is macOS-centric. 
Linux-based systems will likely mirror the steps here--some of the commands or steps will be similar though not identical. 
Windows 10 can also execute these workflows but offers 3 routes to running Python--by using either of two Windows-based Python environments, or, by installing a Linux subsystem for Windows. For Windows 10 users, we suggest the use of a [Linux subsystem installation](https://realpython.com/installing-python/).

**The overview of goals for this tutorial are:**<br/>
* [0. Set up the **Homebrew package manager** to add **Python 3** and **PIP 3** to your command line using **pyenv**](step_0_cli.md);<br/>
* 1a. Set up **Microsoft Azure Cloud** for text recognition and extraction;<br/>
* 1b. Set up **Google Cloud Platform** for text recognition and extraction;<br/>
* 2. Set up your shell **(PATH)** for connecting to Azure and/or GCP for text recognition and extraction;<br/>
* 3. Installing and running a Python module **(handprint)** that interacts with Azure and/or GCP and does the work of using computer vision to analyze images or PDFs containing unrecognized written material to return editable text files. 
