# docker-github-actions-demo

# GitHub Actions Demo

This repository contains a simple GitHub Actions workflow that builds a Docker image and pushes it to DockerHub. The Docker image is a simple application that prints your name.

## Usage

To use this repository, follow these steps:

1. Fork the repository to your own GitHub account.
2. Clone the repository to your local machine.
3. Modify the Dockerfile to include your name or any other customizations you want.
4. Commit and push your changes to the `master` branch.
5. GitHub Actions will automatically trigger a build and push the Docker image to DockerHub.

## Prerequisites

Before using this repository, make sure you have the following:

- A DockerHub account
- Docker installed on your local machine
- GitHub Actions enabled for your repository

## Configuration

To configure the GitHub Actions workflow, you need to set up the following secrets in your repository settings:

- `DOCKER_USERNAME`: Your DockerHub username
- `DOCKER_PASS`: Your DockerHub password or access token

## Running the Docker Image

To run the Docker image, follow these steps:

1. Pull the Docker image from DockerHub using the following command:

```bash
docker pull <your-dockerhub-username>/<image-name>:<tag>
```

Replace `<your-dockerhub-username>` with your DockerHub username, `<image-name>` with the name of the Docker image, and `<tag>` with the desired tag (e.g., `latest`).

2. Run the Docker image using the following command:

```bash
docker run <your-dockerhub-username>/<image-name>:<tag>
```

Replace `<your-dockerhub-username>` with your DockerHub username, `<image-name>` with the name of the Docker image, and `<tag>` with the desired tag (e.g., `latest`).

The Docker container will start and the application will print your name.

Note: Make sure Docker is running on your local machine before running the Docker image.

# For example running my Docker image

## Step 1: Pull the Docker image from DockerHub

```bash
docker pull ahmedmohammed24/github-actions-demo
```

## Step 2: Run the Docker image

```bash
docker run -it --rm ahmedmohammed24/github-actions-demo
```

- `-it`: Enables an interactive mode, allowing you to interact with the application within the Docker container.
- `--rm`: Automatically removes the container after it stops, keeping your system clean. This is useful for temporary containers like this demo.
