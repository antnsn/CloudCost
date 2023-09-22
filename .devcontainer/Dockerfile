echo 'FROM python:3.9-slim

# Avoid warnings by switching to noninteractive
ENV DEBIAN_FRONTEND=noninteractive

# Install OS dependencies
RUN apt-get update && apt-get install -y --no-install-recommends \
    curl \
    git \
    && apt-get clean -y && rm -rf /var/lib/apt/lists/*

# Switch back to dialog for any ad-hoc use of apt-get
ENV DEBIAN_FRONTEND=dialog

# Set the working directory
WORKDIR /workspace

# Install Azure SDKs for Python
RUN pip install azure-mgmt-costmanagement azure-identity' > .devcontainer/Dockerfile
