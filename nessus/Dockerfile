FROM debian:jessie
MAINTAINER Rich Walchuck <rich.walchuck@gmail.com>

ENV DEBIAN_FRONTEND noninteractive
ENV NESSUS_VERSION 6.8.1

RUN apt-get update && \
apt-get install -y wget && \
rm -rf /var/lib/apt/lists/*

RUN wget -O /tmp/Nessus-${NESSUS_VERSION}-debian6_amd64.deb \
"https://downloads.nessus.org/nessus3dl.php?file=Nessus-${NESSUS_VERSION}-debian6_amd64.deb&licence_accept=yes&t=39ef4ab86349938a831307a74e869fa8"

RUN dpkg -i /tmp/Nessus-${NESSUS_VERSION}-debian6_amd64.deb

VOLUME [ "/opt/nessus/var/nessus" ]

EXPOSE 8834

ENTRYPOINT [ "/opt/nessus/sbin/nessusd" ]

