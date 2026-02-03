FROM node:22-alpine

# latest https://github.com/aws/aws-cdk/releases
ENV CDK_VERSION=2.1104.0

RUN apk update && \
    apk add --no-cache \
        curl \
        gcc \
        musl-dev \
        linux-headers \
        build-base \
        ca-certificates \
        bash \
        python3 \
        py3-pip \
        python3-dev \
        jq \
        git \
        openssh

#RUN pip3 install --upgrade pip
RUN npm -g install aws-cdk@$CDK_VERSION
RUN pip3 install awscli

RUN rm -rf /var/cache/apk/*

WORKDIR /work

ENTRYPOINT ["/bin/bash"]
