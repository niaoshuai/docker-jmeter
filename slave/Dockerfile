FROM registry.cn-beijing.aliyuncs.com/niao-jmeter/jmeter-base:1.0.0

MAINTAINER niaoshuai <niao.shuai123@163.com>

EXPOSE 1099

# server.rmi.create=false
RUN sed -i "s#^server.rmi.create=.*#server.rmi.create=false#g"  bin/jmeter-server

ENTRYPOINT ["jmeter-server"]
