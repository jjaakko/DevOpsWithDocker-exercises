FROM ubuntu:16.04
EXPOSE 5000
RUN apt-get update && apt-get install -y curl && apt-get install -y git
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs

WORKDIR /root
RUN git clone https://github.com/docker-hy/frontend-example-docker.git
WORKDIR /root/frontend-example-docker

RUN npm install
RUN API_URL=http://localhost/api npm run build
RUN npm install -g serve
CMD serve -s -l 5000 dist
