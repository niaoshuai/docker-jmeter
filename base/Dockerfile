FROM openjdk:8u212-jre-stretch

MAINTAINER niaoshuai <niao.shuai123@163.com>

ENV JMETER_VERSION=5.1
ENV JMETER_HOME=/usr/local/apache-jmeter-${JMETER_VERSION}
ENV PATH=${JMETER_HOME}/bin:${PATH}

RUN apt-get -y update && \
	apt-get -y install wget 

RUN wget http://mirrors.tuna.tsinghua.edu.cn/apache//jmeter/binaries/apache-jmeter-${JMETER_VERSION}.tgz && \
	tar -xzf apache-jmeter-${JMETER_VERSION}.tgz -C /usr/local/

RUN rm -rf apache-jmeter-${JMETER_VERSION}.tgz \
			${JMETER_HOME}/bin/examples \
			${JMETER_HOME}/bin/templates \
			${JMETER_HOME}/bin/*.cmd \
			${JMETER_HOME}/bin/*.bat \
			${JMETER_HOME}/docs \
			${JMETER_HOME}/printable_docs && \
	apt-get -y remove wget && \
	apt-get -y --purge autoremove && \
	apt-get -y clean && \
	rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

WORKDIR /usr/local/apache-jmeter-${JMETER_VERSION}

# server.rmi.ssl.disable=false
RUN sed -i 's/^#server.rmi.ssl.disable=false/server.rmi.ssl.disable=true/' bin/jmeter.properties
