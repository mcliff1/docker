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

# Create and activate a virtual environment
RUN python3 -m venv /opt/venv
ENV PATH="/opt/venv/bin:$PATH"

RUN pip install --upgrade pip
RUN npm -g install aws-cdk@$CDK_VERSION
RUN pip install awscli

# Install matts-toolbox from private GitLab PyPI repository
# The package is from https://gitlab.com/cliffaws/pypack
# Use BuildKit secret mount to avoid exposing the token in image layers
RUN --mount=type=secret,id=gitlab_token \
    if [ -f /run/secrets/gitlab_token ]; then \
        GITLAB_TOKEN=$(cat /run/secrets/gitlab_token) && \
        pip install matts-toolbox==0.2.4 \
            --index-url https://__token__:${GITLAB_TOKEN}@gitlab.com/api/v4/projects/cliffaws%2Fpypack/packages/pypi/simple \
            --extra-index-url https://pypi.org/simple; \
    else \
        echo "Warning: GITLAB_TOKEN not provided. Skipping matts-toolbox installation."; \
    fi

RUN rm -rf /var/cache/apk/*

WORKDIR /work

# Ensure venv is activated in interactive shells
RUN echo "source /opt/venv/bin/activate" >> /root/.bashrc

ENTRYPOINT ["/bin/bash"]
