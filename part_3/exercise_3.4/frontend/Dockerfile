FROM node:13.6-slim

COPY ./frontend-example-docker /app
WORKDIR /app

RUN npm install && \
API_URL=http://localhost:8888 npm run build && \
npm install -g serve && \
useradd -m app

RUN chown app /app -R

USER app
EXPOSE 5000

CMD serve -s -l 5000 dist
