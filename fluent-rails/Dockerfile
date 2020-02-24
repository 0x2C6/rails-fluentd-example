FROM ruby:2.7.0
RUN apt-get update -qq && apt-get install -y nodejs curl git sqlite3
RUN curl -o- -L https://yarnpkg.com/install.sh | bash
RUN mkdir /app
WORKDIR /app
COPY Gemfile /app/Gemfile
COPY Gemfile.lock /app/Gemfile.lock
RUN bundle install
COPY . /app

EXPOSE 3000