FROM ubuntu:16.04

COPY ./frontend-example-docker /app
WORKDIR /app

RUN apt-get update && apt-get install -y \
curl && \
curl -sL https://deb.nodesource.com/setup_10.x | bash && \
apt-get install -y nodejs && \
npm install && \
API_URL=http://localhost:8888 npm run build && \
npm install -g serve && \
apt-get purge -y --auto-remove curl && \ 
rm -rf /var/lib/apt/lists/*

EXPOSE 5000

CMD serve -s -l 5000 dist
