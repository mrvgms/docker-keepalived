FROM ubuntu:16.04
LABEL maintainer="Merve Gumuscibik"
RUN apt-get update && apt-get install -y nginx
RUN apt-get install keepalived -y
EXPOSE 8880
COPY keepalivedmaster.conf /etc/keepalived/keepalivedmaster.conf
COPY master_index.html /usr/share/nginx/html/master_index.html
COPY keepalived.sh /
CMD ["sh", "/keepalived.sh"]