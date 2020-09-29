# RECOGNIZING AND EXTRACTING HANDWRITTEN TEXT USING PYTHON AND HANDPRINT
This tutorial will help you use Microsoft's Azure and/or Google's Cloud Platform (GCP) to recognize and extract handwritten text from image or PDF files.
This tutorial requires the command line and is macOS-centric. 
Linux-based systems will likely mirror the steps here--some of the commands or steps will be similar though not identical. 
Windows 10 can also execute these workflows but offers 3 routes to running Python--by using either of two Windows-based Python environments, or, by installing a Linux subsystem for Windows. For Windows 10 users, we suggest the use of a <a href="https://realpython.com/installing-python/">Linux subsystem installation</a>.<br/></p>

We will be using a Python Package called <a href="https://github.com/caltechlibrary/handprint" target="_blank">Handprint</a>, developed by the Caltech Library to perform text recognition and extraction on image files or PDF documents that contain handwriting.

**The overview of goals for this tutorial are:**<br/>
[⓵. Set up the **Homebrew package manager** to add **Python 3** and **PIP 3** to your command line using **pyenv**](step_1_cli.md);<br/>
[⓶ⓐ. Set up **Microsoft Azure Cloud** for text recognition and extraction](step_2a_azure.md);<br/>
[⓶ⓑ. Set up **Google Cloud Platform** for text recognition and extraction](step_2b_gcp.md);<br/>
[⓷. Installing and running a Python module **(handprint)** that interacts with Azure and/or GCP and does the work of using computer vision to analyze images or PDFs containing unrecognized written material to return editable text files](step_3_handprint.md)<br/>
 
{% include footer.md %}
