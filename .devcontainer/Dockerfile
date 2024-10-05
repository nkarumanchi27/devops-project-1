# Use the Python 3.9 image as the base
FROM mcr.microsoft.com/vscode/devcontainers/python:3.9

# Install gcloud SDK
RUN apt-get update && \
    apt-get install -y apt-transport-https ca-certificates gnupg && \
    echo "deb [signed-by=/usr/share/keyrings/cloud.google.gpg] https://packages.cloud.google.com/apt cloud-sdk main" | tee -a /etc/apt/sources.list.d/google-cloud-sdk.list > /dev/null && \
    curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | apt-key --keyring /usr/share/keyrings/cloud.google.gpg add - && \
    apt-get update && \
    apt-get install -y google-cloud-sdk

# Install any other additional packages or tools here if needed

# Set the default working directory
WORKDIR /workspace

# Install any Python dependencies if you add them later
# (Uncomment the below line if you have a requirements.txt)
# COPY requirements.txt .
# RUN pip install -r requirements.txt

# Expose any ports (if necessary for your project)
# EXPOSE 8080

