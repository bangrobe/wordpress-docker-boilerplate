FROM wordpress:latest

RUN mkdir /scripts



COPY /wait-for-it.sh /scripts
RUN chmod +x /scripts/wait-for-it.sh
CMD ["/scripts/wait-for-it.sh" , "db:3306" , "--strict" , "--timeout=300" , "--" , "/usr/local/bin/docker-entrypoint.sh", "apache2-foreground"]