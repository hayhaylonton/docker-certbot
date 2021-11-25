# docker-certbot

step 1:
create virtual host listen http

step 2:
run command
docker-compose run --rm  certbot certonly --webroot --webroot-path /var/www/certbot/ --dry-run -d sample.local --agree-tos -m your-email@local

step 3:
run command
docker-compose run --rm  certbot certonly --webroot --webroot-path /var/www/certbot/ -d sample.local

step 4:
update virtual host add listen https

note:
reload nginx
docker-compose exec webserver nginx -s reload