# Portainer + Traefik w/ Let's Encrypt

This repository will help you set up Portainer served by Traefik v2.1.6 over HTTPS (Let's Encrypt)

## Setup

Simply `git clone` the repository into your server's directory.

`git clone https://github.com/AxelPina/portainer-traefik-letsencrypt.git`

  Apply permissions to be able to edit the `.env`.

Then fill the `.env` file with your credentials and your domain:

```
#GENERAL INFO
ACME_EMAIL=email@domain.com
PORTAINER_TRAEFIK_URL=whatever.mydomain.com
RESOLVER=name
```

* `ACME_EMAIL` is the email address which will be used when registering the certificate at Let's Encrypt.

* `ODOO_TRAEFIK_URL` is the hostname which Traefik will listen to to route requests to the Odoo container.

# Resolver

Replace `myresolver` with your own resolver name.

Traefik will automatically renew the certificate every 3 months.

## Run

```bash
cd portainer-traefik-letsencrypt
docker-compose up -d
```
