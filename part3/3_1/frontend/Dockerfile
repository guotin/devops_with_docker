FROM ubuntu:16.04

RUN apt-get update && apt-get install -y curl git && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt-get install -y nodejs && \
    git clone https://github.com/docker-hy/frontend-example-docker.git && \
    apt-get purge -y --auto-remove curl git && \ 
    rm -rf /var/lib/apt/lists/* 

WORKDIR /frontend-example-docker
RUN npm install
ENV API_URL=http://localhost:8000
EXPOSE 5000
CMD ["npm", "start"]
