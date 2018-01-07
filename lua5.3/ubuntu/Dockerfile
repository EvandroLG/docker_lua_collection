FROM ubuntu:latest

MAINTAINER evandrolg <evandrolgoncalves@gmail.com>

RUN apt-get update -y && apt-get -y upgrade
RUN apt-get install -y libssl-dev build-essential libreadline-dev curl wget unzip
RUN curl -R -O http://www.lua.org/ftp/lua-5.3.4.tar.gz \
    && tar zxf lua-5.3.4.tar.gz \
    && rm -rf lua-5.3.4.tar.gz \
    && cd lua-5.3.4 \
    && make linux test && make install

RUN wget https://luarocks.org/releases/luarocks-2.4.3.tar.gz \
    && tar zxpf luarocks-2.4.3.tar.gz \
    && cd luarocks-2.4.3 \
    && ./configure; make bootstrap

CMD ['lua', '-v']
