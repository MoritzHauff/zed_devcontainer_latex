# Use texlive base image as a parent image
FROM docker.io/texlive/texlive:latest

# Create the non-root user 'vscode' (UID/GID 1000) like the official devcontainer base images
RUN groupadd --gid 1000 vscode \
    && useradd --uid 1000 --gid 1000 --create-home --shell /bin/bash vscode \
    && echo 'vscode ALL=(ALL) NOPASSWD:ALL' > /etc/sudoers.d/vscode \
    && chmod 0440 /etc/sudoers.d/vscode

# Set the default user to 'vscode'
USER vscode

# Set the working directory to /home/vscode/work/
WORKDIR /home/vscode/work/
