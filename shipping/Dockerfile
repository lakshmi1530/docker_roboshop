FROM maven:3.8.4
WORKDIR /app
COPY pom.xml .
COPY src ./src
RUN mvn clean package
EXPOSE 8080
ENV CART_URL="cart" \
    CART_PORT="8080" \
    DB_HOST="mysql"
CMD ["java", "-jar", "shipping.jar"]