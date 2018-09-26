FROM ubuntu:16.04
WORKDIR /opt/example

RUN apt-get update \
  && apt-get install -y curl apt-utils build-essential wget git gettext software-properties-common libxrender1 tzdata \
  && apt-get install -y zlib1g-dev libpq-dev libssl-dev libreadline-dev libyaml-dev libsqlite3-dev libxml2-dev libxslt1-dev libcurl4-openssl-dev libffi-dev \
  && curl -sL https://deb.nodesource.com/setup_8.x | bash - \
  && apt-get install -y nodejs

RUN  git clone https://github.com/TramboCloud/hapi-socketio-redis-chat-example.git . \
    && npm install

CMD npm start
