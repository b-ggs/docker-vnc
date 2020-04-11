FROM archlinux

RUN pacman -Sy --noconfirm tigervnc xterm

ENV DUMB_INIT_VERSION=1.2.2
RUN curl -sSLo /usr/local/bin/dumb-init "https://github.com/Yelp/dumb-init/releases/download/v${DUMB_INIT_VERSION}/dumb-init_${DUMB_INIT_VERSION}_amd64" \
  && chmod +x /usr/local/bin/dumb-init

ENV DISPLAY :1
ENV GEOMETRY 1280x720
ENV PASSWORD vncpassword
ENV PORT 5901

COPY start-vnc /usr/local/bin/start-vnc

EXPOSE 5901

ENTRYPOINT ["dumb-init", "--"]

CMD ["start-vnc"]
