FROM --platform=linux/amd64 node:lts-bookworm-slim
SHELL ["/bin/bash", "-c"]
RUN apt update && apt install -y curl bash git tar gzip libc++-dev unzip
RUN curl -fsSL https://bun.sh/install | bash
RUN curl -L https://raw.githubusercontent.com/noir-lang/noirup/refs/heads/main/install | bash
RUN curl -L https://raw.githubusercontent.com/AztecProtocol/aztec-packages/refs/heads/master/barretenberg/bbup/install | bash
RUN echo "PATH=$PATH:/home/codespace/.nargo/bin:$PATH" >> ~/.zshrc
RUN echo "PATH=$PATH:/home/codespace/.bb:$PATH" >> ~/.zshrc
RUN . ~/.zshrc
