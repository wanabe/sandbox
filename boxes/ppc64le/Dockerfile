FROM debian:stretch AS qemu-src
RUN apt-get update && apt-get install -y qemu-user-static

FROM ppc64le/debian:stretch
COPY --from=qemu-src /usr/bin/qemu-ppc64le-static /usr/bin/qemu-ppc64le-static
RUN sed -i -e 's|http://deb.debian.org/|http://cdn-fastly.deb.debian.org/|' /etc/apt/sources.list
RUN apt-get update && apt-get install -y git
