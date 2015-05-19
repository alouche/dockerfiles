from alouche/mesosphere:mesos
MAINTAINER Ali Abbas <ali@alouche.net>

RUN yum -y update; yum clean all
RUN yum -y install chronos; yum clean all
RUN rm /etc/mesos/zk
RUN rm /etc/chronos/conf/http_port

ENTRYPOINT ["/usr/bin/chronos"]
