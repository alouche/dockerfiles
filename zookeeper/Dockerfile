from centos:centos7
MAINTAINER Ali Abbas <ali@alouche.net>

RUN yum -y update; yum clean all
# packages do work with centos7 although marked for el6
RUN rpm -ivh http://archive.cloudera.com/cdh5/one-click-install/redhat/6/x86_64/cloudera-cdh-5-0.x86_64.rpm
RUN rpm --import http://archive.cloudera.com/cdh5/redhat/6/x86_64/cdh/RPM-GPG-KEY-cloudera
RUN yum install -y java-1.8.0-openjdk-devel zookeeper-server; yum clean all
RUN service zookeeper-server init
RUN echo 1 | tee -a /var/lib/zookeeper/myid >/dev/null


ENTRYPOINT ["/usr/lib/zookeeper/bin/zkServer.sh"]
CMD ["start-foreground"]
