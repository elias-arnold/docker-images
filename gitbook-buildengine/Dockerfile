FROM node:lts-alpine

ENV LANG=C.UTF-8
ENV NG_CLI_ANALYTICS=ci

RUN apk add bash
RUN npm install -g gitbook-cli

WORKDIR /app

EXPOSE 8100:8100
EXPOSE 4200:4200
EXPOSE 4300:4300

ENTRYPOINT ["/bin/bash"]
