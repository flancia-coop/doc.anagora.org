Here is an example configuration for Nginx.

```
map $http_upgrade $connection_upgrade {
        default upgrade;
        ''      close;
}
server {
        server_name hedgedoc.example.com;

        location / {
                proxy_pass http://127.0.0.1:3000;
                proxy_set_header Host $host; 
                proxy_set_header X-Real-IP $remote_addr; 
                proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for; 
                proxy_set_header X-Forwarded-Proto $scheme;
        }

        location /socket.io/ {
                proxy_pass http://127.0.0.1:3000;
                proxy_set_header Host $host; 
                proxy_set_header X-Real-IP $remote_addr; 
                proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for; 
                proxy_set_header X-Forwarded-Proto $scheme;
                proxy_set_header Upgrade $http_upgrade;
                proxy_set_header Connection $connection_upgrade;
        }

    listen [::]:443 ssl http2;
    listen 443 ssl http2;
    ssl_certificate fullchain.pem;
    ssl_certificate_key privkey.pem;
    include options-ssl-nginx.conf;
    ssl_dhparam ssl-dhparams.pem;
}
```