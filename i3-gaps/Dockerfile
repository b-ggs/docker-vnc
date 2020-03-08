FROM bxggs/vnc:base

RUN apt update \
  # https://gist.github.com/boreycutts/6417980039760d9d9dac0dd2148d4783
  && apt install -y git cmake libxcb-xrm-dev libxcb-shape0-dev libxcb1-dev libxcb-keysyms1-dev libpango1.0-dev libxcb-util0-dev libxcb-icccm4-dev libyajl-dev libstartup-notification0-dev libxcb-randr0-dev libev-dev libxcb-cursor-dev libxcb-xinerama0-dev libxcb-xkb-dev libxkbcommon-dev libxkbcommon-x11-dev autoconf xutils-dev libtool automake \
  && mkdir -p /tmp \
  && cd /tmp \
  && git clone https://github.com/Airblader/xcb-util-xrm \
  && cd xcb-util-xrm \
  && git submodule update --init \
  && ./autogen.sh --prefix=/usr \
  && make \
  && make install \
  && cd /tmp \
  && git clone https://www.github.com/Airblader/i3 i3-gaps \
  && cd i3-gaps \
  && git checkout gaps && git pull \
  && autoreconf --force --install \
  && rm -rf build \
  && mkdir build \
  && cd build \
  && ../configure --prefix=/usr --sysconfdir=/etc --disable-sanitizers \
  && make \
  && make install \
  && rm -rf /tmp/* \
  && rm -rf /var/lib/apt/lists/*

CMD ["i3"]
