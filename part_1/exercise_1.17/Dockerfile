FROM python:3.7-slim

RUN apt-get update && apt-get install -y vim && apt-get install -y curl && \
apt-get install -y git && apt-get install -y nginx

# Install node 10.
RUN curl -sL https://deb.nodesource.com/setup_10.x | /bin/bash
RUN apt-get install -y nodejs

# Install flask.
RUN pip install flask
CMD /bin/bash