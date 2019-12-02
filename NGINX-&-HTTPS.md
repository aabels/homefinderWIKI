## What is it?
NGINX (pronounced "engine ex") is a web server, similar to Apache. We are using [NGINX](https://www.nginx.com/) to being the "front" of our deployment, managing the HTTPS and routing to the respective backend(s) via `proxy_pass`

## Installing NGINX
NGINX is usually in the default repositories.
```bash
sudo apt install -y nginx
```

## Configuring NGINX
There are many possible configurations for NGINX, however we are only using a tiny subset of its capabilities. Namely the `proxy_pass` module.

Virtual host configurations are stored in `/etc/nginx/sites-available/` and symlinked from `/etc/nginx/sites-enabled/` when you want them enabled. This allows for "turning" websites on and off

Our NGINX config will typically look like this
```
# /etc/nginx/sites-available/homefinder
upstream dev {
    server 10.1.9.51:8000;
}

server {
	server_name app-dev.cybera.rentwhiz.ca;
	location / {
		proxy_pass http://dev; # <--- pass to the other server/host running the app
		proxy_set_header                Host $server_name;
		proxy_set_header                HTTP_Country-Code $geoip_country_code;
		proxy_pass_request_headers      on;
	}
}
```

# HTTPS (Certbot)

We are managing HTTPS certificates using Certbot, a tool that generates and configures HTTPS certificates for us automatically. You can install it following this [guide](https://certbot.eff.org/lets-encrypt/ubuntubionic-nginx)

After you have it installed on the same server as NGINX and have the respective domain names configured to point to the instance, you can run `certbot` to generate the certificates.

```bash
sudo certbot --nginx
```

This will interactively allow you to choose what certificates to generate and enable.


