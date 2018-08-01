FROM ruby:2.5.1

ENV LC_ALL=C.UTF-8

RUN \
  curl -sL https://deb.nodesource.com/setup_8.x | bash - && \
  curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | apt-key add - && \
  echo "deb https://dl.yarnpkg.com/debian/ stable main" | tee /etc/apt/sources.list.d/yarn.list && \
  apt-get update && \
  apt-get install -y \
      mysql-client \
      postgresql-client \
      sqlite3 \
      nodejs \
      yarn \
      imagemagick \
      mecab libmecab-dev mecab-ipadic-utf8 \
      --no-install-recommends && \
  mkdir /tmp/phantomjs && \
  curl -L https://bitbucket.org/ariya/phantomjs/downloads/phantomjs-2.1.1-linux-x86_64.tar.bz2 \
      | tar -xj --strip-components=1 -C /tmp/phantomjs && \
  mv /tmp/phantomjs/bin/phantomjs /usr/local/bin && \
  rm -rf /var/lib/apt/lists/*  /tmp/*
