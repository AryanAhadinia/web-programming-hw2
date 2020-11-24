# Web2
Web Programming HW2 - 2020 Fall

## NGINX
Beware of SELINUX. also we need to configure few things just like this:
```
sudo chmod 750 /path/to/project
cd /path/to/project
sudo usermod -a -G root nginx
```

and then we can configure nginx to serve.
```
    server {
        listen       80 default_server;
        listen       [::]:80 default_server;
        server_name  _;
        root         /root/web2;

        # Load configuration files for the default server block.
        include /etc/nginx/default.d/*.conf;

        location / {
        }

        error_page 404 /404.html;
            location = /usr/share/nginx/html/40x.html {
        }

        error_page 500 502 503 504 /50x.html;
            location = /usr/share/nginx/html/50x.html {
        }
    }
```
also available at web2/nginx.conf

## People
Master of course: **_Mr. Omid Jafari-Nezhad_**
| Name | Student Number |
| :-: | :-: |
| _**Aryan Ahadinia**_ | _98103878_ |
| _**Mohammad Jafari**_ | _98105654_ |
