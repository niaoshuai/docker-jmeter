FROM registry.cn-beijing.aliyuncs.com/niao-jmeter/jmeter-base:1.0.0

MAINTAINER niaoshuai <niao.shuai123@163.com>

ARG REMOTE_HOSTS
ARG JMX_PATH
ARG CSV_PATH

ENTRYPOINT ["jmeter","-n","-t","${JMX_PATH},"-l","CSV_PATH","-R","${REMOTE_HOSTS}"]
