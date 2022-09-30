FROM alpine as builder
ADD "https://github.com/shadowsocks/v2ray-plugin/releases/download/v1.3.2/v2ray-plugin-linux-amd64-v1.3.2.tar.gz" .
RUN tar -xzf v2ray-plugin-linux-amd64-v1.3.2.tar.gz

FROM shadowsocks/shadowsocks-libev:v3.3.5
ENV USER=nobody
COPY --from=builder v2ray-plugin_linux_amd64 /usr/bin/v2ray-plugin