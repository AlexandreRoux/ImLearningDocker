FROM debian:latest
MAINTAINER Alexandre 'SuperKoala42' Roux <alexandreroux4$

RUN apt-get update && apt-get install -y -q tcpdump
ENTRYPOINT ["/usr/sbin/tcpdump"]
