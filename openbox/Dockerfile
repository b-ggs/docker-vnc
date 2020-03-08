FROM bxggs/vnc:base

RUN apt update \
  && apt install -y openbox obmenu \
  && rm -rf /var/lib/apt/lists/*

CMD ["openbox-session"]
