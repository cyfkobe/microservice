FROM cuiyf/oraclejdk:8u201
LABEL cyf <1627999813@qq.com>
COPY target/*.jar app.jar
CMD ["java", "-Djava.security.egd=file:/dev/./urandom", "-jar", "app.jar"]