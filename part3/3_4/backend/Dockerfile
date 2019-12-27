FROM node:10-alpine

RUN apk add --no-cache git && \
    git clone https://github.com/docker-hy/backend-example-docker.git && \
    adduser -D app && \
    apk del git && \
    chown -R app backend-example-docker/ 
 
USER app 

WORKDIR /backend-example-docker
RUN npm install
ENV FRONT_URL=http://localhost:5000
EXPOSE 8000
CMD ["npm", "start"]
