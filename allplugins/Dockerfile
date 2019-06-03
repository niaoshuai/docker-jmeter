FROM registry.cn-beijing.aliyuncs.com/niao-jmeter/jmeter-base:1.0.0

MAINTAINER niaoshuai <niao.shuai123@163.com>

RUN apt-get -y update && \
	apt-get -y install \
	wget \
	unzip 
	
RUN wget -P  ${JMETER_HOME}/lib/ext https://github.com/niaoshuai/docker-jmeter/blob/master/allplugins/JMeter-InfluxDB-Writer-plugin-1.2.jar?raw=true \
    wget -P  ${JMETER_HOME}/lib/ext https://github.com/niaoshuai/docker-jmeter/blob/master/allplugins/jmeter-plugins-casutg-2.8.jar?raw=true

RUN apt-get -y remove wget unzip && \
	apt-get -y --purge autoremove && \
	apt-get -y clean && \
	rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
