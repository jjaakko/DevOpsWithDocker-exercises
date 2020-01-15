FROM ubuntu:16.04
EXPOSE 8000
RUN apt-get update && apt-get install --fix-missing -y \
curl && \
curl -sL https://deb.nodesource.com/setup_10.x | bash  && \
apt-get install -y nodejs && \
apt-get purge -y --auto-remove curl && \ 
rm -rf /var/lib/apt/lists/* && \
mkdir /app && \
useradd -m app && chown app /app -R

USER app

WORKDIR /app
COPY backend-example-docker /app
WORKDIR /app

RUN npm install
CMD FRONT_URL=http://localhost:8001 npm start