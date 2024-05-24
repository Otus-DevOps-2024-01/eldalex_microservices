FROM ruby:2.4

RUN echo "deb [trusted=yes] http://archive.debian.org/debian/ jessie main" > /etc/apt/sources.list.d/debian-archive.list


RUN apt-get update -qq --allow-unauthenticated && apt-get install -y build-essential

ENV APP_HOME /app
RUN mkdir $APP_HOME
WORKDIR $APP_HOME

ADD Gemfile* $APP_HOME/
RUN bundle install
ADD . $APP_HOME

ENV COMMENT_DATABASE_HOST comment_db
ENV COMMENT_DATABASE comments

CMD ["puma"]
