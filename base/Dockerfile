FROM debian:buster

ADD https://github.com/just-containers/s6-overlay/releases/download/v1.22.1.0/s6-overlay-amd64.tar.gz /tmp/
RUN tar xzf /tmp/s6-overlay-amd64.tar.gz -C /

RUN apt update \
  && apt install -y x11vnc xvfb \
  && rm -rf /var/lib/apt/lists/*

COPY services.d /etc/services.d

ENV DISPLAY=:1
ENV DISPLAY_RESOLUTION=1280x720x16
ENV VNC_PASSWORD=vncpassword
ENV VNC_PORT=5901

ENTRYPOINT ["/init"]

CMD ["xterm"]
