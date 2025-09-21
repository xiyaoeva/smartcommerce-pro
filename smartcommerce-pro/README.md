
# SmartCommerce Pro

A distributed microservices-based e-commerce platform skeleton.  
Tech stack: **Java 17, Spring Boot 3, Spring Cloud, RocketMQ, Kafka, Redis, MySQL, AWS (deployment-ready)**.

## Features
- Distributed microservices with Spring Cloud
- Flash-sale simulation (10K QPS target capacity)
- Asynchronous messaging with RocketMQ & Kafka (stubs included)
- Inventory optimization using Redis locks (stubbed)
- Service discovery and registration with Nacos/Eureka
- Deployment-ready for AWS EC2 with auto-scaling

## Run Locally
```bash
# Build all services
./mvnw clean package -DskipTests

# Run one service
java -jar gateway-service/target/gateway-service-0.0.1-SNAPSHOT.jar
```

## Docker (for Redis + MySQL)
```bash
docker-compose up -d
```

## Modules
- `gateway-service` — API Gateway
- `product-service` — Product catalog + inventory
- `order-service` — Order processing

---
This is a **skeleton project** — extend business logic, add DB schemas, and implement async consumers for RocketMQ/Kafka.
