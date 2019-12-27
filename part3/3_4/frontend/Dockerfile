FROM node:10-alpine

RUN apk add --no-cache git && \
    git clone https://github.com/docker-hy/frontend-example-docker.git && \
    adduser -D app && \
    apk del git && \
    chown -R app frontend-example-docker/ 
 
USER app 

WORKDIR /frontend-example-docker
RUN npm install
ENV API_URL=http://localhost:8000
EXPOSE 5000
CMD ["npm", "start"]
