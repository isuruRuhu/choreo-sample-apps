FROM adoptopenjdk:11-jre-hotspot
WORKDIR /wiremock
COPY mappings/ /wiremock/mappings/
EXPOSE 8080

USER 10014
COPY /wiremock-jre8-standalone-2.35.0.jar .

CMD ["java", "-jar", "wiremock-jre8-standalone-2.35.0.jar", "--port", "8080", "--root-dir", "/wiremock"]
