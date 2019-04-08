FROM alpine:3.9
MAINTAINER Sonny Yu <sonnyyuirm@gmail.com>
RUN apk add --upgrade --no-cache tzdata mongodb 
ENV TZ=America/Los_Angeles
VOLUME /data/db
EXPOSE 27017 28017
COPY run.sh /root/run.sh
RUN chmod 755 /root/run.sh
RUN rm -rf /var/cache/apk/* /tmp/*
ENTRYPOINT [ "/root/run.sh" ]
CMD [ "mongod", "--bind_ip", "0.0.0.0" ]
