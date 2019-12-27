FROM ubuntu:16.04

RUN apt-get update && apt-get install -y curl git
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt-get install -y nodejs
RUN git clone https://github.com/guotin/HY-Fullstack_2019.git
WORKDIR /HY-Fullstack_2019/Osa_2/maiden_tiedot
RUN npm install
EXPOSE 3000
CMD ["npm", "start"]
