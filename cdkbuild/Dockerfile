FROM node:20-alpine

# latest https://github.com/aws/aws-cdk/releases
ENV CDK_VERSION=2.93.0
#ENV CDK_VERSION=1.204.0

RUN apk --update add --virtual build-deps --no-cache curl gcc musl-dev \
        linux-headers build-base ca-certificates bash \
        python3 py3-pip python3-dev \
        jq git openssh

#RUN pip3 install --upgrade pip
#RUN apk add --no-cache tzdata

RUN npm -g install cdk@$CDK_VERSION
RUN pip3 install awscli

#RUN apk del build-deps
RUN rm -rf /var/cache/apk/*

WORKDIR /work

ENTRYPOINT ["/bin/bash"]
#CMD ["/bin/sh"]
