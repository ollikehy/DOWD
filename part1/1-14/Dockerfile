FROM ruby:2.6.0

RUN bundle config --global frozen 1

COPY Gemfile Gemfile.lock ./

WORKDIR /example

EXPOSE 3000

RUN apt-get update && apt-get -y install curl

RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs

RUN bundle install

COPY . .

RUN rails db:migrate

CMD ["rails" , "s"]