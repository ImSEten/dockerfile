FROM ubuntu:latest
SHELL ["/bin/bash", "-c"]
RUN apt-get update && apt-get upgrade -y && apt-get install -y git wget curl ssh vim iproute2 net-tools iputils-ping iputils-tracepath inetutils-telnet tcpdump netcat-openbsd && NVM_VERSION=v0.40.4 && curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/$NVM_VERSION/install.sh | bash && NVM_DIR="/root/.nvm" && [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" && [ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion" && NODE_VERSION=v24.15.0 && nvm install $NODE_VERSION && nvm alias default v24.15.0 && PATH=$PATH:/root/.nvm/versions/node/$NODE_VERSION/bin && npm install -g openclaw@latest
COPY ./start.sh /root/start.sh
