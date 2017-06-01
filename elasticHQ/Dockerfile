FROM nginx:latest

MAINTAINER arashicage@yeah.net

RUN \
  apt-get update && \
  apt-get install -y zip unzip && \
  apt-get autoremove -y -q && \
  apt-get clean -y -q

ADD https://github.com/royrusso/elasticsearch-HQ/archive/master.zip /tmp/elasticsearch-HQ-master.zip

RUN \
  unzip -q /tmp/elasticsearch-HQ-master.zip -d /tmp && \
  mv -f /tmp/elasticsearch-HQ-master/* /usr/share/nginx/html && \
  rm -rf /tmp/*