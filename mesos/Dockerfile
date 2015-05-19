from centos:centos7
MAINTAINER Ali Abbas <ali@alouche.net>

RUN yum -y update; yum clean all
RUN rpm -ivh http://repos.mesosphere.io/el/7/noarch/RPMS/mesosphere-el-repo-7-1.noarch.rpm
RUN yum -y install mesos; yum clean all
