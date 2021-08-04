# GitWeb

A web GUI for your repositories
This is assuming an install of git, and nginx

## Install gitweb
Debian already has this as a package.
If your server distro doesn't...

`sudo apt install gitweb fcgiwrap`

## Setup a webpage

### Create a new nginx site
`vim /etc/nginx/sites-available/gitweb`

Add the following
`server {
	listen 80 ;
	listen [::]:80 ;
	server_name git.<domain> www.git.<domain> ;

	location /index.cgi {
		root /usr/share/gitweb/;
		include fastcgi_params;
		gzip off;
		fastcgi_param SCRIPT_NAME $uri;
		fastcgi_param GITWEB_CONFIG /etc/gitweb.conf;
		fastcgi_pass  unix:/var/run/fcgiwrap.socket;
	  }

	location / {
	root /usr/share/gitweb/;
	index index.cgi;
	}
}`

#### Copy new site to site-enables

`ln -s /etc/nginx/sites-available/gitweb /etc/nginx/sites-enabled/`

### Change default gitweb location

`vim /etc/gitweb.conf`

Amend the line containing `/var/lib/git` to `/srv/git`


Reload nginx
`systemctl reload nginx`

