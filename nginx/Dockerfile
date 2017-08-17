FROM nginx:alpine

RUN rm /etc/nginx/conf.d/default.conf

COPY workspace /etc/nginx/html
COPY configuration /etc/nginx

VOLUME /etc/nginx/html
VOLUME /etc/nginx
VOLUME /var/log/nginx