FROM gradle:7.6.11-jdk11 AS build

WORKDIR /app

COPY build.gradle setting.gralde ./

RUN gradle dependencies --no-daemon

COPY . /app

RUN gradle clean build --no-daemon

FROM openjdk:11-jre-slim

COPY --from=build /app/build/libs/*.jar /app/leafy.jar

EXPOSE 8080

ENTRYPOINT ["java"]
CMD ["jar", "leafy.jar"]

