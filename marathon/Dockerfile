from alouche/mesosphere:mesos
MAINTAINER Ali Abbas <ali@alouche.net>

RUN yum -y update; yum clean all
RUN yum -y install marathon; yum clean all

ENTRYPOINT ["/usr/bin/marathon"]
