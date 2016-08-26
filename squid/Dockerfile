FROM centos:latest

RUN \
 yum -y update && \
 yum -y install squid && \
 yum clean all

#USER squid

EXPOSE 3128/tcp

ENTRYPOINT ["squid", "-N"]

