# Use the official Ubuntu 20.04 LTS image as the base image
FROM ubuntu:20.04

# Set environment variables (optional)
ENV DEBIAN_FRONTEND=noninteractive \
    LANG=C.UTF-8 \
    LC_ALL=C.UTF-8

# Update the package repository and install essential packages
RUN apt-get update && \
    apt-get install -y \
    software-properties-common \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg \
    lsb-release \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Install additional packages or perform other setup steps as needed
# For example, installing a text editor (nano in this case)
RUN apt-get update && \
    apt-get install -y nano \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

# Set the default working directory
WORKDIR /app

# Optional: Expose any necessary ports
# EXPOSE 80

# Optional: Define a default command to run when the container starts
# CMD ["/bin/bash"]
