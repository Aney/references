# Nginx

## Install
`apt install nginx`

## Make the site directory, and index
`mkdir /var/www/<website>'
'touch /var/www/<website>/index.html'
### Git
If you're using git VC for the website then after making the directory
just `git clone <repo>` and checkout the appropriate release/branch.

## Make a config
`vim /etc/nginx/sites-available/<website>`

### Basic config
`server {
        listen 80 ;
        listen [::]:80 ;
        server_name <domain>, www.<domain> ;
        root /var/www/<website> ;
        index index.html index.htm ;
        location / {
                try_files $uri $uri/ =404 ;
        }
}`

#### Basic description of above:
listen - listen to port 80 on ipv4 and ipv6
server_name - the website/url that someone connecting to the server is looking for
root - directory for the website (commonly kept in `/var/www/<websitename>`
index - the default file to load when connecting to the site. In order of desc priority
location - how the server should lookup files, if these aren't met throw a 404 error

#### Example Configs
Some examples can be found on nginx's site [here](https://www.nginx.com/resources/wiki/start/topics/examples/full/)


## Enable the site
This uses the config we build, by creating a symbolic link to it.
`ln -s /etc/nginx/sites-available/<website> /etc/nginx/sites-enabled/<website>`

### Restart nginx
`sudo systemctl reload nginx`
Using reload will not restart the service if a config is incorrect, so this is
generally safer, especially in a working environment.

## Allow http traffic
If you've not got a firewall installed, this can be ignored. If you do, for 
example after installing adar's _base you're going to want to allow traffic.

Http
`ufw allow 80` 
Https (recommended, all sites need SSL these days)
`ufw allow 443`

## WIP

## Internal address
Edit `/etc/hosts` line `127.0.0.1 localhost` to `127.0.0.1 \*.localhost`
Edit `.../sites-available/<website>` server_name and add <address>,localhost 

