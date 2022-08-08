FROM alpine:latest

ENV CRON_SCHEDULE="0 0 * * * *"
RUN apk --update add logrotate
RUN echo "${CRON_SCHEDULE}	/usr/sbin/logrotate -v /etc/logrotate.conf" >> /etc/crontabs/root && \
    mkdir -p /etc/logrotate.d

ADD logrotate.conf /etc/logrotate.conf

ENTRYPOINT [ ]
CMD ["crond", "-f"]
