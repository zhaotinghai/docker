FROM alpine:3.8

MAINTAINER zhaotinghai <zhaotinghai@sina.cn>

RUN apk upgrade --update && \
    && apk add --no-cache bash dnsmasq \
    && rm -rf /var/cache/apk/*

#ADD config/* /etc/

EXPOSE 53 53/udp

ENTRYPOINT ["dnsmasq", "-k"]
