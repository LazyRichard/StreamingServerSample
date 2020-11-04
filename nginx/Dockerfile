FROM alpine:3

LABEL MAINTAINER="Suh Junmin <junmin.suh@realtek.com>"

ENV HTTP_PORT 80
ENV HTTPS_PORT 443
ENV RTMP_PORT 1935

RUN apk add --update \
  nginx-mod-rtmp \
  ffmpeg

RUN mkdir -p /run/nginx && \
    mkdir -p /usr/local/nginx/html/stream

EXPOSE $HTTPS_PORT
EXPOSE $HTTP_PORT
EXPOSE $RTMP_PORT

ENTRYPOINT [ "nginx", "-g", "daemon off;" ]
