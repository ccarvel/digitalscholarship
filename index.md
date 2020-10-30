---
layout: default
title: Overview
nav_order: 1
description: "Recognizing and Extracting Handwritten Text Using Python and Handprint"
permalink: /
---
# RECOGNIZING AND EXTRACTING HANDWRITTEN TEXT USING PYTHON AND HANDPRINT
This tutorial will help you use two of the most impressive computer vision libraries available: Microsoft's Azure and/or Google's Cloud Platform (GCP) for Handwritten Text Recognition (HTR)--**to recognize and extract handwritten text from image or PDF files**. (Note: The Handprint package can also make use of Amazon's Rekognition and Textract services; we focus on Azure and GCP because their performance has, anecdotally, proven more accurate)<br/><br/>
This tutorial requires the use of **Terminal in macOS**, or **PowerShell in Windows**
**Linux-based systems** will likely work using most of the same commands. 

We will be using a Python Package called <a href="https://github.com/caltechlibrary/handprint" target="_blank">Handprint</a>, developed by the Caltech Library to perform text recognition and extraction on image files or PDF documents that contain handwriting.<br/>

**The overview of goals for this tutorial are:**<br/>
If you are using a **Mac**, start here:<br/>
[⓵. Set up the **Homebrew package manager** to add **Python 3** and **PIP 3** to your command line (Terminal) using **pyenv**](step_1_cli.md);<br/><br/>
If you are using **Windows**, start here:<br/>
[⓵ⓐ. Set up **Chocolatey package manager** to add **Python 3** and **PIP 3** to your command line (PowerShell) using **anaconda**](step_1a_win_cli.md);<br/><br/>
[⓶ⓐ. Set up **Microsoft Azure Cloud** for text recognition and extraction](step_2a_azure.md);<br/><br/>
[⓶ⓑ. Set up **Google Cloud Platform** for text recognition and extraction](step_2b_gcp.md);<br/><br/>
[⓷. Installing and running a Python module **(handprint)** that interacts with Azure and/or GCP and does the work of using computer vision to analyze images or PDFs containing unrecognized written material to return editable text files](step_3_handprint.md)<br/>
 
{% include footer.html %}
