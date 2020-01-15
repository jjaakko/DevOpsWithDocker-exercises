FROM node:13.6-alpine as build-stage

COPY ./frontend-example-docker /app
WORKDIR /app

RUN npm install && \
API_URL=http://localhost:8888 npm run build

FROM node:13.6-alpine

COPY --from=build-stage /app/dist /app/dist

RUN adduser -D app

RUN npm install -g serve && \
chown app /app -R

WORKDIR /app
USER app
EXPOSE 5000

CMD serve -s -l 5000 dist
