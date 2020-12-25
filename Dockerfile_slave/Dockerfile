FROM ubuntu:16.04
LABEL maintainer="Merve Gumuscibik"
RUN apt-get update && apt-get install -y nginx
RUN apt-get install keepalived -y
EXPOSE 8881
COPY keepalivedslave.conf /etc/keepalived/keepalivedslave.conf
COPY slave_index.html /usr/share/nginx/html/slave_index.html
COPY keepalived.sh /
CMD ["sh", "/keepalived.sh"]