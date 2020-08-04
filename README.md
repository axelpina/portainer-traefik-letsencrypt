# Portainer + Traefik w/ Let's Encrypt

This repository will help you set up Portainer served by Traefik v2.1.6 over HTTPS (Let's Encrypt)

##Setup

Simply `git clone` the repository into your server's directory.

`git clone https://github.com/AxelPina/portainer-traefik-letsencrypt.git`

Then fill the `.env` file with your credentials and your domain:

```
#GENERAL INFO
ACME_EMAIL=email@domain.com
PORTAINER_TRAEFIK_URL=whatever.mydomain.com
RESOLVER=name
```

`ACME_EMAIL` is the email address which will be used when registering the certificate at Let's Encrypt.
`ODOO_TRAEFIK_URL` is the hostname which Traefik will listen to to route requests to the Odoo container.
`RESOLVER` is responsible for retrieving certificates from an ACME server.