FROM nginx
LABEL "project" = "Interior"
LABEL " Author" = "ckc"

RUN rm -rf /etc/nginx/conf.d/default.conf
COPY ngnxvpapp.conf /etc/nginx/conf.d/vgroapp.conf