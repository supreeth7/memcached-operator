FROM quay.io/app-sre/boilerplate:image-v2.2.0 AS builder

ENV OPERATOR=/usr/local/bin/memcached-operator-0.17 \
    USER_UID=1001 \
    USER_NAME=memcached-operator-0.17

# install operator binary
COPY build/_output/bin/memcached-operator-0.17 ${OPERATOR}

COPY build/bin /usr/local/bin
RUN  /usr/local/bin/user_setup

ENTRYPOINT ["/usr/local/bin/entrypoint"]

USER ${USER_UID}
