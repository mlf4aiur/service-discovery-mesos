FROM ruby:2-alpine

ENV LISTEN_PORT 4567

RUN mkdir -p /myapp
WORKDIR /myapp

COPY . /myapp

RUN bundle config --global frozen 1 \
    && bundle install \
    && chmod u+x ./stocks.rb

CMD ["./stocks.rb"]
