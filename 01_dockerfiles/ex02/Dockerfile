#Bundler provides a consistent environment for Ruby projects by tracking and installing the exact gems and versions that are needed.

FROM ruby

RUN apt-get update -qq && apt-get install -y nodejs && gem install rails && gem install bundler

ONBUILD COPY . /opt/app
ONBUILD WORKDIR /opt/app

ONBUILD RUN bundle install
ONBUILD EXPOSE 3000

ONBUILD RUN rake db:migrate
ONBUILD RUN rake db:seed

#Rake is a utility built into Ruby and Rails, which provides an efficient way for managing database changes.
#Migrations setup the tables in the database.When you run rake db:seed it will load all the admin data into your application.

#Applications for testing:
#git clone https://github.com/RailsApps/rails-signup-thankyou
#git clone https://bitbucket.org/railstutorial/sample_app_4th_ed.git

#how to use this Dockerfile:
#1)in Ex02 folder run: docker build -t ft-rails:on-build .
#2)git clone one of the apps. Go into an app folder and create the Dockerfile provided by the subject.
#3)in app folder run: docker build -t myapp -f Dockerfile .
#4)to launch the app run: docker run -p 3000:3000 --rm myapp
#5)to verify go to browser and at the end of ip address add :3000
