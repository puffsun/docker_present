
FROM ruby
RUN apt-get update
RUN apt-get install -y build-essential nodejs git-core
RUN mkdir /source
WORKDIR /source
RUN git clone https://github.com/Thibaut/devdocs.git
WORKDIR /source/devdocs
RUN bundle install --verbose
CMD ['thor', 'docs:download', '--all']
EXPOSE 9292
