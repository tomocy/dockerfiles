FROM debian

RUN apt-get update && apt-get install -y \
    curl \
    git \
    unzip \
    xz-utils \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

ENV WORKDIR /root
WORKDIR $WORKDIR
RUN curl -o flutter -L https://storage.googleapis.com/flutter_infra/releases/stable/linux/flutter_linux_v1.9.1+hotfix.6-stable.tar.xz \
 && tar xf flutter
ENV PATH $PATH:$WORKDIR/flutter/bin:$WORKDIR/flutter/bin/cache/dart-sdk/bin/
RUN flutter precache