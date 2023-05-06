FROM bahmniindiadistro/proxy:latest

# this command need to be given to build proxy image locally before starting service on any server
# docker compose down
# docker compose build proxy
# docker compose up -d

USER root


RUN echo 'Running some proxy commands'

Add proxy/resources/bahmniLogoFull.png /tmp/

Add proxy/resources/index.html /tmp/

RUN cp /tmp/bahmniLogoFull.png  /usr/local/apache2/htdocs/bahmni-logo.png

RUN cp /tmp/index.html  /usr/local/apache2/htdocs/

COPY proxy/resources/favicon.ico /usr/local/apache2/htdocs/

