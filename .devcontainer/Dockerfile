from docker.io/ubuntu:noble-20241011

RUN apt-get update && apt-get install -y perl wget && \
    wget -qO- "https://yihui.org/tinytex/install-bin-unix.sh" | sh && \
    apt-get clean

ENV PATH=$PATH:/root/.TinyTeX/bin/x86_64-linux

# This is required as the most geographically close Mirrors to me don't seem to work.
RUN tlmgr option repository http://mirror.ctan.org/systems/texlive/tlnet

RUN tlmgr install