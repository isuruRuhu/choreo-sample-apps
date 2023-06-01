# Create a new user with UID 10014
FROM openjdk:11
WORKDIR /wiremock
COPY mappings/ /wiremock/mappings/

RUN addgroup -g 10014 choreo && \
    adduser  --disabled-password  --no-create-home --uid 10014 --ingroup choreo choreouser
VOLUME /tmp
USER 10014

EXPOSE 8080
CMD ["java", "-jar", "wiremock-standalone.jar", "--port", "8080", "--root-dir", "/wiremock"]

