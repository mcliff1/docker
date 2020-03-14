FROM node:10-alpine

CDK_VERSION=1.27.0

RUN apk --update add --virtual build-deps --no-cache curl gcc musl-dev python2-dev python3 && \
    apk --update add jq git

RUN npm -g install cdk@${CDK_VERSION}

RUN apk del build-deps
rm -rf /var/cache/apk/*

WORKDIR /work

#ENTRYPOINT ["/usr/local/bin/sam"]
CMD ["/bin/sh"]
