# stage 1 : build
FROM maven:3.9-eclipse-temurin-17 AS builder
WORKDIR /app

COPY pom.xml .
# "télécharge mes ingrédients maintenant"

RUN mvn dependency:go-offline
# ce layer est caché tant que pom.xml ne change pas
# maintenant tu copies le code
COPY src/ ./src/

# compile avec les deps déjà en cache
RUN mvn clean package

# stage 2 : run
FROM eclipse-temurin:17-jdk-alpine
WORKDIR /app
COPY --from=builder /app/target/*.jar app.jar
EXPOSE 8080
ENTRYPOINT ["java", "-jar", "app.jar"]