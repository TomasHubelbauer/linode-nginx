# Linode NGinx

[**WEB**](https://tomashubelbauer.github.io/linode-nginx)

- Buy a domain name
- Set domain name DNS servers to `ns1.linode.com` through `ns5.linode.com`
- Wait until `dig`/`whois` show the Linode DNS servers
- Go to the Linode site and add your domain
- Select a backing node for the site
- Install NGinx `apt install nginx` (run `apt update` in case of a fresh box)
- Verify NGinx installation and find configuration file path: `nginx -t`
- Access the node IP to ensure NGinx servers the welcome page
- Follow https://github.com/TomasHubelbauer/nginx-sites-available
- Secure using https://github.com/TomasHubelbauer/nginx-lets-encrypt

## To-Do
