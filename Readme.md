# Commands Console Nginx

- `start nginx`     start proccess PID
- `nginx -t`        check file config Nginx
- `nginx -s stop`   stop proccess PID
- `nginx -s reload` reload proccess PID
- `nginx -s quit` 	graceful shutdown
- `nginx -s reopen`	re-opening log files

## Install OpenSsl

- after install openssl execute into console

`openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout ./local.key -out ./local.crt`

- Fullfill data on console

```
Country Name (2 letter code) [AU]:US
State or Province Name (full name) [Some-State]:New York
Locality Name (eg, city) []:New York City
Organization Name (eg, company) [Internet Widgits Pty Ltd]:Bouncy Castles, Inc.
Organizational Unit Name (eg, section) []:Ministry of Water Slides
Common Name (e.g. server FQDN or YOUR name) []:server_IP_address
Email Address []:admin@your_domain.com
```

### commands console Windows

- taskkill /PID <PID> /F
- C:\nginx-1.19.7>tasklist /fi "imagename eq nginx.exe"


### Step 1 — Enabling HTTP/2 Support

- Allow Http 2

```
    listen [::]:443 ssl http2 ipv6only=on;
    listen 443 ssl http2;

    ssl_certificate     common.crt;
    ssl_certificate_key common.key;
```


