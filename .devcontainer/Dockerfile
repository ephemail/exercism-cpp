FROM docker.io/debian:stable

RUN apt update && apt install -y fish git wget

RUN mkdir -p ~/bin ~/.config/fish/completions \
    && wget https://github.com/exercism/cli/releases/download/v3.5.8/exercism-3.5.8-linux-x86_64.tar.gz -O exercism.tar.gz \
    && tar -xzf exercism.tar.gz -C ~/bin exercism \
    && tar -xzf exercism.tar.gz -C ~/.config/fish/completions --strip-components=1 shell/exercism.fish \
    && rm exercism.tar.gz

ENV PATH="$PATH:/root/bin"
