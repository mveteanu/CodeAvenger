Did you know that you can host your website on GitHub? This blog is currently [hosted for free on GitHub](http://github.com/mveteanu/CodeAvenger). You can do this as simple as creating a GitHub repository.

This article shows how to add a custom domain purchased via GoDaddy to the GitHub repository that contains the website.


Purchase a domain from GoDaddy
------------------------------

1. Open an account with [GoDaddy](http://www.godaddy.com) and purchase a .com, .net, .etc domain.

2. In our case we'll purchase vmasoft.net


Create the GitHub pages site
----------------------------

1. Open an account with [GitHub](http://www.github.com). If you already have a github account, you can use that one.

2. On you GitHub account, create a new project repository: E.g. vmasoft

   ![](/img/posts/godaddy_github_01.png)

3. Create your site in a local folder.
At minimum, create only 1 page named index.html

4. Push the local files into the GitHub repository.
There are multiple ways to push files into the GitHub repository.
If you prefer the command line you can do via git, like in this example:
   
   ```
   git init
   git add .
   git commit -m "first version"
   git remote add origin https://github.com/mveteanu/vmasoft.git
   git push -u origin master
   ```

5. Go to GitHub repository settings, and locate the In the "GitHub Pages" section.
Select "master branch" from the Source combobox to allow your repository behave like a website.
Hit "Save".

   ![](/img/posts/godaddy_github_02.png)

   ![](/img/posts/godaddy_github_03.png)

6. Test your website by navigating to the displayed Url.
In our example, this will be: [https://mveteanu.github.io/vmasoft/](https://mveteanu.github.io/vmasoft/)


Configure the custom domain in GitHub
-------------------------------------

1. In the same "GitHub Pages" section, populate the "Custom domain" textbox with your domain. GitHub recommends using a www subdomain as your custom domain.

   In our case this will be:

   [www.vmasoft.net](http://www.vmasoft.net)

   Of course, you can use other subdomains, or no subdomains at all.
   You can find more information about supported custom domains [here](https://help.github.com/articles/about-supported-custom-domains/) on GitHub.
   
   GitHub has this [warning](https://help.github.com/articles/setting-up-a-www-subdomain/):

   "Warning: We highly recommend adding your custom domain to your GitHub Pages site's repository before configuring your domain name with your DNS provider."


Set-up A and CNAME records in GoDaddy
-------------------------------------

Go back to GoDaddy and enter the "Manage DNS" section for your domain.

   ![](/img/posts/godaddy_github_04.png)

1. To set up the apex domain, such as vmasoft.net, we need to configure two A records with GoDaddy.

   The A records will point to the following two IP addresses as required by GitHub and explained [here](https://help.github.com/articles/setting-up-an-apex-domain/)


   - 185.199.108.153
   - 185.199.109.153
   - 185.199.110.153
   - 185.199.111.153


2. To set up the www subdomain, such as [www.vmasoft.net](http://www.vmasoft.net) we need to configure a CNAME record with GoDaddy.
In order to take advange of GitHub CDN, we will have to point the www subdomain to GitHub account address.

   At this point, the GoDaddy DNS records should contain the following:

   |NAME  |   TYPE  |  VALUE               |
   |------|---------|----------------------|
   |@     |   A     |  185.199.108.153     |
   |@     |   A     |  185.199.109.153     |
   |@     |   A     |  185.199.110.153     |
   |@     |   A     |  185.199.111.153     |
   |www   |   CNAME |  mveteanu.github.io  |


   Note: Other entries may be already pre-populated. Don't worry about those.

   ![](/img/posts/godaddy_github_05.png)

   Warning: In the past these IPs used to be 192.30.252.153 and 192.30.252.154. If you have the old ones, please replace them with the new ones.

Test your new domain
--------------------

1. Wait a few minutes (or hours) for the changes to propagate.

2. Test your new website / domain. E.g. [http://www.vmasoft.net](http://www.vmasoft.net)

3. If you have access to a Linux machine you can use the dig command to check the DNS settings. It should look like this:

```sh
dig www.vmasoft.net
```

![](/img/posts/godaddy_github_06.png)

