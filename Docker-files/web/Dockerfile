FROM nginx 
LABEL "Project"="Vprofile"
LABEL "Author"="Kalyan"

RUN rm -rf  /etc/nginx/conf.d/default.conf
#The above line is for removing the default configuration provided and the location is provided in the documentation

COPY nginvproapp.conf /etc/nginx/conf.d/vproapp.conf
