# Docker 部署 Springboot

## 第一种：

### 1.在idea终端运行命令mvn package生成jar包放至服务器中

### 2.在jar包所在文件夹下编写Dockerfile:

```dockerfile
FROM openjdk:8
VOLUME /tmp
ADD implementstest-0.0.1-SNAPSHOT.jar app.jar
EXPOSE 9999
ENTRYPOINT ["java","-jar","/app.jar"]
```

### 3.build自己的镜像

```
docker build -t docker_springboot .
```

## 参考

<https://spring.io/guides/gs/spring-boot-docker/>

