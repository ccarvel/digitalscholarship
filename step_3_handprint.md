---
layout: default
title: "3. Install and Run Handprint: A Python Package for Handwritten Text Recognition"
nav_order: 4
---
## 3. Install and Run Handprint: A Python Package for Handwritten Text Recognition
You can find detailed background and installation instructions for Handprint in the [Handprint Repo](https://github.com/caltechlibrary/handprint)<br>

1. <a href="https://github.com/caltechlibrary/handprint/blob/master/README.md#-installation-and-configuration" target="_blank">Install and Configure</a><br>
2. <a href="https://github.com/caltechlibrary/handprint/blob/master/README.md#-add-cloud-service-credentials" target="_blank">Add Cloud Services</a><br>
3. <a href="https://github.com/caltechlibrary/handprint/blob/master/README.md#microsoft" target="_blank">Microsoft</a><br>
4. <a href="https://github.com/caltechlibrary/handprint/blob/master/README.md#google" target="_blank">Google</a><br>
5. <a href="https://github.com/caltechlibrary/handprint/blob/master/README.md#%EF%B8%8E-usage" target="_blank">Usage</a><br>

<br>
    <iframe id="github-iframe" src="" style="width:1000px;height:1000px;"></iframe>
    <script>
        fetch('https://api.github.com/repos/caltechlibrary/handprint/contents/README.md#-introduction')
            .then(function(response) {
                return response.json();
            }).then(function(data) {
                iframe = document.getElementById('github-iframe');
                iframe.src = 'data:text/html;base64,' + encodeURIComponent(data['content']);
            });
    </script>

{% include footer.html %}
