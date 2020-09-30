---
layout: default
title: Overview
nav_order: 1
description: "Recognizing and Extracting Handwritten Text Using Python and Handprint"
permalink: /
---
# RECOGNIZING AND EXTRACTING HANDWRITTEN TEXT USING PYTHON AND HANDPRINT
This tutorial will help you use two of the most impressive computer vision libraries available: Microsoft's Azure and/or Google's Cloud Platform (GCP) for Handwritten Text Recognition (HTR)--**to recognize and extract handwritten text from image or PDF files**. (Note: The Handprint package can also make use of Amazon's Rekognition and Textract services; we focus on Azure and GCP because their performance has, anecdotally, proven more accurate)<br/><br/>
This tutorial requires the command line and is **macOS-centric**. 
**Linux-based systems** will likely mirror the steps here--some of the commands or steps will be similar though not identical. 
**Windows 10** can also perform these operations but offers a few routes to running Python--for Windows 10 users, we suggest the use of a **<a href="https://realpython.com/installing-python/#how-to-install-python-on-windows" target="_blank">Linux subsystem installation</a>**.<br/>

We will be using a Python Package called <a href="https://github.com/caltechlibrary/handprint" target="_blank">Handprint</a>, developed by the Caltech Library to perform text recognition and extraction on image files or PDF documents that contain handwriting.<br/>

**The overview of goals for this tutorial are:**<br/>
[⓵. Set up the **Homebrew package manager** to add **Python 3** and **PIP 3** to your command line using **pyenv**](step_1_cli.md);<br/><br/>
[⓶ⓐ. Set up **Microsoft Azure Cloud** for text recognition and extraction](step_2a_azure.md);<br/><br/>
[⓶ⓑ. Set up **Google Cloud Platform** for text recognition and extraction](step_2b_gcp.md);<br/><br/>
[⓷. Installing and running a Python module **(handprint)** that interacts with Azure and/or GCP and does the work of using computer vision to analyze images or PDFs containing unrecognized written material to return editable text files](step_3_handprint.md)<br/>
 
{% include footer.html %}
