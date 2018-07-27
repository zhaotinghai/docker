FROM alpine:3.8

MAINTAINER zhaotinghai <zhaotinghai@sina.cn>

RUN apk --no-cache add dnsmasq

#ADD config/* /etc/

EXPOSE 53 53/udp

ENTRYPOINT ["dnsmasq", "-k"]
