ARG BASE=alpine
FROM $BASE

ARG arch=none
ENV ARCH=$arch

COPY qemu/qemu-$ARCH-static* /usr/bin/

COPY . /container
RUN /container/build.sh

ENV LANG="en_US.UTF-8" \
    LANGUAGE="en_US:en" \
    LC_ALL="en_US.UTF-8"

ENTRYPOINT ["/container/tool/run"]
