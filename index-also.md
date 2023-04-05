---
layout: default
title: Overview
nav_order: 1
description: "Digital Scholarship at Brown: Signing up, setting up, installing an application"
permalink: /
---
**If you have any questions or have an issues, please [email me](mailto:cody_carvel@brown.edu)**<br/>
### SIGNING UP FOR DIGITAL SCHOLARSHIP HOSTING SERVICES AT BROWN

1. Go to [the Digital Scholarship landing page](https://digitalscholarship.brown.edu/) <br/>
![](https://raw.githubusercontent.com/ccarvel/digitalscholarship/gh-pages/assets/images/00_sign-up.png)
2. Click Sign Up
3. Fill out the form, register with your brown email address. 
4. The form will then be submitted for approval.
5. Once approved, you'll get a link to choose a subdomain:
	* yourdomain.digitalscholarship.brown.edu
	* I suggest choosing something memorable; shorter is better (30 characters or less)
6. Once you've chosen your subdomain and submitted it, you can login by going to: 
	* [the Digital Scholarship landing page](https://digitalscholarship.brown.edu/){:target="_blank" rel="noopener"}
	* You will then be asked to enter your brown credentials via shibboleth. <br/>
	![](https://raw.githubusercontent.com/ccarvel/digitalscholarship/gh-pages/assets/images/02-shib.png)
7. Once authenticated you'll be brought to the cpanel dashboard:<br/>
![](https://raw.githubusercontent.com/ccarvel/digitalscholarship/gh-pages/assets/images/03-dashboard.png)

8. You will want to install a security certificate on your domain. This will make accessing your site easier and help you avoid seeing warnings from your browser about your site being unsafe--this is what adds the little lock on the url bar and makes your site an https:// site and not simply an http:// site--[instructions from Reclaim are here](https://support.reclaimhosting.com/hc/en-us/articles/4405723680023-Installing-Free-SSL-Certificates#installing-free-ssl-certificates-0-0){:target="_blank" rel="noopener"}

### INSTALLING OMEKA, SCALAR, OR ANOTHER APPLICATION--Do I need another subdomain?
- Do you want to install to your current subdomain or create another subdomain for your application?

You can either install your choice of app into the subdomain you picked and issued your security certificate for
(yourdomain.digitalscholarship.brown.edu) <br/>
or you can create another subdomain (a subdomain of your subdomain) to install to<br/>
eg-- omeka.yourdomain.digitalscholarship.brown.edu

Creating an additional subdomain has the benefit of keeping your space on the server more orderly. I tend to create a subdomain for each application I install. If you think you will only need to use your digitalscholarship space for a single application you can skip the creation of another subdomain.

### TO CREATE ADDITIONAL SUBDOMAINS:

1. [See here for Reclaim's guide](https://support.reclaimhosting.com/hc/en-us/articles/1500013046121-Creating-and-Managing-Subdomains){:target="_blank" rel="noopener"}

2. You should then install a security certificate to that subdomain. Again, [Reclaim's instructions are here](https://support.reclaimhosting.com/hc/en-us/articles/4405723680023-Installing-Free-SSL-Certificates#installing-free-ssl-certificates-0-0){:target="_blank" rel="noopener"}.


### INSTALL YOUR APPLICATION (Omeka Classic)
- Reclaim has a [guide for installing Omeka here](https://support.reclaimhosting.com/hc/en-us/articles/1500005712342-Installing-Omeka-Classic-on-Reclaim-Hosting#:~:text=After%20logging%20into%20your%20cPanel,and%20click%20Install%20this%20Application.&text=By%20default%20our%20automated%20installer,up%2Dto%2Ddate%20automatically)

1. On your main cpanel dashboard, select 'All Applications' to see what you can install. We will work with Omeka Classic for this tutorial.<br/>
![](https://raw.githubusercontent.com/ccarvel/digitalscholarship/gh-pages/assets/images/05-applications.png)

2. Choose the red Omeka icon.<br/>
![](https://raw.githubusercontent.com/ccarvel/digitalscholarship/gh-pages/assets/images/06-omeka.png)

3. Click 'Install this Application'<br/>
![](https://raw.githubusercontent.com/ccarvel/digitalscholarship/gh-pages/assets/images/07-install_01.png)

4. Choose the subdomain you want to install to (one that begins with https://)<br/>

5. Fill out the rest of the form's required fields:<br/>
	* choose a version--3.1; 
	* accept the EULA;
	* choose whether to automatically update;
	* choose whether to enable automatic backups;
	* choose an administrator name;
	* choose an administrator password;
	* choose an administrator email;
	* give your site a title;

	* Under Advanced Settings Management, I recommend you select:
		* 'Automatically manage advanced settings for me.' 

	* Then click **install** at the lower right. <br/>

Installation should take a minute or two.

Once installation is complete you can login to your Omeka site using the admin username and password you set. Some form of the urls below should get you to your login screen.

yourdomain.digitalscholarship.brown.edu/admin/users/login <br/>
or<br/>
www.yourdomain.digitalscholarship.brown.edu/admin/users/login<br/>


### POST-INSTALLATION TASKS FOR OMEKA CLASSIC

* [Set up Imagemagick--to help process any images you might add to your site](https://support.reclaimhosting.com/hc/en-us/articles/1500005621461-ImageMagick-in-Omeka-Classic){:target="_blank" rel="noopener"}

* Install Escher, a plugin for easily installing plugins and themes:<br/>
	* [Download the Escher plugin zip file](https://drive.google.com/file/d/1hSzAWkgx8IlWQKaGuSxFi7sCR-Q0HIMa/view?usp=share_link){:target="_blank" rel="noopener"}
	* Follow the directions for adding the zip file and extracting it as [explained here](https://support.reclaimhosting.com/hc/en-us/articles/1500005711142-Managing-Plugins-and-Themes-in-Omeka-and-Omeka-S){:target="_blank" rel="noopener"}<br/>

* [Optional] [Set your php-cli path](https://support.reclaimhosting.com/hc/en-us/articles/1500007923562-Setting-the-PHP-CLI-path-in-Omeka){:target="_blank" rel="noopener"}
 
{% include footer.html %}
