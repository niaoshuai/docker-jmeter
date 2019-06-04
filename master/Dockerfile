FROM registry.cn-beijing.aliyuncs.com/niao/jmeter-base-plugin:1.0.0

MAINTAINER niaoshuai <niao.shuai123@163.com>

#ARG REMOTE_HOSTS
#ARG JMX_PATH
#ARG CSV_PATH

#ENTRYPOINT ["jmeter","-n","-t","${JMX_PATH},"-l","CSV_PATH","-R","${REMOTE_HOSTS}"]
ENTRYPOINT ["jmeter.sh","-n","-Jclient.tries=3","-Jclient.retries_delay=10000","-Jclient.continue_on_fail=true"]
