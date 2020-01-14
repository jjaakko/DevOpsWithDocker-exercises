FROM python:3.8-slim

RUN apt-get update && apt-get install -y \
ffmpeg && \
pip install --user --upgrade yle-dl && \
mv $HOME/.local/bin/yle-dl /usr/local/bin/.

WORKDIR /videos
ENTRYPOINT ["/usr/local/bin/yle-dl"] 