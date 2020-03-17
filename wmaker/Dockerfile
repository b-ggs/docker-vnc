FROM bxggs/vnc:base

RUN apt update \
  && apt install -y wmaker wmnd wmdate \
  && rm -rf /var/lib/apt/lists/*

CMD ["wmaker"]
