FROM amazoncorretto:17.0.7-alpine
RUN apk add --no-cache bash wget curl dos2unix

COPY  settings.json /settings.json
COPY  protocol-runner.jar /protocol-runner.jar
COPY  protocol-dns-plugin.jar /protocol-dns-plugin.jar

COPY  ./start.sh /tpmrunner.sh
RUN dos2unix /tpmrunner.sh
RUN chmod +x /tpmrunner.sh
ENTRYPOINT ["/tpmrunner.sh"]

# Debug
EXPOSE 5005
# APIs
EXPOSE 8081
# Dns
EXPOSE 53
# Redis
EXPOSE 6379
# MySQL
EXPOSE 3306
# Postgres
EXPOSE 5432
# Mqtt
EXPOSE 1883
# AMQP
EXPOSE 5672
# MongoDB
EXPOSE 27017
# Http/Https/Proxy
EXPOSE 80
EXPOSE 443
EXPOSE 9000

HEALTHCHECK --interval=3s --retries=30  CMD curl --fail http://localhost:8081/api/status || exit 1