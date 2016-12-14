FROM debian:latest
MAINTAINER Alexandre 'SuperKoala42' Roux <alexandreroux42@gmail.com>

RUN apt-get update && apt-get install -y -q ldnsutils

ENTRYPOINT [ "/usr/bin/drill" ]
