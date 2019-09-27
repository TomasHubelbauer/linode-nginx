# Linode NGinx

- Buy a domain name
- Set domain name DNS servers to `ns1.linode.com` through `ns5.linode.com`
- Wait until `dig`/`whois` show the Linode DNS servers
- Go to the Linode site and add your domain
- Select a backing node for the site
- Install NGinx `apt install nginx`
- Verify NGinx installation and find configuration file path: `nginx -t`
- Access the node IP to ensure NGinx servers the welcome page
- Edit the initial NGinx configuration to include a `server` block `nano /etc/nginx/nginx.conf`

```nginx
http {
  // ...
  server {
    location / {
      root /www;
    }
  }
  // ...
}
```

- Create the `/www` static site directory `mkdir /www` and `cd` to it
- Create an index file for the site `echo <h1>My Site</h1> > index.html`
- Reload NGinx config `nginx -s reload` or restart the service `service nginx restart`
- Access the custom domain and veirfy NGinx serves the static site

---

- [ ] Find out why in my case it still serves the welcome page
- [ ] Add configs for having a static site in a directory or on a subdomain
- [ ] Add configs and information about SSL using LE

https://hooshmand.net/add-a-new-domain-or-subdomain-to-your-ghost-blog/
