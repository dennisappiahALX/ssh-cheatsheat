## Nginx

Nginx is a webserver that can be used as `reverse proxy`, `load balancer`, `mail proxy`, and `HTTP cache`

**Features**

* Nginx is easy to configure in order to server `static` web content or as a proxy server
* Nginx can be deployed to serve `dynamic` content on the network using FastCGI, SCGI handlers for scripts, WSGI application servers
* Nginx uses an asynchronous event-driven approach to handle requests

## 1. How to Install Nginx Ubuntu

<https://www.digitalocean.com/community/tutorials/how-to-install-nginx-on-ubuntu-16-04>



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



