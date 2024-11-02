# Multi-Architecture Docker Image for FastAPI Hello World

This repository demonstrates how to build and deploy a multi-architecture Docker image for a simple "Hello World" application using FastAPI. The primary goal is to provide a guide for building and pushing Docker images for multiple architectures (such as `linux/amd64` and `linux/arm64`) to Docker Hub, following best practices in containerization.

## About the Project

This project is built with FastAPI, a modern, fast (high-performance), and asynchronous web framework for Python. The application itself is a simple "Hello World" app designed to demonstrate how to create, containerize, and distribute multi-architecture Docker images. The repository includes:

- A **Dockerfile** following security best practices, including running the application as a non-root user.
- A **GitHub Action** workflow that builds and pushes the Docker image to Docker Hub for both `amd64` and `arm64` architectures.

## Key Features

- **Multi-architecture Docker build:** Ensures compatibility across various platforms.
- **GitHub Actions integration:** Automates the process of building and pushing images to Docker Hub.
- **Security best practices:** Runs the application as a non-root user within the container.

## Getting Started

To pull and run this image:

1. **Pull the image:**

    ```bash
    docker pull <DOCKERHUB_USERNAME>/multi-arch-fastapi-docker:latest
    ```

2. **Run the container:**

    ```bash
    docker run -d -p 8000:8000 <DOCKERHUB_USERNAME>/multi-arch-fastapi-docker:latest
    ```

3. **Access the application at [http://localhost:8000](http://localhost:8000).**

## Repository Structure

- **Dockerfile:** Defines the environment, installs dependencies, and specifies the non-root user.
- **requirements.txt:** Lists required Python packages, including `fastapi[standard]`
- **GitHub Workflow:** Automates the multi-architecture Docker build and push to Docker Hub.

## Contributing

Contributions are welcome! Please fork this repository and submit a pull request if you'd like to add improvements or features.
