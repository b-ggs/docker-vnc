FROM archlinux

RUN pacman -Sy --noconfirm tigervnc

ENV DISPLAY :1
ENV GEOMETRY 1280x720
ENV PASSWORD vncpassword
ENV PORT 5901

COPY entrypoint /entrypoint

ENTRYPOINT ["/entrypoint"]

CMD ["docker-start"]
