FROM alpine:latest

RUN \
 apk update && \
 apk upgrade && \
 apk add squid 

#USER squid

EXPOSE 3128/tcp

ENTRYPOINT ["squid", "-N"]

