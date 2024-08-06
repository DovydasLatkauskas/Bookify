# Bookify

**Bookify** is a manually-hosted web application designed to connect customers seeking various services (e.g., a haircut, dry cleaning) with businesses providing those services. This project features a comprehensive suite of functionalities, including service discovery, appointment booking, and client management. The platform is designed to streamline the process of service management and booking for both providers and customers.

## Code Access

The website is intended for production thus not open-source

Email me at dovydas@dovydas.one to receive access
## Features

- **Service Discovery**: Easily search and discover a variety of businesses.
- **Appointment Booking**: Seamlessly schedule appointments for services.
- **Client Management**: Manage client interactions and service records efficiently.

## Technology Stack

- **Frontend**:
  - HTMX
  - Tailwind CSS
  - Alpine.js
  - Razor Pages
- **Backend**:
  - ASP.NET Core (.NET 8)
  - Entity Framework Core
- **Database**: PostgreSQL
- **Containerization**: Docker Compose
- **CDN and Security**: Cloudflare for CDN, DNS, DDoS protection
- **Reverse Proxy**: Nginx 
- **Hosting**:
  - Dev environment: Self-hosted on Arch Linux
  - Test environment: AWS EC2

## Development and Deployment

- **Testing**: Comprehensive unit and integration tests ensure the reliability and robustness of the application.
- **CI/CD**: Automated builds and deployments using GitHub Actions.
- **Logging and Observability**: Implemented extensive logging and observability features to monitor application performance and health.
- **Scripts and Services**: Custom bash scripts for setting up Arch/Ubuntu Linux VMs, along with Systemctl services for managing CI/CD pipelines and other processes.
- **Environments**: Created separate development and test environments to ensure smooth development and deployment processes.

## Roadmap

- **Load Testing**: Conduct load testing to evaluate the application's performance under stress.
- **Database Backups**: Implement regular database backup mechanisms to prevent data loss.
- **Switch to Kubernetes**: No downtime deployments, running separate sites for separate regions

## Getting Started

### Prerequisites

- A virtual machine, virtual private server, or a physical server
- Access to the codebase (Email dovydas@dovydas.one for access)

### Installation
1. **Install Arch Linux** on your server.
2. **Copy the codebase** to the server.
3. **Build and run the application** using Docker Compose:
    ```bash
    cd Bookify/scripts
    chmod +x setup-vm.sh
    ./setup-vm.bash
    chmod +x deploy.sh
    ./deploy.sh
    ```

4. **Access the application**: Open a web browser and navigate to `{your server's IP}:8080`

### Running Tests

Run unit and integration tests using the following command:
```bash
dotnet test
```

## CI/CD Pipeline

- **Continuous Integration**: On every push, the tests are run automatically.
- **Continuous Deployment**: If the tests pass, a new version is deployed to the server using the GitHub Actions runner.

## Deployment

This application is hosted at [https://dovydas.one/](https://dovydas.one/) on AWS EC2. The deployment process is automated using GitHub Actions, which handles building, testing, and deploying the application. The dev environment is self-hosted on an old laptop running Arch Linux.

## Architecture

- **Database**: PostgreSQL for data storage, with robust data management and querying capabilities.
- **Containerization**: Docker and Docker Compose for managing service lifecycles and ensuring consistent environments.
- **Reverse Proxy**: Nginx for handling different environments, logging, and monitoring requests.
- **CDN and Security**: Cloudflare for enhanced security and performance optimization.

## Observability and Monitoring

Implemented extensive logging and observability to monitor application performance and troubleshoot issues effectively. This includes:

- **Structured Logging**: Capturing detailed logs for monitoring application behavior.
- **Performance Metrics**: Collecting and analyzing performance metrics to ensure optimal operation.

## License

This project is licensed under a proprietary license. All rights are reserved, and the source code is not open for redistribution or modification
