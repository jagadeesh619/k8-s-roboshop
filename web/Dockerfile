FROM nginx

RUN rm -rf /usr/share/nginx/html/index.html

RUN rm -rf /etc/nginx/nginx.conf

RUN rm -rf /etc/nginx/conf.d/default.conf

COPY roboshop.conf /etc/nginx/nginx.conf

# folder will not copy , only files in it will copy to /usr/share/nginx/html

ADD static /usr/share/nginx/html/   


