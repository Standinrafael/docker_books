
#docker build -t app-authors .
#docker run -i --rm -p 9090:9090 app-authors
#docker run -d --name authors01 -p 9090:9090 app-authors

#docker tag app-authors violentpanda1007/app-authors
#docker login
#docker push violentpanda1007/app-authors

FROM eclipse-temurin:17.0.10_7-jre-alpine

RUN mkdir /app
WORKDIR /app

COPY build/quarkus-app/app ./app
COPY build/quarkus-app/lib ./lib
COPY build/quarkus-app/quarkus ./quarkus
COPY build/quarkus-app/quarkus-run.jar app.jar

CMD ["java","-jar","app.jar"]
