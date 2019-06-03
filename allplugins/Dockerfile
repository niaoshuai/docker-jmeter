FROM registry.cn-beijing.aliyuncs.com/niao-jmeter/jmeter-base:1.0.0

MAINTAINER niaoshuai <niao.shuai123@163.com>

RUN apt-get -y update && \
	apt-get -y install \
	wget \
	unzip 

# Wget
RUN wget -P  ${JMETER_HOME}/lib/ext https://github.com/niaoshuai/docker-jmeter/raw/master/allplugins/JMeter-InfluxDB-Writer-plugin-1.2.jar \
    wget -P  ${JMETER_HOME}/lib/ext https://github.com/niaoshuai/docker-jmeter/raw/master/allplugins/jmeter-plugins-casutg-2.8.jar 

RUN apt-get -y remove wget unzip && \
	apt-get -y --purge autoremove && \
	apt-get -y clean && \
	rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
