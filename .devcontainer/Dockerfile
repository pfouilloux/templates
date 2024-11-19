FROM mcr.microsoft.com/devcontainers/base:debian

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends bats \
    && apt-get clean -y && rm -rf /var/lib/apt/lists/*

RUN npm install -g @devcontainers/cli