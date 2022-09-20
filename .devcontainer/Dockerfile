FROM perl:latest


RUN apt-get update -qq && apt-get install -y \
  libwww-perl \
  liblwp-protocol-https-perl \
  libmojolicious-perl \
  libxml-libxml-perl \
  libcgi-pm-perl \
  bash \
  git \
  zsh \
  isc-dhcp-server \
  squid

RUN cpanm LWP LWP::Protocol::https XML::LibXML Mojolicious CGI

RUN sh -c "$(wget -O- https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

COPY zshrc /root/.zshrc

WORKDIR /apps

ENTRYPOINT []

