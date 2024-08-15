FROM nginx
LABEL "Project"="Vprofile"
LABEL "Author"="Imran"

#removing the default config file
RUN rm -rf /etc/nginx/conf.d/default.conf

#adding out own confif file to the location specified in he docs
COPY nginvproapp.conf /etc/nginx/conf.d/vproapp.conf