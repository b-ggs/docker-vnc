FROM archlinux

RUN pacman -Sy --noconfirm tigervnc xterm supervisor

COPY services.d /etc/services.d

ENV DISPLAY :1
ENV GEOMETRY 1280x720
ENV PASSWORD vncpassword
ENV PORT 5901

EXPOSE 5901

ENTRYPOINT ["/init"]

CMD ["sleep", "1000"]
