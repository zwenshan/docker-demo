# docker-demo
docker 学习笔记
> - 1   ADD jdk-7u80-linux-x64.tar.gz $WORK_HOME 可识别的镜像文件，容器会自动解压缩
> - 2  docker run 命令后面的／bin/bash会替换掉dockerfile里面的cmd命令
> - 3  ENTRYPOINT 可以接收docker run 的参数
# Dockerfile demo 

> - FROM  hub.c.163.com/library/tomcat:7.0-jre7
> - MAINTAINER " <XX27@gmail.com>"
> - RUN rm -rvf /usr/local/tomcat/webapps/ROOT
> - ADD wxsmall.war /usr/local/tomcat/webapps/ROOT.war
> - EXPOSE 8080
# Docker 结果 格式化
> - docker inspect --format='{status:{{.State.Status}},IPAddress:{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}}' a1
