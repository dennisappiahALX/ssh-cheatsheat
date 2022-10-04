## Nginx

Nginx is a webserver that can be used as `reverse proxy`, `load balancer`, `mail proxy`, and `HTTP cache`

**Features**

* Nginx is easy to configure in order to server `static` web content or as a proxy server
* Nginx can be deployed to serve `dynamic` content on the network using FastCGI, SCGI handlers for scripts, WSGI application servers
* Nginx uses an asynchronous event-driven approach to handle requests

## 1. How to Install Nginx Ubuntu

<https://www.digitalocean.com/community/tutorials/how-to-install-nginx-on-ubuntu-16-04>


**Server Configuration**

* `/etc/nginx`: The Nginx configuration directory. All of the Nginx configuration files reside here.
* `/etc/nginx/nginx.conf`: The main Nginx configuration file. This can be modified to make changes to the Nginx global configuration.
* `/etc/nginx/sites-available/`: The directory where per-site “server blocks” can be stored. Nginx will not use the configuration files found in this directory unless they are linked to the sites-enabled directory (see below). Typically, all server block configuration is done in this directory, and then enabled by linking to the other directory.
* `/etc/nginx/sites-enabled/`: The directory where enabled per-site “server blocks” are stored. Typically, these are created by linking to configuration files found in the sites-available directory.
* `/etc/nginx/snippets`: This directory contains configuration fragments that can be included elsewhere in the Nginx configuration. Potentially repeatable configuration segments are good candidates for refactoring into snippets.

**Server Logs**

* `/var/log/nginx/access.log`: Every request to your web server is recorded in this log file unless Nginx is configured to do otherwise.
* `/var/log/nginx/error.log`: Any Nginx errors will be recorded in this log.


## 2. How to Set Up Nginx Server Blocks (virtual Hosts) On Ubuntu 16.04

Server blocks (virtual Hosts in Apache) can be used to encapsulate configuration details and host `more than one` domain on a `single server`

* By Default Nginx has one server block enabled . It is configured to serve documents out of a directory at `/var/www/html`.

* While this works well for a single site, we need additional directories if we’re going to serve multiple sites. We can consider the `/var/www/html` directory the default directory that will be served if the client request doesn’t match any of our other sites.

* We will create a directory structure within `/var/www` for each of our sites. The actual web content will be placed in an `html` directory within these site-specific directories. This gives us some additional flexibility to create other directories associated with our sites as siblings to the html directory if necessary

Follow link below to set up nginx server blocks

- Check out your confgured added sites

`/etc/nginx/sites-available/` - all sites available  (`default` is the available and enabled site by default)

`cd /etc/nginx/sites-enabled/` - all sites enabled 

**Steps**

<https://www.digitalocean.com/community/tutorials/how-to-set-up-nginx-server-blocks-virtual-hosts-on-ubuntu-16-04>



