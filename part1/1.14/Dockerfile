FROM ruby:2.6.0

COPY rails-example-project .
RUN bundle install

RUN apt-get update && apt-get install -y --allow-unauthenticated nodejs

RUN rails db:migrate

EXPOSE 3000
CMD ["rails", "s"]