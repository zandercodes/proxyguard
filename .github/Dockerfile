FROM --platform=$BUILDPLATFORM scratch

LABEL org.opencontainers.image.authors="Julian Zander <admin@zandercodes.com>" \
      org.opencontainers.image.description="A simple proxy server for WireGuard" \
      org.opencontainers.image.licenses="MIT" \
      org.opencontainers.image.source="https://github.com/zandercodes/proxyguard" \
      org.opencontainers.image.title="proxyguard-server" \
      org.opencontainers.image.url="https://github.com/zandercodes/proxyguard"

COPY /proxyguard/proxyguard-server /proxyguard-server

EXPOSE 51821/tcp

ENTRYPOINT ["/proxyguard-server"]
CMD ["--listen", "[::]:51821", "--to", "127.0.0.1:51820"]