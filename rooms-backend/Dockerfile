FROM maven:3.8.1-openjdk-16-slim AS build  
COPY src /usr/src/app/src  
COPY pom.xml /usr/src/app  
#RUN mvn -f /usr/src/app/pom.xml clean package
RUN --mount=type=cache,target=/root/.m2 mvn -f /usr/src/app/pom.xml clean package -Dmaven.test.skip

FROM gcr.io/distroless/java  
COPY --from=build /usr/src/app/target/*.jar /usr/app/app.jar  
ENTRYPOINT ["java","-jar","/usr/app/app.jar"] 