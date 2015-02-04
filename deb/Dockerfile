FROM ubuntu:14.04

MAINTAINER Mathias Lafeldt <mathias.lafeldt@gmail.com>

ENV REFRESHED_AT 2015-02-04

ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update -y && apt-get install -y --no-install-recommends \
        build-essential \
        curl \
        git \
        ruby \
        ruby-dev

RUN echo "gem: --no-ri --no-rdoc" >/etc/gemrc
RUN gem install fpm -v 1.3.3
RUN gem install fpm-cookery -v 0.25.0

VOLUME /data
WORKDIR /data

CMD ["fpm-cook", "package", "--debug", "--tmp-root", "/tmp", "recipe.rb"]
