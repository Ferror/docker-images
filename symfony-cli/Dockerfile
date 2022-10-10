FROM alpine:3.16

ARG CLI_VERSION=5.4.16

RUN apk add --no-cache bash curl && \
    curl -1sLf https://dl.cloudsmith.io/public/symfony/stable/setup.alpine.sh | bash && \
    apk add --no-cache symfony-cli && \
    apk del bash curl && \
    rm -rf /var/cache/apk/*

#RUN apk add --no-cache wget && \
#    wget https://github.com/symfony-cli/symfony-cli/releases/download/v${CLI_VERSION}/symfony-cli_${CLI_VERSION}_aarch64.apk && \
#    apk add --no-cache symfony-cli_${CLI_VERSION}_aarch64.apk && \
#    rm symfony-cli_${CLI_VERSION}_aarch64.apk

ENTRYPOINT ["symfony"]
