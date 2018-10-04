FROM ruby

RUN apt-get update -qq && apt-get install -y nodejs && gem install rails && gem install bundler

ONBUILD COPY . /opt/app
ONBUILD WORKDIR /opt/app

ONBUILD RUN bundle install
ONBUILD EXPOSE 3000

ONBUILD RUN rake db:migrate
ONBUILD RUN rake db:seed

#git clone https://github.com/RailsApps/rails-signup-thankyou
#git clone https://bitbucket.org/railstutorial/sample_app_4th_ed.git
