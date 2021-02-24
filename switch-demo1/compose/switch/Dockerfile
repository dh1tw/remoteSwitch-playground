FROM alpine:3

ARG release=v0.5.2
ARG arch=amd64
ARG os=linux
ARG url=https://github.com/dh1tw/remoteSwitch/releases/download/${release}/remoteSwitch-${release}-${os}-${arch}.zip

RUN apk add --no-cache libc6-compat \
    && wget ${url} \
    && unzip *.zip \
    && rm *.zip \
    && mv ./remoteSwitch /bin

COPY ./config /app

WORKDIR /app
