FROM alpine:3.7
RUN apk update \
    && apk add --no-cache --virtual build-dependencies \
                         build-base \
                         gcc \
                         wget \
                         git \
    && apk add ruby \
               ruby-dev \
    && gem install bundler --no-ri --no-rdoc

ENV APP_HOME /app
RUN mkdir $APP_HOME

WORKDIR $APP_HOME
ADD Gemfile* $APP_HOME/
RUN bundle install

RUN apk del build-dependencies

ADD . $APP_HOME

ENV POST_SERVICE_HOST post
ENV POST_SERVICE_PORT 5000
ENV COMMENT_SERVICE_HOST comment
ENV COMMENT_SERVICE_PORT 9292

CMD ["puma"]
