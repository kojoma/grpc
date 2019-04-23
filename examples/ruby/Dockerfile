FROM ruby:2.6.3

ENV WORK_DIR=/grpc BUNDLE_PATH=/vendor/bundle LANG=C.UTF-8 LC_ALL=C.UTF-8

RUN \
  mkdir $WORK_DIR \
  mkdir -p $BUNDLE_PATH
WORKDIR /grpc

RUN gem install bundler
COPY Gemfile $WORK_DIR
COPY Gemfile.lock $WORK_DIR
COPY grpc-demo.gemspec $WORK_DIR
RUN BUNDLER_VERSION=1.17.3 bundle install
