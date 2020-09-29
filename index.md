# RECOGNIZING AND EXTRACTING HANDWRITTEN TEXT USING PYTHON AND HANDPRINT
This tutorial will help you use Microsoft's Azure and/or Google's Cloud Platform (GCP) to recognize and extract handwritten text from image or PDF files.
This tutorial requires the command line and is macOS-centric. 
Linux-based systems will likely mirror the steps here--some of the commands or steps will be similar though not identical. 
Windows 10 can also execute these workflows but offers 3 routes to running Python--by using either of two Windows-based Python environments, or, by installing a Linux subsystem for Windows. For Windows 10 users, we suggest the use of a [Linux subsystem installation](https://realpython.com/installing-python/).<br/>

We will be using a Python Package called [Handprint](https://github.com/caltechlibrary/handprint), developed by the Caltech Library to perform text recognition and extraction on image files or PDF documents that contain handwriting.

**The overview of goals for this tutorial are:**<br/>
[⓵. Set up the **Homebrew package manager** to add **Python 3** and **PIP 3** to your command line using **pyenv**](step_1_cli.md);<br/>
[⓶ⓐ. Set up **Microsoft Azure Cloud** for text recognition and extraction](step_2a_azure.md);<br/>
[⓶ⓑ. Set up **Google Cloud Platform** for text recognition and extraction](step_2b_gcp.md);<br/>
[⓷. Installing and running a Python module **(handprint)** that interacts with Azure and/or GCP and does the work of using computer vision to analyze images or PDFs containing unrecognized written material to return editable text files](step_3_handprint.md)
    
<h1 id="recognizing-and-extracting-handwritten-text-using-python-and-handprint">RECOGNIZING AND EXTRACTING HANDWRITTEN TEXT USING PYTHON AND HANDPRINT</h1>
<p>This tutorial will help you use Microsoft&#39;s Azure and/or Google&#39;s Cloud Platform (GCP) to recognize and extract handwritten text from image or PDF files.
This tutorial requires the command line and is macOS-centric. 
Linux-based systems will likely mirror the steps here--some of the commands or steps will be similar though not identical. 
Windows 10 can also execute these workflows but offers 3 routes to running Python--by using either of two Windows-based Python environments, or, by installing a Linux subsystem for Windows. For Windows 10 users, we suggest the use of a <a href="https://realpython.com/installing-python/">Linux subsystem installation</a>.<br/></p>
<p>We will be using a Python Package called <a href="https://github.com/caltechlibrary/handprint" target="_blank">Handprint</a>, developed by the Caltech Library to perform text recognition and extraction on image files or PDF documents that contain handwriting.</p>
<p><strong>The overview of goals for this tutorial are:</strong><br/>
<a href="step_1_cli.md">⓵. Set up the <strong>Homebrew package manager</strong> to add <strong>Python 3</strong> and <strong>PIP 3</strong> to your command line using <strong>pyenv</strong></a>;<br/>
<a href="step_2a_azure.md">⓶ⓐ. Set up <strong>Microsoft Azure Cloud</strong> for text recognition and extraction</a>;<br/>
<a href="step_2b_gcp.md">⓶ⓑ. Set up <strong>Google Cloud Platform</strong> for text recognition and extraction</a>;<br/>
<a href="step_3_handprint.md">⓷. Installing and running a Python module <strong>(handprint)</strong> that interacts with Azure and/or GCP and does the work of using computer vision to analyze images or PDFs containing unrecognized written material to return editable text files</a></p>
