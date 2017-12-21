FROM debian:latest

MAINTAINER evandrolg <evandrolgoncalves@gmail.com>

RUN apt-get update -y && apt-get -y upgrade
RUN apt-get install -y libssl-dev build-essential libreadline-dev curl

RUN curl -R -O http://www.lua.org/ftp/lua-5.3.4.tar.gz \
    && tar zxf lua-5.3.4.tar.gz \
    && rm -rf lua-5.3.4.tar.gz \
    && cd lua-5.3.4 \
    && make linux test \
    && ln -s /lua-5.3.4/src/lua /usr/bin/lua

CMD ['lua', '-v']
