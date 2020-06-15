FROM mysql:5.7.30
ARG REGION=${REGION}
ARG COUNTRY=${COUNTRY}
RUN cp /usr/share/zoneinfo/${REGION}/${COUNTRY} /etc/localtime && echo "${REGION}/${COUNTRY}" > /etc/timezone