FROM ubuntu:21.10

ENV COCOAPODS_ALLOW_ROOT=true
ENV LANG=C.UTF-8
ENV NG_CLI_ANALYTICS=ci

RUN apt-get update && apt-get install -y git ruby-full curl build-essential
RUN curl -sL https://deb.nodesource.com/setup_14.x | bash -
RUN apt-get update && apt-get -y install nodejs

RUN gem install cocoapods
RUN pod setup

RUN npm install -g @ionic/cli
RUN npm install -g capacitor
RUN npm install -g capacitor-resources
RUN npm install -g @angular/cli

WORKDIR /app

EXPOSE 8100:8100
EXPOSE 4200:8100

ENTRYPOINT ["/bin/bash"]
