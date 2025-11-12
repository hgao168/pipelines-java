# Hello World Kubernetes Application

This project is a simple web application that responds with "Hello, World!" when accessed. It is designed to be containerized using Docker and deployed to a Kubernetes cluster.

## Project Structure

```
hello-world-k8s
├── src
│   └── index.js          # Entry point of the application
├── Dockerfile             # Dockerfile for building the application image
├── .dockerignore          # Files to ignore when building the Docker image
├── k8s
│   ├── deployment.yaml    # Kubernetes deployment configuration
│   ├── service.yaml       # Kubernetes service configuration
│   └── ingress.yaml       # Kubernetes ingress configuration
├── package.json           # npm configuration file
├── .gitignore             # Files to ignore in Git
├── Makefile               # Build automation directives
└── README.md              # Project documentation
```

## Getting Started

### Prerequisites

- Docker
- Kubernetes (Minikube, GKE, EKS, etc.)
- Node.js and npm

### Building the Docker Image

To build the Docker image, run the following command:

```
docker build -t hello-world-k8s .
```

### Running the Application Locally

To run the application locally, you can use the following command:

```
node src/index.js
```

### Deploying to Kubernetes

1. Apply the deployment configuration:

   ```
   kubectl apply -f k8s/deployment.yaml
   ```

2. Apply the service configuration:

   ```
   kubectl apply -f k8s/service.yaml
   ```

3. (Optional) Apply the ingress configuration:

   ```
   kubectl apply -f k8s/ingress.yaml
   ```

### Accessing the Application

Once deployed, you can access the application through the service or ingress, depending on your configuration.

## License

This project is licensed under the MIT License. See the LICENSE file for details.