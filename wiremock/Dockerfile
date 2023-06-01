FROM adoptopenjdk:11-jre-hotspot
WORKDIR /wiremock
COPY mappings/ /wiremock/mappings/
EXPOSE 8080

USER 10014

CMD ["java", "-jar", "wiremock-standalone.jar", "--port", "8080", "--root-dir", "/wiremock"]
