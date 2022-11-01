# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.245.2/containers/rust/.devcontainer/base.Dockerfile

# [Choice] Debian OS version (use bullseye on local arm64/Apple Silicon): buster, bullseye
ARG VARIANT="buster"
FROM mcr.microsoft.com/vscode/devcontainers/rust:0-${VARIANT}

# [Optional] Uncomment this section to install additional packages.
# RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
#    && apt-get -y install --no-install-recommends <your-package-list-here>

ENV WASI_VERSION=16
ENV WASI_VERSION_FULL=${WASI_VERSION}.0
ENV WASI_SDK_PATH=/usr/local/share/wasi-sdk-${WASI_VERSION_FULL}
RUN curl -L -o - https://github.com/WebAssembly/wasi-sdk/releases/download/wasi-sdk-${WASI_VERSION}/wasi-sdk-${WASI_VERSION_FULL}-linux.tar.gz \
    | tar zx -C /usr/local/share/
