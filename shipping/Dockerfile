FROM maven:3.9.16 AS builder
WORKDIR /app
COPY pom.xml .
COPY src ./src
RUN mvn clean package 
RUN mv target/shipping-1.0.jar shipping.jar 
ENV CART_ENDPOINT=cart:8080 \
    DB_HOST=mysql:3306
EXPOSE 8080
CMD ["java", "-jar", "shipping.jar"]