# microservice

```
启动eureka-server
docker run -d --name eureka-server -p 1025:1025 cuiyf/microservice:eureka_server

启动config-server
docker run -d --name config-server -p 8010:8010 -e SPRING_PROFILES_ACTIVE=amqp -e ip=192.168.10.24 cuiyf/microservice:config_server

启动rabbitmq
docker run -d -h mqnode1 --name mqnode1 -p4369:4369 -p5671-5672:5671-5672 -p15671-15672:15671-15672 -p 25672:25672 -e RABBITMQ_NODENAME=rabbitmq@mqnode1 -e RABBITMQ_ERLANG_COOKIE='mqcluster' -e RABBITMQ_DEFAULT_USER=admin -e RABBITMQ_DEFAULT_PASS=admin rabbitmq:3.7-management

启动gitlab
docker run -d -p80:80 -p443:443 -p22:22 -v /home/cyf/docker/gitlab/config:/etc/gitlab -v /home/cyf/docker/gitlab/data:/var/opt/gitlab --name gitlab twang2218/gitlab-ce-zh:11.1
```
