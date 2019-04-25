FROM haproxy:latest
MAINTAINER HaproxyLog

RUN apt-get update && apt-get install rsyslog -y

ADD haproxy.conf /etc/rsyslog.d
ADD rsyslog.conf /etc/rsyslog.conf
ADD haproxy.cfg /usr/local/etc/haproxy/haproxy.cfg

COPY docker-entrypoint.sh /

LABEL org.label-schema.build-date="2019-03-25T10:23:04Z" \
            org.label-schema.docker.dockerfile="/Dockerfile" \
            org.label-schema.license="MIT" \
            org.label-schema.name="HAproxy-syslog"

EXPOSE 80 443

ENTRYPOINT ["/docker-entrypoint.sh"]
