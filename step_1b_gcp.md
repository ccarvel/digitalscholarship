To enable the use of the Google OCR API, first you must create the necessary credentials in [Google Cloud Platform (GCP)](https://cloud.google.com/docs/overview/#projects).  There is an summary of this process in the Google documentation under the section on [Creating a service account](https://cloud.google.com/docs/authentication/getting-started); what follows below is a walk through with screenshots for better clarity.

## 1.  Create a project in Google GCP

Visit the [Google GCP page for creating service accounts](https://console.cloud.google.com/apis/credentials/serviceaccountkey).  Click the project pull-down menu in the top blue bar, located in-between the name "Google Cloud Platform" and search field &ndash; look for the small white down arrow in the screenshot below:

<p align="center">
<img  width="500px" src="https://github.com/ccarvel/handprint/raw/master/.graphics/google-gcp-create-service-account-key.png">
</p>

This will generate a pop-up dialog in which you can select an existing project or create a new one.  It's probably best to create a new project, so click the "New project" link in the upper right of the pop-up:

<p align="center">
<img  width="500px" src="https://github.com/ccarvel/handprint/raw/master/.graphics/google-select-project.png">
</p>

In the page that is presented next, give the project a name that makes sense for your needs, and leave the rest of the fields as they are. Click the **Create** button at the bottom.

<p align="center">
<img  width="500px" src="https://github.com/ccarvel/handprint/raw/master/.graphics/google-gcp-new-project.png">
</p>


## 2. Create a service account key

The next page should look something like this:

<p align="center">
<img  width="500px" src="https://github.com/ccarvel/handprint/raw/master/.graphics/google-gcp-create-service-account-key.png">
</p>

Click on the "Select..." button and select "New service account", which should be the only option in the pop-up menu anyway.  Give this new service account a name in the "Service account name" field, and then under "Role", click the "Select a role" button and pick "Project"&nbsp;**>**&nbsp;"Owner" as the role.  Finally, click the **Create** button at the bottom.

<p align="center">
<img  width="500px" src="https://github.com/ccarvel/handprint/raw/master/.graphics/google-gcp-role.png">
</p>


## 3. Rename the JSON file

The previous step should have resulted in a JSON file being downloaded to your computer.  Check that the file contents look something like this:

```
{
  "type": "service_account",
  "project_id": "my-project-1533599323905",
  "private_key_id": "79e2e3c5ca55989a86001f0463bd159711b73042",
  "private_key": "-----BEGIN PRIVATE KEY-----\nMIIEvgIBADANBgkqhkiG9w0BAQEFAASCBKgwggSkAgEAAoIBAQDYnY25oavHUuy1\nkNm7aSfvf6Dv4WFow5ZCedwTAF4hF+3e9rXfpx7FnmC0MwyvzuGVyTfgqGw8XdIF\nk5WdsqQWrssZQ0oFrRNOfLjRCVukK6vuoSAqG+FNL06nIIqS+XrC/lrHM/psrewU\njBTYSIjJVD2EUZIHj5APwfoDAZEejZw5vExNckXkQ4gCSdK43DAKvJXIE6/I2BA1\nAqYxzTiXGHXDr0cdVWZToj/jkuLPph8IT4KZhZJQLolmVTUsrEpYVNyoK7ftRuYg\naJFPOji4GU/l44MHXCVL6GG7L42gkQyKaJ1i3RBvSq2osQ3TGWyihOhABJ57iwGn\ndr+erELVAgMBAAECggEAGY7JXIgnQO7XT/rlvbeEBz2LSxJQEHDXR0OihDlsYcI1\nhjOctOU+e7mallhZnFqwAiDKL38fuiWltJO7uO4Nb0GzY+ktECtiFkYf9kYA4odm\nk1K+fUlp1VYKFS0BPKMj6WLiahOHbhA9RRVcFkLEpOCEG5sWPD8jk8Bi07z5Ft4N\n0rrU7tzA5NgMtva1EGv7777xnldQ7DUL6zc/jY106fLU9wOiFEiCaIqpa8brS76o\nASFgDfWczVe1d/GTMkKbbCtJdMc8ijjSAwM10VRXO97XeLT2C3f7IAk2HnASgX3/\nh5SdsRy2/Ct3RbeuZQUQ/Qde5Na/aUyJLJXm8gQ8cQKBgQD5Mnjo/lcqKvsTDVJI\nvLr/KTw77HYb3hyyRd39G5mnQBJTz4q6mQejC1AmAbss3UYOEEniw+ZVFlQ85jMJ\nJZQlu/LeFE5YwRDiz3biIUlzQAbtGYlKmbJ4TRRdodtKXDK0tL/7b7FiQZqx5I3Q\n+1sUbNArSq/yACDPNLs3WPqTTQKBgQDeh2Hbh9yYARgRqyQRKBPevBgq75CO2cx2\naHmSMyc4TT/O07pOLdeDyBQPTnjXFNuYzCSBz9bd6ZFezbwhq7E9iAPZujI/ZC7a\nplYWQb/z9fmtQRtGkUCCGs8cbXsZYnI04zYSxWL/vc3MWdDllSItsn2zRIBiH0ee\nH+3rkBiZqQKBgQDs0/btF6snPCnZdXOaBSOClGHWYWfuHC0RkCzk+3IP7Wh9lmS1\n6fHEFmBZfpOwk6qcewZ9KMiiXNI5/lzKeJhPNEwgmxPKbdHqfFjzl8cCbPsoInjE\nGUXv5vFP+x85kF3wN0etYf0m8EpgfmH5Fqj8xF0ih5ynVU/ZHLhAZaPekQKBgE1G\nKf838KyARMFt8rpadnv0SVgvlL1meI/tu7m/NbFhcfT6pUmctag3hG/ESkY2IgOv\ncEX7zJuHDkojm1795jB92Qh0lhpZScP32xEjh+rJ0ggOAdDBg+sqMB2pDwRDoXEo\nLZDbJoO0f5Ck59uxrAq+XtQvx31La21HnTEd+szxAoGBAKLq8g/VFInAhTzKkRZk\n7WP7yDGpWvdZg+4I/Eyp1PSnsw2TumG3EnjubBHybimNnf3f3zaPbA2i9p1SEQC+\n8SPW41QDkR2LqcZ9HZs4NW7gBlMQ99R7elrEzPjhUu4qg35B2+ZbAMLY2MttZqdM\ndAa2iAJpYkumjMqjZBR//HL0\n-----END PRIVATE KEY-----\n",
  "client_email": "handprint-demo-916@my-project-1533599323905.iam.gserviceaccount.com",
  "client_id": "101550716014308063202",
  "auth_uri": "https://accounts.google.com/o/oauth2/auth",
  "token_uri": "https://oauth2.googleapis.com/token",
  "auth_provider_x509_cert_url": "https://www.googleapis.com/oauth2/v1/certs",
  "client_x509_cert_url": "https://www.googleapis.com/robot/v1/metadata/x509/handprint-demo-916%40my-project-1533599323905.iam.gserviceaccount.com"
}
```


Rename the JSON file to `google_credentials.json` and move that file into the credentials directory used by Handprint. As described in the [README file](https://github.com/ccarvel/handprint), by default, Handprint looks for credentials in a directory named `creds` within the directory where Handprint is installed, but you can use another directory if you run `handprint` with the `-c` option.


## 4. Enable billing

Billing needs to enabled before the account can be used for accessing Google cloud API resources.  Go back to the [GCP dashboard]() and look for the "Billing" option in the left-hand list:

<p align="center">
<img  width="500px" src="https://github.com/ccarvel/handprint/raw/master/.graphics/google-gcp-billing.png">
</p>

The page that comes next will probably say that there is no billing account associated with the project:

<p align="center">
<img  width="500px" src="https://github.com/ccarvel/handprint/raw/master/.graphics/google-gcp-no-billing.png">
</p>

Click "Manage billing accounts".  The next screen should look like this:

<p align="center">
<img  width="500px" src="https://github.com/ccarvel/handprint/raw/master/.graphics/google-gcp-add-billing-account.png">
</p>

Click "Add billing account". Sign up for $300 of free credit:

<p align="center">
<img  width="600px" src="https://github.com/ccarvel/handprint/raw/master/.graphics/google-gcp-free.png">
</p>

In the next screen that follows after that one, which will contain a form for filling in your account information, select "Individual" as the "Account type", and fill in the rest with information such as address and a credit card.  The card will not be charged even after the free trial ends; Google does not autocharge but rather uses the card as a way to weed out robots.
