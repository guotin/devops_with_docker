FROM ubuntu:16.04 as build-stage

RUN apt-get update && apt-get install -y curl git && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt-get install -y nodejs && \
    git clone https://github.com/docker-hy/frontend-example-docker.git

WORKDIR /frontend-example-docker
RUN npm install && npm run build

FROM node:10-alpine
COPY --from=build-stage /frontend-example-docker/dist ./dist

RUN npm install -g serve && \
    adduser -D app && \
    chown -R app ./dist/

USER app

ENV API_URL=http://localhost:8000
EXPOSE 5000
CMD serve -s -l 5000 dist
