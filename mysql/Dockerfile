FROM mysql:5.7.30
ARG REGION=Asia
ARG COUNTRY=Hong_Kong
RUN cp /usr/share/zoneinfo/$REGION/$COUNTRY /etc/localtime && echo "$REGION/$COUNTRY" > /etc/timezone