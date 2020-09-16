FROM frrouting/frr:v7.3.1
MAINTAINER Jake Holland <jholland@akamai.com>

# this is a stub to just provide a pim upstream, because without one
# the FRR pimd does not propagate the forwarding information base for
# joins upstream.

RUN mkdir /var/log/frr/
RUN chown frr:frr /var/log/frr/

RUN rm -r /etc/frr/*
COPY frr/* /etc/frr/
RUN chown frr:frr /etc/frr/*

ENTRYPOINT [ "/sbin/tini", "--", "/usr/lib/frr/docker-start" ]

