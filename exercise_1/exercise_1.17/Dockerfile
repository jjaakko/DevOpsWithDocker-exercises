FROM ubuntu:16.04
#RUN apt-get update && apt-get install -y curl && apt-get install -y git
RUN apt-get update  && apt-get install -y git
# && apt-get upgrade
RUN apt-get install debconf-utils
RUN echo "tzdata    tzdata/Areas    select    Europe" | debconf-set-selections
RUN echo "tzdata    tzdata/Zones/Europe    select    Helsinki" | debconf-set-selections
# RUN apt-get update & apt-get install -y git
# RUN apt-get install -y build-essential checkinstall zlib1g-dev
RUN apt-get install -y --no-install-recommends make build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev
RUN git clone https://github.com/pyenv/pyenv.git ~/.pyenv
RUN echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
RUN echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
RUN echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.bashrc
RUN echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.bashrc
#RUN echo 'if command -v pyenv 1>/dev/null 2>&1; then\n  eval "$(pyenv init -)"\nfi' >> ~/.bashrc
RUN echo 'eval "$(pyenv init -)"' >> ~/.bashrc
RUN ["/bin/bash", "-c", "source ~/.bashrc"]
RUN ["/bin/bash", "-c", "exec \"$SHELL\""]
#RUN source $HOME/.bashrc
#RUN pyenv install 3.6.8
RUN ~/.pyenv/bin/pyenv install 2.7.17


# WORKDIR $HOME

# apt install build-essential checkinstall zlib1g-dev -y
# apt-get update; apt-get install --no-install-recommends make build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev