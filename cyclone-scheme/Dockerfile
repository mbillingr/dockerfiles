from alpine:latest

RUN apk add zsh grml-zsh-config git make clang musl-dev ck-dev

#ENV CYCLONE_VERSION v0.35.0
ENV CYCLONE_VERSION master

RUN git clone https://github.com/justinethier/cyclone-bootstrap
WORKDIR cyclone-bootstrap
RUN git checkout ${CYCLONE_VERSION}
RUN make -j
RUN make install

WORKDIR /

