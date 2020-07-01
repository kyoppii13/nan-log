FROM ruby:2.6.5
ENV LANG C.UTF-8

RUN apt-get update -qq && apt-get install -y \
  build-essential \
  nodejs \
  && rm -rf /var/lib/apt/lists/*

RUN curl -o /usr/local/bin/berglas https://storage.googleapis.com/berglas/master/linux_amd64/berglas \
  && chmod a+x /usr/local/bin/berglas

RUN gem install bundler

ENV APP_HOME /app
RUN mkdir -p $APP_HOME
WORKDIR $APP_HOME
ADD . $APP_HOME
