<<<<<<< HEAD
FROM mcr.microsoft.com/devcontainers/universal:1-focal

# Install .NET SDK
RUN apt-get update && \
    apt-get install -y --no-install-recommends wget gnupg ca-certificates && \
    wget https://packages.microsoft.com/config/ubuntu/ $(lsb_release -rs)/packages-microsoft-prod.deb -O packages-microsoft-prod.deb && \
=======
# Use the universal base image from Microsoft
FROM mcr.microsoft.com/devcontainers/universal:1-focal

# Install .NET SDK 6.0
RUN apt-get update && \
    apt-get install -y --no-install-recommends wget gnupg ca-certificates && \
    wget https://packages.microsoft.com/config/ubuntu/$(lsb_release -rs)/packages-microsoft-prod.deb -O packages-microsoft-prod.deb && \
>>>>>>> 4b48224476e43cfdf015660261398809a05b0da4
    dpkg -i packages-microsoft-prod.deb && \
    rm packages-microsoft-prod.deb && \
    apt-get update && \
    apt-get install -y dotnet-sdk-6.0

# Install Go
ARG GO_VERSION=1.20
<<<<<<< HEAD
RUN wget -O go.tar.gz https://go.dev/dl/go ${GO_VERSION}.linux-amd64.tar.gz && \
=======
RUN wget -O go.tar.gz https://go.dev/dl/go${GO_VERSION}.linux-amd64.tar.gz && \
>>>>>>> 4b48224476e43cfdf015660261398809a05b0da4
    tar -C /usr/local -xzf go.tar.gz && \
    rm go.tar.gz && \
    mkdir -p /home/vscode/go && \
    chown -R vscode:vscode /home/vscode/go

ENV PATH="/usr/local/go/bin:${PATH}"
ENV GOPATH="/home/vscode/go"

USER vscode
WORKDIR /home/vscode

<<<<<<< HEAD
# Install global Node.js packages if needed
=======
# Optional: Install global npm tools
>>>>>>> 4b48224476e43cfdf015660261398809a05b0da4
RUN npm install -g eslint typescript prettier

USER root