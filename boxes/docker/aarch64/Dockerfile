FROM debian:stretch AS qemu-src
RUN apt-get update && apt-get install -y qemu-user-static

FROM arm64v8/debian:stretch
COPY --from=qemu-src /usr/bin/qemu-aarch64-static /usr/bin/qemu-aarch64-static
RUN apt-get update && apt-get install -y git
