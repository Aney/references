# HTTPS/SSL

To make your website safer.
It's also good for SEO, and having people actually be willing to us your site.

## Install certbot
And it's nginx module
`apt install python3-certbot-nginx`

## Start certbot 
`certbot --nginx`
This will ask for an email, for renewals
`certbot --nginx --register-unsafely-without-email`
This will not ask for an email (although it's probably a good idea to use one)

Read the terms and accept what you want. E.g. if you don't want to give
your email to anyone, deny that.

When it asks for auto redirects, select option 2

### Apply SSL changes (if 2 selected)
`systemctl reload nginx`

## Automatic SSL certificated renewal
With a crontab

`crontab -e`

Add a line containing 
`0 0 1 * * certbot --nginx renew` 
Every 1 month, it will try to renew your SSL certificates

