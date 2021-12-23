FROM ruby:2.7

ENV LANG=C.UTF-8 \
  TZ=Asia/Tokyo

RUN apt-get update -qq && apt-get install -y nodejs default-mysql-client

WORKDIR /app

COPY Gemfile /app/Gemfile
COPY Gemfile.lock /app/Gemfile.lock

RUN bundle install

COPY docker-entrypoint.sh /docker-entrypoint.sh

CMD [ "/docker-entrypoint.sh" ]
