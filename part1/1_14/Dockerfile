FROM ruby:2.6.0

RUN git clone https://github.com/docker-hy/rails-example-project.git
RUN gem install bundler
WORKDIR /rails-example-project
RUN bundle install
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get -y install nodejs
RUN rails db:migrate
EXPOSE 3000
CMD rails s
