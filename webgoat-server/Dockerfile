FROM azul/zulu-openjdk:15

ARG webgoat_version=v8.2.0-SNAPSHOT

RUN useradd --home-dir /home/webgoat --create-home -U webgoat

USER webgoat
WORKDIR /home/webgoat
COPY target/webgoat-server-*.jar /home/webgoat/webgoat.jar

EXPOSE 8080
ENTRYPOINT ["java", "-jar", "/home/webgoat/webgoat.jar", "--server.address=0.0.0.0", "--server.port=8080"]
