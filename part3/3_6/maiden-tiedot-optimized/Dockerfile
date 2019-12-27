FROM ubuntu:16.04 as build-stage

RUN apt-get update && apt-get install -y curl git
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs
RUN git clone https://github.com/guotin/HY-Fullstack_2019.git
WORKDIR /HY-Fullstack_2019/Osa_2/maiden_tiedot
RUN npm install && npm run build

FROM node:10-alpine
COPY --from=build-stage HY-Fullstack_2019/Osa_2/maiden_tiedot/build ./build

RUN npm install -g serve && \
    adduser -D app && \
    chown -R app ./build/

USER app

EXPOSE 3000
CMD serve -s -l 3000 build
