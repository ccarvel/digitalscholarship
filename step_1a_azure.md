## 1a. Set up **Microsoft Azure Cloud** for text recognition and extraction
To sign up for Azure and obtain a key, visit [https://portal.azure.com](https://portal.azure.com) and create a new account.  (Note: you will need to turn off browser security plugins such as Ad&nbsp;Block and uMatrix if you have them, or else the site will not work.)  You can use a version of your Brown Credentials to login to Azure by entering your MyAccount username plus @ad.brown.edu (ex. jcarberry@ad.brown.edu). You will then be redirected to the Microsoft Azure Dashboard [https://portal.azure.com](https://portal.azure.com), from where you can create credentials. Otherwise, if you create a new account, after going through the various screens, you will also end up on the Dashboard page.

Before you create any service accounts, the Microsoft Azure Dashboard looks somewhat like this:

<p align="center">
<img alt="Azure Dashboard" src="https://github.com/ccarvel/handprint/raw/master/.graphics/01_azure_dashboard.png">

</p>

To create a service account, first click on the green **Create Resources** button.  This will lead to a page where you select resources that looks somewhat like this:

<p align="center">
<img alt="Create Azure resource" src="https://github.com/ccarvel/handprint/raw/master/.graphics/03_azure_ai_machine.png">
</p>

Click **AI + Machine Learning**; this will bring up a list of "Featured" options in the right-hand column (the things with the blue squares in the screen capture above), and there look for **Computer Vision**.  Click on that one.  The next page will look somewhat like this:

<p align="center">
<img alt="Azure Dashboard" src="https://github.com/ccarvel/handprint/raw/master/.graphics/azure-start-free-account.png">
</p>

Click **Start Free**, then click through to fill out account information and identification.  It will require a phone number and a credit card, but you won't be charged anything.

After all that's done, you will once again be put back to the Portal Dashboard.  Click on **Create Resources** again, select **AI + Machine Learning** followed by **Computer Vision** again, and this time the following form will appear:

<p align="center">
<img src="https://github.com/ccarvel/handprint/raw/master/.graphics/05_azure_create_cv.png">
</p>

Fill in the blanks in this form. Give the service a name (for your own organizational purposes), keep the "Free Trial", and for the location, make sure to select `West US`.  For the pricing tier, select the F0 free option.  For the "Resource group", click on the "Create new" link below the blank and create a new resource name &ndash; it can be anything that makes sense, such as "Handprint" or "OCR test" or whatever.

Finally, after the form is done, you should be able to click on the resource name in your Azure Dashboard.  This should lead to a page that looks somewhat like this:

<p align="center">
<img src="https://github.com/ccarvel/handprint/raw/master/.graphics/azure-get-keys.png">
</p>

Double-check what the API endpoint begins with (this *should* be https://westus.api.cognitive.microsoft.com) in Section 2 and then click on the **Keys** link in Section 1. The key will be a string such as `"18de248475134eb49ae4a4e94b93461c"`. The next page will provide two keys.  You can copy either one and save it in a file `microsoft.json`.
