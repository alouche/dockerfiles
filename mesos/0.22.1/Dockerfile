from centos:centos7
MAINTAINER Ali Abbas <ali@alouche.net>

ENV MESOS_VERSION 0.22.1

RUN yum -y update; yum clean all
RUN yum -y install epel-release maven python-devel subversion-devel apr-devel zlib-devel libcurl-devel gcc-c++ make patch tar java-1.8.0-openjdk-devel; yum clean all
RUN \
  curl -sSfL http://www.apache.org/dist/mesos/$MESOS_VERSION/mesos-$MESOS_VERSION.tar.gz | tar -xzC /usr/local && \
  cd /usr/local/mesos-$MESOS_VERSION && \
  ./configure && \
  make && \
  make check && \
  make install
