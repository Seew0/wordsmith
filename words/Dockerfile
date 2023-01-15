FROM maven:adoptopenjdk as build

WORKDIR /home/lab

COPY pom.xml .

RUN mvn verify -DskipTests --fail-never

COPY . .

RUN mvn verify

FROM adoptopenjdk:8-jre

EXPOSE 8080

WORKDIR /app

COPY --from=build /home/lab/target .

CMD [ "java", "-Xmx8m" , "-Xms8m", "-jar" , "/app/words.jar"]