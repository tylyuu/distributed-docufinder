# Distributed DocuFinder

## Overview

Distributed DocuFinder is a full-stack document search system designed to handle large-scale data with high efficiency and reliability. The system architecture is split into two main components: a frontend webserver and a backend search cluster.

## Project Architecture

The diagram below illustrates the architecture and data flow within the application. The modular design ensures seamless communication and efficient data handling.

![Distributed DocuFinder Architecture](https://github.com/tylyuu/distributed-docufinder/assets/114101094/24b287d8-dd69-4c2a-8f57-394a5ef7fb76)

## Features

- **Dynamic Cluster Management**: Utilizes Apache ZooKeeper for dynamic leader election and service registry, enhancing scalability and fault tolerance.
- **Advanced Searching Capabilities**: Implements the DF-ITF algorithm for sophisticated data partitioning and parallel processing, ensuring quick and accurate search results.
- **Loose Coupling**: The system's components are loosely coupled, promoting flexibility and ease of maintenance.
- **Efficient Communication**: API endpoints are established for efficient communication between the frontend server, the coordinator, and worker nodes using Protocol Buffers over HTTP requests.
- **Optimized Data Models**: Custom data models are designed for optimal data serialization, supporting high-performance data exchanges.

## Getting Started

### Prerequisites

Before setting up the system, ensure you have the following installed:
- Apache Maven
- Apache ZooKeeper
- Java Development Kit (JDK) version 8 or higher

### Building the Application

Execute the following Maven command in the terminal to build both the frontend and backend components of the application:

```shell
mvn clean package
```

## Running the Application

Follow these steps to get the system up and running:

1. **Start Apache ZooKeeper Server**: Initialize the Apache ZooKeeper server on your chosen machine.

2. **Launch Frontend Server**: Execute the frontend server JAR, which should automatically establish a connection with the ZooKeeper server.

3. **Activate ZooKeeper Worker Nodes**: Deploy the worker nodes by running their respective JAR files.

