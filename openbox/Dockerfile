FROM bxggs/vnc:base

COPY services.d /etc/services.d/

RUN apt update \
  && apt install -y openbox obmenu \
  && rm -rf /var/lib/apt/lists/*
