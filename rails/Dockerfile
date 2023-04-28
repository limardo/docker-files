FROM ruby:2.7.8
RUN apt-get update -qq && \
    apt-get install build-essential nodejs postgresql-client -y --no-install-recommends && \
    rm -rf /var/lib/apt/lists/*
WORKDIR /app

COPY Gemfile Gemfile.lock /app/
COPY ./src /app/
RUN bundle install

COPY entrypoint.sh /usr/bin/
RUN chmod +x /usr/bin/entrypoint.sh
ENTRYPOINT ["entrypoint.sh"]

EXPOSE 3000

CMD ["rails", "server", "-b", "0.0.0.0"]
