FROM docker.io/texlive/texlive:latest

RUN echo "ttf-mscorefonts-installer msttcorefonts/accepted-mscorefonts-eula select true" | debconf-set-selections

RUN apt-get update && apt-get install -y \
    fonts-khmeros \
    wget \
    git \
    make \
    fontconfig \
    && rm -rf /var/lib/apt/lists/*

RUN fc-cache -fv

WORKDIR /workspace
CMD ["sleep", "infinity"]
