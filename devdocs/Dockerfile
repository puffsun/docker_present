
FROM ruby
RUN apt-get update
RUN apt-get install -y build-essential nodejs git-core
RUN mkdir /source
WORKDIR /source
RUN git clone https://github.com/Thibaut/devdocs.git
RUN cd devdocs && bundle install && thor docs:download --all
RUN rackup
EXPOST 9292
