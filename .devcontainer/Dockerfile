FROM node:19.5-slim

RUN apt update && \
    apt-get -y upgrade && \
    apt-get -y install \
    bash \
    curl \
    git \
    openssh-client \
    unzip && \
    mkdir ~/.ssh && \
    yarn global add serverless && \ 
    curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" && \
    unzip awscliv2.zip && \
    ./aws/install && \
    rm awscliv2.zip && rm -rf ./aws

CMD "/bin/bash"