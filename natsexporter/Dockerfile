FROM alpine:3.6
MAINTAINER Konstantin Makarov <konstantin.makarov@altarix.ru>


RUN apk update && apk add ca-certificates && rm -rf /var/cache/apk/*

RUN mkdir app

ADD prometheus-nats-exporter /app/
WORKDIR app

ENTRYPOINT ["./prometheus-nats-exporter", "-varz", "http://test.pcs.pxl.alx:8222"]
