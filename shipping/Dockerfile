
# Stage 1 compile / Build code convert into jar file 

FROM maven AS build

WORKDIR /opt/shipping

COPY pom.xml /opt/shipping/
RUN mvn dependency:resolve
COPY src /opt/shipping/src/
RUN mvn package

# stage 2 to run the code 

FROM openjdk:8-jdk

EXPOSE 8080

WORKDIR /opt/shipping

COPY --from=build /opt/shipping/target/shipping-1.0.jar shipping.jar

CMD [ "java", "-Xms1750m", "-Xmx1750m", "-jar", "shipping.jar" ]
