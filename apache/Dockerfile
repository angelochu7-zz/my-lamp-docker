FROM httpd:2.4.43-alpine
ARG REGION=Asia
ARG COUNTRY=Hong_Kong
RUN apk update; \
    apk upgrade;
RUN apk add \
    libmcrypt-dev \
    -U tzdata;
RUN cp /usr/share/zoneinfo/$REGION/$COUNTRY /etc/localtime && echo "$REGION/$COUNTRY" > /etc/timezone
# Copy apache vhost file to proxy php requests to php-fpm container
COPY demo.apache.conf /usr/local/apache2/conf/demo.apache.conf
RUN echo "Include /usr/local/apache2/conf/demo.apache.conf" \
    >> /usr/local/apache2/conf/httpd.conf
