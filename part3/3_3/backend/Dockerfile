FROM ubuntu:16.04

RUN apt-get update && apt-get install -y curl git && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt-get install -y nodejs && \
    git clone https://github.com/docker-hy/backend-example-docker.git && \
    apt-get purge -y --auto-remove curl git && \ 
    rm -rf /var/lib/apt/lists/* && \
    useradd -m app && \
    chown -R app backend-example-docker/ 
 
USER app 

WORKDIR /backend-example-docker
RUN npm install
ENV FRONT_URL=http://localhost:5000
EXPOSE 8000
CMD ["npm", "start"]
