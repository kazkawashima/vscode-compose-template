FROM node:16
#https://zenn.dev/leftletter/articles/0969dcef061ff8
RUN apt-get update

#RUN npm i -g create-react-app
RUN npm install -g node-gyp
#RUN curl https://sdk.cloud.google.com | bash

#RUN curl https://sdk.cloud.google.com > install.sh 
RUN bash install.sh --disable-prompts --usage-reporting false --rc-path ~/.bashrc --command-completion true --path-update true
#RUN bash ./bin/gcloud init
RUN npm install -g firebase-tools

