FROM node:12-alpine

# latest https://github.com/aws/aws-cdk/releases
ENV CDK_VERSION=1.94.1

RUN apk --update add --virtual build-deps --no-cache curl gcc musl-dev \
        linux-headers build-base ca-certificates bash \
        python3 p3-pip python3-dev \
        jq git
    #    jq git && \
    #python3 -m ensurepip && \
    #rm -r /usr/lib/python*/ensurepip && \
    #pip3 install --upgrade pip setuptools && \
    #if [ ! -e /usr/bin/pip ]; then ln -s pip3 /usr/bin/pip ; fi && \
    #rm -r /root/.cache

RUN pip3 install --upgrade pip
#RUN apk add --no-cache tzdata

RUN npm -g install cdk@$CDK_VERSION
RUN pip3 install awscli

#RUN apk del build-deps
RUN rm -rf /var/cache/apk/*

WORKDIR /work

ENTRYPOINT ["/bin/bash"]
#CMD ["/bin/sh"]
