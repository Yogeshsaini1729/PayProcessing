# PayProcessing

## Overview
PayProcessing is a microservices-based payment integration system designed to act as a middleware between clients and payment service providers (PSPs). The system is built using **Spring Boot** and **Stripe** for seamless payment processing. It includes multiple services for validation, processing, and provider integration.

## Features
- **Secure Payment Validation**: Implements **OAuth2.0**, **HMAC-SHA256**, and **Spring Boot Security** for authentication and validation.
- **Dynamic Business Rules**: Supports flexible validation of payment fields based on dynamic business rules.
- **Payment Processing**: Manages payment transactions, status updates, and notifications using **ActiveMQ**.
- **Stripe Integration**: Interacts with Stripe for session creation, payment status retrieval, and expiration handling.
- **Asynchronous Communication**: Uses **Redis Cache** and **ActiveMQ** for message queuing and inter-service communication.
- **AWS Deployment**: Hosted on **AWS EC2** with **RDS**, **Secret Manager**, and scalable architecture.

## Architecture
The system consists of three key services:
1. **Payment Validation Service**: Handles authentication, request validation, and dynamic rule enforcement.
2. **Payment Processing Service**: Manages transaction workflows and communicates with the provider service.
3. **Stripe Provider Service**: Interfaces with Stripe for payment execution and confirmation.

## Technology Stack
- **Backend**: Java, Spring Boot, Spring Security
- **Messaging & Caching**: ActiveMQ, Redis
- **Database**: AWS RDS (PostgreSQL/MySQL)
- **Payment Integration**: Stripe API
- **Deployment**: AWS EC2, AWS Secret Manager

## Installation & Setup
1. Clone the repository:
   ```sh
   git clone https://github.com/Yogeshsaini1729/Payprocessing.git
   cd Payprocessing
   ```
2. Configure environment variables for **AWS**, **Stripe**, and **Database** in `application.properties`.
3. Build and run the application:
   ```sh
   mvn clean install
   mvn spring-boot:run
   ```



## Contributing
1. Fork the repository.
2. Create a feature branch:
   ```sh
   git checkout -b feature-name
   ```
3. Commit your changes:
   ```sh
   git commit -m "Added new feature"
   ```
4. Push and open a pull request.

## License
This project is licensed under the **MIT License**.

---
Feel free to contribute and improve **PayProcessing**!

