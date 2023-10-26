FROM nginx
LABEL "Project"="fidevcontainerization"
LABEL "Author"="Fidelosa"

RUN rm -rf /etc/nginx/conf.d/default.conf
COPY nginxfidevapp.conf /etc/nginx/conf.d/fidevapp.conf