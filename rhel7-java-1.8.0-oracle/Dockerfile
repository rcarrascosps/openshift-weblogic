FROM container-registry.oracle.com/oraclelinux:7-slim
MAINTAINER Rolando Carrasco <rcarrasco@spsolutions.com.mx>

ENV JAVA_VERSION=${JAVA_VERSION:-1.8.0} \
    JAVA_TYPE=${JAVA_TYPE:-oracle}

ENV JAVA_HOME=/usr/lib/jvm/java-${JAVA_VERSION}-${JAVA_TYPE}

RUN yum --disablerepo=* \
        --enablerepo=rhel-7-server-rpms \
        --enablerepo=rhel-7-server-extras-rpms \
        --enablerepo=rhel-7-server-optional-rpms \
        --enablerepo=rhel-7-server-thirdparty-oracle-java-rpms \
      install -y \
      java-1.8.0-oracle-devel-1.8.0.171-1jpp.2.el6.x86_64.rpm \
      java-${JAVA_VERSION}-${JAVA_TYPE}-jdbc && \
    yum clean all
