FROM ubuntu:16.04
EXPOSE 8000
RUN apt-get update && apt-get install -y curl && apt-get install -y git
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash
RUN apt install -y nodejs

WORKDIR /root
COPY backend-example-docker /root/.
WORKDIR /root/backend-example-docker

RUN npm install
CMD FRONT_URL=http://localhost:8001 npm start