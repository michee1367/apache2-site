# Documentation

## Activer les modules

```bash

    a2enmod proxy
    a2enmod proxy_http
    a2enmod proxy_ajp
    a2enmod rewrite
    a2enmod deflate
    a2enmod headers
    a2enmod proxy_balancer
    a2enmod proxy_connect
    a2enmod proxy_html

```

## fichier de configuration

```conf
<VirtualHost *:80>
        ServerName  example.com
        ServerAlias www.example.com
        ProxyPreserveHost On

        
        # Servers to proxy the connection, or;
        # List of application servers:
        # Usage:
        # ProxyPass / http://[IP Addr.]:[port]/
        # ProxyPassReverse / http://[IP Addr.]:[port]/
        # Example: 
        ProxyPass / http://0.0.0.0:8080/
        ProxyPassReverse / http://0.0.0.0:8080/
        
</VirtualHost>

```