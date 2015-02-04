FROM centos:7

MAINTAINER Mathias Lafeldt <mathias.lafeldt@gmail.com>

ENV REFRESHED_AT 2015-02-04

RUN yum update -y && yum install -y \
        curl \
        gcc \
        git \
        make \
        rpm-build \
        ruby \
        ruby-devel \
        tar

RUN echo "gem: --no-ri --no-rdoc" >/etc/gemrc
RUN gem install fpm -v 1.3.3
RUN gem install fpm-cookery -v 0.25.0

VOLUME /data
WORKDIR /data

CMD ["fpm-cook", "package", "--debug", "--tmp-root", "/tmp", "recipe.rb"]
