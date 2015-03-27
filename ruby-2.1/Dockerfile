FROM ruby:2.1.5

# FROM: https://github.com/docker-library/rails/blob/master/Dockerfile
RUN apt-get update && apt-get install -y nodejs postgresql-client \
      --no-install-recommends && rm -rf /var/lib/apt/lists/*

# Installing phantomjs 1.9.8
RUN wget -P /usr/local https://bitbucket.org/ariya/phantomjs/downloads/phantomjs-1.9.8-linux-x86_64.tar.bz2
RUN tar xjf /usr/local/phantomjs-1.9.8-linux-x86_64.tar.bz2 --directory=/usr/local
RUN rm -f /usr/local/phantomjs-1.9.8-linux-x86_64.tar.bz2
ENV PHANTOMJS_PATH /usr/local/phantomjs-1.9.8-linux-x86_64/bin/

RUN mkdir /cache
RUN mkdir /app
