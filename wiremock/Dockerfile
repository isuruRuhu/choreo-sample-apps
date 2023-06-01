# Create a new user with UID 10014
FROM openjdk:11-alpine
WORKDIR /wiremock
COPY mappings/ /wiremock/mappings/

# https://security.alpinelinux.org/vuln/CVE-2021-46848
RUN apk add --upgrade libtasn1-progs

# https://security.alpinelinux.org/vuln/CVE-2022-37434
RUN apk update && apk upgrade zlib

RUN addgroup -g 10014 choreo && \
    adduser  --disabled-password  --no-create-home --uid 10014 --ingroup choreo choreouser
VOLUME /tmp
USER 10014

EXPOSE 8080
CMD ["java", "-jar", "wiremock-standalone.jar", "--port", "8080", "--root-dir", "/wiremock"]

