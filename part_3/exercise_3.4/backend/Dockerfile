FROM node:13.6-slim
EXPOSE 8000
RUN mkdir /app && \
useradd -m app

COPY backend-example-docker /app
RUN chown app /app -R

USER app
WORKDIR /app

RUN npm install
CMD FRONT_URL=http://localhost:8001 npm start