Learning Activities & Resources
-------------------------------
I set up a hosted VPS and installed Nginx, PHP and MySQL. I also installed phpMyAdmin and Joomla. I mostly learned from reading the official Joomla documentation.

### Resources
 * [Joomla technical requirements](https://manual.joomla.org/docs/next/get-started/technical-requirements/)
 * [Installing Joomla](https://docs.joomla.org/Special:MyLanguage/J4.x:Installing_Joomla)
 * [Joomla Hosting Setup](https://docs.joomla.org/J4.x:Hosting_Setup)
 * [Certbot instructions](https://certbot.eff.org/instructions?ws=other&os=debianbuster)

Estimated Hours
---------------
About 1 hour of learning.

Content Insights
----------------
The Joomla documentation is quite poor and community resources lacking compared to what's available for WordPress, so I had to spend more than searching for the correct information and making educated guesses.

Joomla uses "menus" to define what pages are available on the website, so to add an article as an independent page, you must add it as a "Single Article" in your site's menu.

I learned that the required PHP modules for running a Joomla website are: `php8.2-gd php8.2-curl php8.2-xml`.

When creating TLS certificates with `certbot`, you can specify the webroot by using the `-w` option before specifying the domain with the `-d` option. For example:
```sh
certbot certonly --webroot -w /home/jcu/joomla -d joomla.jcu.shibesoft.com
```

When installing Debian, I accidentally mistyped the DNS information. This caused some system utilities to not be installed. Especially the `man` command was unavailable, but it can be installed with `apt install man-db` once DNS queries can be resolved.

Career/Employability/Learning Insights
--------------------------------------

Being able to set up a working VPS and installing the server components manually is a valuable skill. It allows you to easily set up a local enviornment, as well as the production enviornment.

Joomla tries to do a little bit of everything, which makes it a rather user-unfriendly system with a steep learning curve. I won't be using Joomla again after this subject.
