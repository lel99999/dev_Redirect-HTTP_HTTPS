# dev_Redirect-HTTP_HTTPS
HTTP -> HTTPS Redirect with Apache2

#### To redirect to a website use the following
In Red-Hat based distros such as CentOS and Fedora, virtual host files are stored in the /etc/httpd/conf.d. While on Debian and its derivatives like Ubuntu the files are stored in the /etc/apache2/sites-available directory.

To redirect a website to HTTPS, use the Redirect directive as shown below:<br/>

```
<VirtualHost *:80> 
  ServerName example.com
  ServerAlias www.example.com

  Redirect permanent / https://example.com/
# RedirectMatch permanent ^/(.*)$ https://www.example.com/$1 -- redirects recursive pages.
</VirtualHost>

<VirtualHost *:443>
  ServerName example.com
  ServerAlias www.example.com

  Protocols h2 http/1.1

  # SSL Configuration

  # Other Apache Configuration

</VirtualHost>
```
