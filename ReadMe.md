# Go Microservices Example Project

This project is an example of a microservices architecture implemented in Go, showcasing deployment and testing strategies using Docker Swarm and Kubernetes. It's designed as a practical guide following a tutorial attended on building, deploying, and managing microservices.

## Services Overview

The application is composed of several microservices, each serving a unique function within the system:

- **Broker Service**: Manages message brokering and distribution between services using RabbitMQ.
- **Auth Service**: Handles authentication and authorization, ensuring secure access to the system.
- **Mail Service**: Responsible for sending emails, notifications, and other communication.
- **Log Service**: Captures and stores logs from various services, aiding in monitoring and debugging.
- **Listener Service**: Listens for messages on RabbitMQ and performs actions based on the message content.

## Database

The application utilizes two types of databases to store its data:

- **MongoDB**: A NoSQL database used for storing unstructured data.
- **PostgreSQL**: A relational database management system used for structured data storage.

## Deployment

### Docker Swarm

The project is configured to run on Docker Swarm, enabling it to scale across multiple Docker hosts and manage its microservices efficiently. The `docker-compose.yml` file contains the necessary configuration to deploy the services to a Swarm cluster.

### Kubernetes

For Kubernetes deployment, the project includes a set of YAML configuration files under the `k8s` directory. These files define the necessary Kubernetes resources such as Deployments, Services, and Ingress rules required to deploy and expose the microservices on a Kubernetes cluster.

## Testing

Testing strategies for microservices include unit testing individual services and integration testing the interaction between services. The project includes example tests demonstrating how to mock dependencies and test services in isolation.

## Getting Started

To get started with this project, clone the repository and follow the setup instructions for either Docker Swarm or Kubernetes deployment. Ensure you have Docker, Docker Compose, and Kubernetes CLI tools installed on your system.

## Contributing

Contributions to the project are welcome. Please follow the standard fork and pull request workflow. Ensure you write tests for new features and document your changes.

## License

This project is licensed under the MIT License - see the LICENSE file for details.