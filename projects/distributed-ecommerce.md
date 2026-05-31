# 🛒 Distributed E-Commerce System

> Event-driven e-commerce system for scalable and fault-tolerant order processing using Apache Kafka.

[← Back to Profile](../README.md) | [→ View Team Repository](https://github.com/DS-Kafka/Kafka-)

---

## Overview

This system implements a distributed e-commerce architecture where order processing is handled asynchronously through Apache Kafka. When a purchase request is made, it is published to a Kafka topic and consumed by downstream services independently — decoupling the frontend from backend processing and enabling fault-tolerant, scalable order handling.

The system also features real-time order status updates via WebSocket, allowing the frontend to reflect changes instantly without polling.

## Tech Stack

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Apache Kafka](https://img.shields.io/badge/Apache_Kafka-231F20?style=for-the-badge&logo=apachekafka&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)

## System Architecture

The system is composed of the following components running in Docker containers:

- **Frontend** — User interface for placing orders
- **Backend** — REST API that receives purchase requests and publishes events to Kafka (`buy_topic`)
- **Apache Kafka + Zookeeper** — Message broker handling asynchronous order event streaming
- **MySQL** — Persistent storage for order data
- **WebSocket Servers** — Two real-time servers (port 8083 & 8085) pushing order status updates to the frontend
- **Nginx** — Reverse proxy routing traffic between services

## Key Features

- **Event-driven order processing** via Kafka `buy_topic` for asynchronous, fault-tolerant communication
- **Real-time order updates** via WebSocket without frontend polling
- **Containerized deployment** with Docker Compose for consistent, reproducible environments
- **Bottleneck analysis** through component and sequence diagrams
- **Performance evaluation** under high concurrency using Grafana k6 load testing

## My Contributions

- Contributed to system architecture design through collaborative discussions
- Created sequence diagrams to document event flows between services
- Independently designed and implemented the WebSocket layer for real-time order status updates
- Evaluated system performance under high concurrency using Grafana k6 load testing

## Team Repository

The full source code, setup instructions, and documentation are available in the team repository:

**[→ View Team Repository](https://github.com/DS-Kafka/Kafka-)**