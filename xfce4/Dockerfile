FROM bxggs/vnc:base

RUN apt update \
  && apt install -y xfce4-panel xfdesktop4 xfwm4 xfce4-settings xfce4-session \
  && rm -rf /var/lib/apt/lists/*

CMD ["startxfce4"]
