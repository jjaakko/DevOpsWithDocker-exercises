FROM ubuntu:16.04
RUN apt-get update  && apt-get install -y git

# Ensure that no input is required when installing dependencies for pyenv.
# See https://serverfault.com/a/407358 for more information.
RUN apt-get install debconf-utils
RUN echo "tzdata    tzdata/Areas    select    Europe" | debconf-set-selections
RUN echo "tzdata    tzdata/Zones/Europe    select    Helsinki" | debconf-set-selections

# Use suggested build environment for Ubuntu.
# See https://github.com/pyenv/pyenv/wiki
RUN apt-get install -y --no-install-recommends make build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev

# Install pyenv
RUN git clone https://github.com/pyenv/pyenv.git ~/.pyenv
RUN echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
RUN echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
RUN echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
RUN echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
RUN echo 'eval "$(pyenv init -)"' >> ~/.bashrc
RUN ["/bin/bash", "-c", "source ~/.bashrc"]
RUN ["/bin/bash", "-c", "exec \"$SHELL\""]

# Install multiple versions of Python 
# Why code below doesn't work
# RUN pyenv install 2.7.17
RUN ~/.pyenv/bin/pyenv install 2.7.17
RUN ~/.pyenv/bin/pyenv install 3.6.8